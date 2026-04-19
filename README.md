# Manna Coffee — Design Bundle

Curated subset of the Manna Coffee brand + design system for feeding into design tools.

**Brand:** Manna Smart Retail Inc (Miami, FL) — automated bean-to-cup smart coffee kiosks.
**Slogan:** Coffee, Love & Robots.
**Architecture:** Hybrid system — Brand Core (official, from CEO's designer) + Digital System (extensions for web/UI).

## What's here

| File | Purpose |
|---|---|
| `design-system.md` | **Primary source of truth.** Full tokens — colors (Forest/Mint/Coral/Warm/Ink scales), typography (Baloo 2 + Manrope + JetBrains Mono), spacing, radius, shadows, components, dark mode. |
| `brand-foundation.md` | Brand story, mission, vision, personality, audience positioning. |
| `tone-of-voice.md` | Voice guide — say/don't-say, tone by context, copy examples. |
| `assets/README.md` | How the binary assets are organized. |
| `assets/tokens.w3c.json` | Design tokens in W3C DTCG format (Style Dictionary, modern tools). |
| `assets/tokens.json` | Design tokens in Figma Tokens Studio format. |
| `assets/logos/` | Master vector logos — 5 PDF variants (horizontal/vertical × mint/white). |
| `assets/favicons/` | Browser + PWA + Apple touch icons (SVG + PNG all sizes). |
| `assets/social/` | OG image, Instagram square, Story, LinkedIn banner. |
| `assets/fonts/` | Self-hosted fonts — Baloo 2 (500/600/700/800), Manrope (400/500/600/700), JetBrains Mono (400/500). TTF + WOFF2, OFL 1.1. |

## Anchor values (quick reference)

- **Primary Dark (Forest):** `#2E4B46` — body color, primary buttons
- **Accent Light (Mint):** `#98E086` — highlights, success, logo-green
- **CTA (Coral, extension):** `#FF6B55` — conversion buttons only
- **Warm (Coffee, extension):** `#C4956A` — craft/premium moments
- **Ink (Dark text):** `#141D24` — body text, dark mode base
- **Brand font:** Baloo 2 (rounded, friendly, single-font brand voice)
- **UI font (extension):** Manrope (dense data, long admin labels)

## How to use this bundle

1. Read `design-system.md` first — it's the complete spec.
2. Use `brand-foundation.md` + `tone-of-voice.md` for voice/copy decisions.
3. Pull exact values from `assets/tokens.w3c.json` when generating code.
4. Reference logos in `assets/logos/` by variant (1=horizontal mint, 2=vertical mint, 3=horizontal white, 4=vertical white, CLR=brandbook preview).

## Legacy note

HTML materials created before 2026-04-14 use a pre-official palette (`#3D7A6E` teal + `#7BD96B` mid-green + Space Grotesk). That's **off-brand** — use the anchors above instead.
