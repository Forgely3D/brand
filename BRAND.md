# Forgely Brand Guide

The full identity, voice, and usage reference for Forgely Inc.

> Canonical source of truth. When product code (storefronts, email, video) and this
> guide disagree, **this guide wins** — open a PR to fix the drift. See
> [`docs/reconciliation.md`](docs/reconciliation.md) for known drift as of the last sync.

---

## 1. Identity

| | |
|---|---|
| **Company** | Forgely Inc. |
| **Founded** | 2023 |
| **Tagline** | Premium 3D Printing Filament That Just Works |
| **Secondary tagline** | Advanced materials for the next generation of distributed manufacturing. Engineered in the USA. Printed worldwide. ±0.02mm standard. |
| **Manufacturing** | Ogden, Utah, USA — 2675 S Industrial Dr, Ogden, UT 84401 |
| **Retail store** | Roy, Utah, USA ([forgelyroy.com](https://forgelyroy.com)) |
| **Website** | [forgely3d.com](https://forgely3d.com) |

Positioning line: **"Made in Ogden, Utah — not imported."**

---

## 2. Color system

Dark-mode-first. Charcoal + Orange on White is the canonical pairing.

| Name | Hex | Token | Live CSS var | Usage |
|---|---|---|---|---|
| Charcoal | `#121212` | `--color-charcoal` | `--color-charcoal` | Primary dark background, body text |
| White | `#ffffff` | `--color-white` | `--color-off-white` / `--color-accent` | Light surface, inverse text |
| Brand Orange | `#ff4f00` | `--color-brand-orange` | `--color-primary` / `--color-safety` | Primary accent, CTAs, highlights |
| Orange Light | `#fe6e00` | `--color-orange-light` | — | Hover states, secondary accent |
| Safety Yellow | `#ffd700` | `--color-safety-yellow` | — | Highlights, badges, "attention" callouts |
| Dark Grey | `#262626` | `--color-dark-grey` | `--color-muted` | Cards, secondary surfaces |
| Mid Grey | `#333333` | `--color-mid-grey` | `--color-border` | Secondary text, borders (dark) |
| Light Grey | `#e5e5e5` | `--color-light-grey` | `--color-light-muted` | Borders, dividers |
| Off White | `#f5f5f5` | `--color-off-white` | `--color-light-bg` | Subtle backgrounds |
| Black | `#000000` | `--color-black` | `--color-dark` | High-contrast elements |

Importable tokens: [`colors/tokens.json`](colors/tokens.json) · [`colors/tokens.css`](colors/tokens.css) · [`colors/tokens.scss`](colors/tokens.scss)

> **Note:** the live storefront names the same orange twice (`--color-primary` **and**
> `--color-safety`, both `#ff4f00`). Treat them as one brand orange. The storefront's
> "Light Gray" section background renders as `#f5f5f0` on the `/brand-guidelines` page
> — a hair off the `#f5f5f5` token here; the token is canonical (see reconciliation notes).

### Gradient

Primary brand gradient (used in logo lockup and key marketing surfaces):

```css
background: linear-gradient(135deg, #ff4f00 0%, #fe6e00 100%);
```

---

## 3. Typography

| Role | Font | Weights | Source |
|---|---|---|---|
| Logo wordmark **only** | **Venite Adoremus** (Chequered Ink) | Regular | Licensed — see note below |
| Display / Headings | **Space Grotesk** | 500, 700 | [`fonts/SpaceGrotesk-Variable.ttf`](fonts/SpaceGrotesk-Variable.ttf) |
| Body / UI | **Inter** | 400, 500, 600, 700 | [`fonts/Inter-Variable.ttf`](fonts/Inter-Variable.ttf) |
| Technical / Monospace | **Space Mono** | 400, 700 | Google Fonts |

CSS face declarations: [`fonts/fonts.css`](fonts/fonts.css)

> **Venite Adoremus** is reserved for the "Forgely" wordmark in the logo lockup **only** —
> never use it for headlines, body copy, or UI. Forgely holds a single-font commercial
> license from Chequered Ink; **do not redistribute the font file**. For everything else
> use Space Grotesk (display) and Inter (body).

### Type scale (recommended)

| Step | Size | Use |
|---|---|---|
| Display | 56 / 64px | Hero |
| H1 | 40 / 48px | Page titles |
| H2 | 32 / 40px | Section heads |
| H3 | 24 / 32px | Sub heads |
| Body | 16 / 24px | Paragraph |
| Small | 14 / 20px | Caption, meta |

---

## 4. Logo

Current production set (as served by the storefront):

| File | Variant | When to use |
|---|---|---|
| [`logo/forgely-logo-color.png`](logo/forgely-logo-color.png) | Color wordmark (horizontal lockup) | Primary — light backgrounds, marketing |
| [`logo/forgely-logo-white.png`](logo/forgely-logo-white.png) | Reverse/white wordmark | Dark backgrounds, photo overlays, footers |
| [`logo/forgely-icon-color.png`](logo/forgely-icon-color.png) | Color icon / mark | Favicons, avatars, app tiles |
| [`logo/forgely-icon-white.png`](logo/forgely-icon-white.png) | White icon / mark | Dark backgrounds, stamps |

> `logo/forgely-logo-orange.png` is retained as a legacy alias of the color wordmark
> (byte-identical) so existing links keep working. Prefer `forgely-logo-color.png`.

### Clear space

Maintain padding equal to the height of the **F** mark on all sides.

### Don'ts

- Don't recolor the logo outside approved variants
- Don't stretch, skew, or rotate
- Don't place the color/gradient wordmark on busy backgrounds — use the white variant
- Don't drop shadows or strokes
- Don't set the wordmark in any font other than Venite Adoremus; don't combine the mark with another logo into a single lockup

---

## 5. Voice & tone

- **Direct and confident** — "Filament That Just Works"
- **Technical but accessible** — speaks to both makers and engineers
- **American-made pride** without being preachy
- **No fluff** — short, punchy copy preferred

### Avoid

- "industry-leading", "world-class", "best-in-class", "cutting-edge", "revolutionary"
- "synergy", "ecosystem", "game-changer", and similar corporate jargon
- Filler openers ("I hope this email finds you well") and AI-tells ("delve", "dive into", "it's worth noting")
- Hyperbole without a number behind it

### Prefer

- Specific numbers (`±0.02mm`, `$21.99/kg`, `ships in 24h`)
- Active voice
- Sentences that fit on one line

> The full enforced block list (forbidden phrases, off-limits topics, competitor rules,
> and the CAN-SPAM footer requirement) lives in [`docs/copy-compliance.md`](docs/copy-compliance.md)
> and is checked automatically against every outbound draft.

---

## 6. Key value props

1. Ships from Utah — fast domestic shipping
2. Free shipping over $49
3. Fast support from real makers
4. Trusted by print farms
5. ±0.02mm tolerance standard

Messaging pillars and audience framing: [`docs/messaging.md`](docs/messaging.md).

---

## 7. Brand values

Precision Engineering · Made in USA · Quality You Can Trust · Makers First ·
Reliability · Innovation · Transparency

---

## 8. Target markets

- **Education** — classrooms, makerspaces
- **Engineering** — rapid prototyping
- **Creative** — art, design
- **Manufacturing** — jigs, fixtures, end-use parts
- **Healthcare** — medical *models* and assistive devices (see topic limits in `docs/copy-compliance.md`)
- **Hobby & makers**

---

## 9. Products

| Product | Status | Price |
|---|---|---|
| PLA | Live | From $21.99/kg |
| PETG | Coming soon | TBD |
| ABS | Coming soon | TBD |
| TPU | Coming soon | TBD |
| Hardware | Bambu printer partnerships | — |

---

## 10. Sub-brands

### Forgely Roy — retail storefront ([forgelyroy.com](https://forgelyroy.com))

The Roy, Utah physical store site. Same brand family; intentionally lighter and more
retail than the flagship.

- Shares the brand orange `#ff4f00`; adds a darker hover variant **`#e64600`** (`--color-forgely-orange-dark`)
- Light-mode-first (flagship is dark-mode-first)
- Retail-specific UI: in-store pickup badges, store hours, wishlist, quick-add
- Cross-links to `forgely3d.com`

---

## 11. Tech stack

- Headless **Shopify** (React / Hydrogen)
- **Tailwind CSS**
- Hosted on **Shopify Oxygen** CDN
- Built by **Elevation Tech** (Ver 3.1.0-stable_rebuild)

---

## 12. Email / newsletter assets

All hosted at `https://forgely3d.com/assets/newsletter/`.

| Asset | File | Use |
|---|---|---|
| Logo | `logo-forgely.png` | Email header, all campaigns |
| Spool Hero (Blue) | `spool-blue-primary.webp` | Welcome email (Email 1) |
| Spool Detail (Black) | `spool-black-primary.webp` | Material education (Email 2) |
| Spool Social (Red) | `spool-red-primary.webp` | Social proof (Email 3) |
| Spool Offer (Orange) | `spool-orange-primary.webp` | Discount / CTA (Email 4) |

**Format:** WebP, < 300 KB each. **Width:** 600 px (responsive scaling). Always include alt text.

---

## 13. Video / avatar content

Guidance for HeyGen and other on-camera/avatar content lives in
[`docs/video-guidelines.md`](docs/video-guidelines.md).

---

## 14. Social

- TikTok — [@forgely](https://tiktok.com/@forgely)
- Instagram — [@forgely](https://instagram.com/forgely)
- Facebook — Forgely Inc.
