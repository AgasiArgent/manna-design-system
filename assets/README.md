# Manna Coffee — Brand Assets

Master files for all brand-facing outputs. **Source of truth** for design-system.md anchors.

## Structure

```
brand-assets/
├── logo-pdf/        # Master vector files from CEO's designer (CorelDRAW 2024)
├── logo-preview/    # PNG previews (150 DPI) for quick visual reference
├── favicon/         # Browser/PWA/Apple touch icons + clean SVG
├── social/          # OG/Twitter/Instagram social previews
├── tokens/          # Design tokens — Figma Tokens Studio + W3C formats
└── README.md        # This file
```

## logo-pdf/ — Master files

Vector PDFs. Edit in Illustrator / Inkscape / Affinity Designer. Never flatten to raster.

| File | Variant | Use |
|---|---|---|
| `Logo_manna_CLR.pdf` | Brandbook preview (logo + swatches + font label) | Reference only |
| `Logo_manna_1.pdf` | Horizontal · mint · transparent | Light-bg headers, one-pagers |
| `Logo_manna_2.pdf` | Vertical · mint · transparent | Stacked contexts, social avatars |
| `Logo_manna_3.pdf` | Horizontal · white · on forest | Dark headers, reverse-out |
| `Logo_manna_4.pdf` | Vertical · white · on forest | Dark stacked, merch, signage |

## favicon/ — Web icons

| File | Size | Use |
|---|---|---|
| `favicon.ico` | 16/32/48/64 (multi-size ICO) | Legacy browsers, default |
| `favicon.svg` | vector, forest | Modern browsers (scales perfectly) |
| `icon.svg` | vector, `currentColor` | Inherits via CSS for dark mode |
| `icon-white.svg` / `icon-mint.svg` | vector variants | Dark bg / brand-accent contexts |
| `icon-forest-{16..512}.png` | PNG sizes | Fallback, meta tags |
| `apple-touch-icon.png` | 180×180, mint on forest tile | iOS home screen |
| `icon-maskable-192.png` / `icon-maskable-512.png` | PWA maskable | Android home screen, PWA |

### HTML snippet

```html
<link rel="icon" href="/favicon.ico" sizes="32x32">
<link rel="icon" href="/favicon.svg" type="image/svg+xml">
<link rel="apple-touch-icon" href="/apple-touch-icon.png">
<link rel="manifest" href="/site.webmanifest">
<meta name="theme-color" content="#2E4B46">
```

## social/ — Social previews

| File | Size | Use |
|---|---|---|
| `og-image.png` | 1200×630 | Open Graph (Facebook, LinkedIn, Slack, iMessage), Twitter Summary Large |
| `og-square-1080.png` | 1080×1080 | Instagram feed, LinkedIn post |
| `story-1080x1920.png` | 1080×1920 | Instagram/Facebook Story, Reels cover |

### Meta tags

```html
<meta property="og:image" content="https://manna.coffee/og-image.png">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:image" content="https://manna.coffee/og-image.png">
```

## tokens/ — Design tokens

| File | Format | Use |
|---|---|---|
| `tokens.json` | Tokens Studio (legacy) | **Figma Tokens Studio plugin** — import directly |
| `tokens.w3c.json` | W3C DTCG draft | Style Dictionary, modern token tools |

### Figma import

1. Install [Tokens Studio for Figma](https://tokens.studio/) plugin
2. Plugin → Settings → JSON → Import from file
3. Select `tokens.json`
4. Apply to canvas — all color scales, fonts, spacing, radius, shadows available as Figma variables

## When to refresh

Regenerate outputs when:
- Brand anchors change (forest / mint / Baloo 2) → regenerate **all** favicons + social + tokens
- Color scales extended → regenerate tokens only
- New logo variants provided → add to `logo-pdf/` + re-render to `logo-preview/`

Never hand-edit generated files (favicon PNGs, OG images, tokens). Regenerate from the source PDFs and `design-system.md`.

## Provenance

- Master logos: CEO's designer (CorelDRAW 2024), received 2026-04-14
- Favicons / social / tokens: generated 2026-04-14 from master files + `design-system.md`
