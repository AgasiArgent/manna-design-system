# Manna Coffee — Brand Design System

**Slogan:** Coffee, Love & Robots
**Brand Essence:** Specialty coffee craft meets smart automation. Premium but accessible, tech-forward but warm.
**Target:** Entrepreneurs and small business operators in the US.

**Architecture:** Hybrid system. [Brand Core](#brand-core-official) = official decisions from CEO's designer (logo, 3 anchor colors, brand font). [Digital System Extended](#digital-system-extended) = our additions for web/dashboards/materials (full color scales, CTA color, dark mode, UI font pairing, component tokens).

---

## Brand Core (Official)

Source of truth for brand identity. Do not override these in brand-facing surfaces (landing hero, logo uses, key marketing headlines, physical materials).

### Logo

Master files: `brand-assets/logo-pdf/` — vector PDFs from CorelDRAW 2024, fonts outlined. Scale infinitely.

| File | Variant | Use |
|---|---|---|
| `Logo_manna_CLR.pdf` | Brandbook preview (logo + swatches + font) | Reference only — not for placement |
| `Logo_manna_1.pdf` | Horizontal, light green, transparent | Website headers on light bg, one-pagers |
| `Logo_manna_2.pdf` | Vertical, light green, transparent | Stacked contexts, social avatars, badges |
| `Logo_manna_3.pdf` | Horizontal, white, on dark green | Dark headers, reverse-out marketing |
| `Logo_manna_4.pdf` | Vertical, white, on dark green | Dark stacked contexts, merch, signage |

PNG previews at 150 DPI live in `brand-assets/logo-preview/` for quick embedding in docs.

**Concept:** Stylized praying hands / mountain silhouette with light rays above — evokes abundance, craft, and arrival (biblical manna).

**Minimum clear space:** 1× height of the "M" on all sides.

### Anchor Colors

| Role | Hex | Meaning |
|---|---|---|
| **Primary Dark (Forest)** | `#2E4B46` | Deep, grounded, premium. Brand body color, dark backgrounds, primary text on light bg. |
| **Accent Light (Mint)** | `#98E086` | Fresh, alive, "go." Brand accent, highlight marks, logo in light contexts, success states. |
| **Black** | `#000000` | Hard contrast — used in official brandbook on reverse-out samples. |

### Brand Font

**Baloo 2** — rounded, friendly sans. Used for **both headline and body** in the official brandbook (single-font brand voice — warm and approachable, not corporate).

```html
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@400;500;600;700;800&display=swap" rel="stylesheet">
```

Weights available: 400, 500, 600, 700, 800. Default display = 700, body = 500.

---

## Digital System (Extended)

Extensions built around the Brand Core for web, dashboards, sales materials, dense data UIs. Use these when the 3 anchor colors + single font aren't sufficient (forms, tables, semantic states, dark mode, long-form reading).

### Color Scales

Full 50-900 scales derived from the brand anchors. Use shade numbers (`primary-500`, `accent-200`) in CSS tokens rather than raw hex.

#### Primary — Forest (anchor: #2E4B46 at 500)

Trust, premium quality, grounded professionalism.

| Shade | Hex | Usage |
|---|---|---|
| 50 | `#EEF2F1` | Page backgrounds, subtle tints |
| 100 | `#D8E1DF` | Hover backgrounds, cards |
| 200 | `#B2C4C0` | Borders, dividers |
| 300 | `#8BA6A0` | Disabled states, secondary elements |
| 400 | `#5C7973` | Placeholder text, icons |
| **500** | **`#2E4B46`** | **Brand body color, primary buttons, links (official anchor)** |
| 600 | `#263D39` | Button hover |
| 700 | `#1E302D` | Active/pressed |
| 800 | `#162321` | Dark text on light bg |
| 900 | `#0E1614` | Darkest forest |

#### Accent — Mint (anchor: #98E086 at 500)

Energy, growth, freshness, "go" signals.

| Shade | Hex | Usage |
|---|---|---|
| 50 | `#F4FCF1` | Success backgrounds |
| 100 | `#E6F8E1` | Light green cards |
| 200 | `#CCF1C3` | Tags, badges, light fills |
| 300 | `#B3E9A5` | Progress bars, charts |
| 400 | `#A6E496` | Secondary accents |
| **500** | **`#98E086`** | **Accent (official anchor) — highlights, success, logo-green** |
| 600 | `#7BC36B` | Accent hover |
| 700 | `#5FA051` | Accent active |
| 800 | `#437639` | Dark accent text |
| 900 | `#294A22` | Darkest green |

#### CTA — Coral *(extension, not in brand core)*

Action, urgency. Brand core has no call-to-action color; coral was added for conversion surfaces (buy buttons, "Get Started"). Use **sparingly** — overuse dilutes the Forest/Mint identity.

| Shade | Hex | Usage |
|---|---|---|
| 50 | `#FFF3F1` | Error/warning bg |
| 100 | `#FFE4E0` | Light alert cards |
| 200 | `#FFCBC4` | Notification badges |
| 300 | `#FFAEA2` | CTA hover states |
| 400 | `#FF8C7A` | Secondary CTA |
| **500** | **`#FF6B55`** | **Primary CTA buttons** |
| 600 | `#D95B48` | CTA hover |
| 700 | `#B34B3C` | CTA active |
| 800 | `#80362B` | Error text |
| 900 | `#4D201A` | Critical alerts |

#### Warm — Coffee *(extension, not in brand core)*

Warmth, craft, coffee heritage. Use for testimonials, "bean-to-cup" messaging, premium/quality moments where Forest feels too cool.

| Shade | Hex | Usage |
|---|---|---|
| 50 | `#FAF7F3` | Warm page backgrounds |
| 100 | `#F4ECE4` | Coffee-tinted cards |
| 200 | `#EADACB` | Borders in warm contexts |
| 300 | `#DFC5AD` | Decorative elements |
| 400 | `#D1AC8B` | Icons, warm accents |
| **500** | **`#C4956A`** | **Coffee/craft accent** |
| 600 | `#A77F5A` | Warm hover |
| 700 | `#89684A` | Warm active |
| 800 | `#624B35` | Dark warm text |
| 900 | `#3B2D20` | Darkest coffee |

#### Neutral — Ink (for text + digital dark mode)

Official brand uses pure `#000000`; for screens, pure black is harsh against light backgrounds at body size. Use the Ink scale for digital typography and dark mode surfaces. Pure `#000` is still correct for print, logo variants, and maximum contrast moments.

| Shade | Hex | Usage |
|---|---|---|
| 50 | `#ECEDEF` | Light gray backgrounds |
| 100 | `#D5D6D8` | Subtle borders |
| 200 | `#ADB0B2` | Muted text |
| 300 | `#7E8387` | Secondary text, placeholders |
| 400 | `#484F54` | Body text secondary |
| **500** | **`#141D24`** | **Body text primary, dark mode base** |
| 600 | `#11191F` | Darker surfaces |
| 700 | `#0E1419` | Dark card backgrounds |
| 800 | `#0A0F12` | Deepest dark |
| 900 | `#06090B` | Near-black |

### Semantic Colors

| Role | Hex | Source |
|---|---|---|
| Success | `#98E086` (accent-500) | Brand core anchor |
| Warning | `#F59E0B` | Extension (standard amber) |
| Error | `#FF6B55` (cta-500) | Extension (coral) |
| Info | `#3B82F6` | Extension (standard blue) |

---

## Typography

### Font Stack

| Role | Font | Fallback | Weights |
|---|---|---|---|
| **Brand / Display** | Baloo 2 (official) | system-ui, sans-serif | 500, 600, 700, 800 |
| **UI / Data** | Manrope *(extension)* | system-ui, sans-serif | 400, 500, 600, 700 |
| **Monospace / Data** | JetBrains Mono | monospace | 400, 500 |

**When to use which:**

- **Baloo 2** — all brand-facing surfaces: landing pages, hero sections, marketing headlines, CTAs, logo-adjacent typography, print materials, social graphics. This is the voice of the brand.
- **Manrope** — dense UI only: dashboards, data tables, form fields, long admin labels, playbook grids where Baloo 2's roundness hurts readability at small sizes. Same neutral letterforms; pairs cleanly without fighting Baloo 2.
- **JetBrains Mono** — numeric data, code, API responses, anything monospaced.

**Rule of thumb:** if a user would read it to feel Manna, use Baloo 2. If a user would read it to get work done fast, Manrope is acceptable. When in doubt, default to Baloo 2.

### Google Fonts Import

```html
<link
  href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@500;600;700;800&family=Manrope:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap"
  rel="stylesheet"
/>
```

### Type Scale (1.25 ratio)

| Size | Name | Usage |
|---|---|---|
| 11px | Micro | Labels, badges, legal text |
| 13px | Small | Secondary text, table cells, card descriptions |
| 16px | Base | Body text, form inputs, list items |
| 20px | Medium | Card titles, section labels |
| 24px | Large | Section headings |
| 30px | XL | Page titles, hero subtitles |
| 36px | 2XL | Hero numbers ($2,138, 212%) |
| 48px | Display | Hero headline, brand name |

### Type Rules

- **Headlines (Baloo 2):** weight 700-800, letter-spacing -0.01em, leading 1.2
- **Body (Baloo 2 or Manrope):** weight 400-500, leading 1.6, max-width 65ch
- **Numbers/Stats (Baloo 2):** weight 800, letter-spacing -0.02em
- **Labels (Manrope):** weight 600-700, uppercase, letter-spacing 0.06em, 10-11px
- **CTAs/Buttons (Baloo 2):** weight 600-700, 14-16px

---

## Spacing Scale

| Token | Value | Usage |
|---|---|---|
| xs | 4px | Icon gaps, tight inline spacing |
| sm | 8px | Compact list items, tag padding |
| md | 12px | Form field gaps, card internal |
| base | 16px | Standard card padding, button padding |
| lg | 24px | Section gaps within cards |
| xl | 32px | Between cards/components |
| 2xl | 48px | Between page sections |
| 3xl | 64px | Page margins, hero spacing |

---

## Border Radius

| Token | Value | Usage |
|---|---|---|
| sm | 6px | Tags, badges, small buttons |
| md | 10px | Input fields, inner cards |
| lg | 14px | Cards, modals |
| xl | 18px | Hero cards, featured sections |
| full | 9999px | Pills, avatars, circular buttons |

Radius scale echoes Baloo 2's rounded character — don't go sharp-cornered (0-2px) except in data tables where it clashes.

---

## Shadows

| Token | Value | Usage |
|---|---|---|
| sm | `0 1px 3px rgba(20,29,36,0.08)` | Cards at rest |
| md | `0 4px 12px rgba(20,29,36,0.10)` | Cards on hover, dropdowns |
| lg | `0 8px 24px rgba(20,29,36,0.12)` | Modals, featured cards |
| glow | `0 0 20px rgba(46,75,70,0.20)` | Primary accent glow (uses forest) |

---

## Component Patterns

### Buttons

| Variant | Background | Text | Border | Usage |
|---|---|---|---|---|
| Primary | Primary-500 (Forest) | White | None | Main actions (Buy, Submit) |
| Accent | Accent-500 (Mint) | Primary-700 | None | Brand-forward secondary CTAs |
| CTA | CTA-500 (Coral) | White | None | Urgent conversion (Get Started, Buy Now) |
| Secondary | Transparent | Primary-500 | Primary-200 | Secondary actions |
| Ghost | Transparent | Primary-500 | None | Tertiary, navigation |
| Dark | Ink-500 | White | None | On colored backgrounds |

**Button specs:** height 40px (sm: 36px, lg: 48px), padding 16px-24px horizontal, radius-md (10px), font Baloo 2 weight 600.

### Cards

| Context | Background | Border | Shadow | Radius |
|---|---|---|---|---|
| Light theme | White | Primary-200 1px | shadow-sm | radius-xl (18px) |
| Dark theme | Ink-700 | rgba(255,255,255,0.06) | none | radius-xl (18px) |
| Featured | White | Primary-500 1.5px | shadow-md | radius-xl (18px) |
| Warning | CTA-50 | CTA-500 1.5px | none | radius-xl (18px) |
| Success | Accent-50 | Accent-500 1.5px | none | radius-xl (18px) |

### Data Rows (inside cards)

Alternate row backgrounds:

- Odd: transparent
- Even: Primary-50 (`#EEF2F1`) on light, rgba(255,255,255,0.03) on dark

### Tags / Badges

| Variant | Background | Text | Usage |
|---|---|---|---|
| Green | Accent-100 | Accent-700 | Win, advantage, positive |
| Red | CTA-100 | CTA-700 | Threat, competitor, negative |
| Yellow | Warning bg | Warning text | Medium, tie, caution |
| Blue | Info bg | Info text | Neutral information |
| Forest | Primary-100 | Primary-700 | Brand, feature |
| Coffee | Warm-100 | Warm-700 | Premium, craft, quality |

---

## Brand Voice

**Full guide:** `docs/tone-of-voice.md`

### Pillars

- **Direct** — lead with numbers: "$800-1,200/month profit" not "significant returns"
- **Warm** — human first: "Coffee, Love & Robots" not "disrupting the coffee industry"
- **Honest** — real margins, real timelines. Say 50-80% ROI, not 212%.
- **Confident** — "Manna delivers barista quality" not "we're the best"
- **Empowering** — "Your kiosk, your business, your profit"

### Say / Don't Say

| Say | Don't Say |
|---|---|
| Smart kiosk, coffee bar | Vending machine |
| Bean-to-cup, barista-quality | Premium, gourmet |
| Partner, licensee | Franchisee, customer |
| Plug & play, $3.75 espresso | Easy, affordable, cheap |
| License, $100/mo flat | Franchise fee |

---

## Animation

| Token | Value | Usage |
|---|---|---|
| ease-out | `cubic-bezier(0.23, 1, 0.32, 1)` | Elements entering, hover feedback |
| ease-in-out | `cubic-bezier(0.77, 0, 0.175, 1)` | Moving elements |
| duration-fast | 150ms | Hover, tooltip |
| duration-normal | 200ms | Dropdown, toggle |
| duration-slow | 300ms | Modal, panel |

### Rules

- Never `transition: all` — specify properties
- Never `ease-in` for UI — use ease-out
- UI animations under 300ms
- Respect `prefers-reduced-motion`

---

## Dark Theme Tokens

| Token | Light Value | Dark Value |
|---|---|---|
| Background | `#FFFFFF` | `#0F1419` |
| Surface | `#FFFFFF` | `#1A1F2E` |
| Surface hover | `#EEF2F1` | `#232838` |
| Text primary | `#141D24` | `#E8E8E8` |
| Text secondary | `#7E8387` | `rgba(255,255,255,0.6)` |
| Text muted | `#ADB0B2` | `rgba(255,255,255,0.4)` |
| Border | `#B2C4C0` | `rgba(255,255,255,0.06)` |
| Card | `#FFFFFF` | `#1A1F2E` |

---

## Legacy Artifact Note

HTML materials created before 2026-04-14 (`Manna-Coffee-Battlecard.html`, `Operator-Sales-Playbook.html`, `Manna-vs-Crane-Playbook.html`, investment overview, competitors report) use the pre-official palette: `#3D7A6E` teal + `#7BD96B` mid-green + Space Grotesk headlines. They are not broken — just off-brand. Realign opportunistically when touching them for other reasons; do not bulk-rewrite.

---

_Last updated 2026-04-14. Brand Core anchors provided by CEO's designer (CorelDRAW master files in `brand-assets/logo-pdf/`). Digital System extends the core for web/dashboards/dense UI._
_"Coffee, Love & Robots"_
