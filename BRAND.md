# Forgely Brand Guide

The full identity, voice, and usage reference for Forgely Inc.

---

## 1. Identity

| | |
|---|---|
| **Company** | Forgely Inc. |
| **Tagline** | Premium 3D Printing Filament That Just Works |
| **Secondary tagline** | Advanced materials for the next generation of distributed manufacturing. Engineered in the USA. Printed worldwide. ±0.02mm standard. |
| **Location** | Ships from Utah, USA |
| **Website** | [forgely3d.com](https://forgely3d.com) |

---

## 2. Color system

Dark-mode-first. Charcoal + Orange on White is the canonical pairing.

| Name | Hex | Token | Usage |
|---|---|---|---|
| Charcoal | `#121212` | `--color-charcoal` | Primary dark background, body text |
| White | `#ffffff` | `--color-white` | Light surface, inverse text |
| Brand Orange | `#ff4f00` | `--color-brand-orange` | Primary accent, CTAs, highlights |
| Orange Light | `#fe6e00` | `--color-orange-light` | Hover states, secondary accent |
| Dark Grey | `#262626` | `--color-dark-grey` | Cards, secondary surfaces |
| Mid Grey | `#333333` | `--color-mid-grey` | Secondary text |
| Light Grey | `#e5e5e5` | `--color-light-grey` | Borders, dividers |
| Off White | `#f5f5f5` | `--color-off-white` | Subtle backgrounds |
| Black | `#000000` | `--color-black` | High-contrast elements |

Importable tokens: [`colors/tokens.json`](colors/tokens.json) · [`colors/tokens.css`](colors/tokens.css) · [`colors/tokens.scss`](colors/tokens.scss)

### Gradient

Primary brand gradient (used in logo lockup and key marketing surfaces):

```css
background: linear-gradient(135deg, #ff4f00 0%, #fe6e00 100%);
```

---

## 3. Typography

| Role | Font | Weights | Source |
|---|---|---|---|
| Display / Headings | **Space Grotesk** | 700, 900 | [`fonts/SpaceGrotesk-Variable.ttf`](fonts/SpaceGrotesk-Variable.ttf) |
| Body | **Inter** | 400, 500, 600 | [`fonts/Inter-Variable.ttf`](fonts/Inter-Variable.ttf) |
| Monospace | **Space Mono** | 400 | Google Fonts |

CSS face declarations: [`fonts/fonts.css`](fonts/fonts.css)

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

| File | Variant | When to use |
|---|---|---|
| [`logo/forgely-logo-orange.png`](logo/forgely-logo-orange.png) | Orange gradient lockup | Primary — light backgrounds, marketing |
| [`logo/forgely-logo-white.png`](logo/forgely-logo-white.png) | White monochrome | Dark backgrounds, photo overlays |

### Clear space

Maintain padding equal to the height of the **F** mark on all sides.

### Don'ts

- Don't recolor the logo outside approved variants
- Don't stretch, skew, or rotate
- Don't place the orange gradient on busy backgrounds — use the white monochrome
- Don't drop shadows or strokes

---

## 5. Voice & tone

- **Direct and confident** — "Filament That Just Works"
- **Technical but accessible** — speaks to both makers and engineers
- **American-made pride** without being preachy
- **No fluff** — short, punchy copy preferred

### Avoid

- "industry-leading"
- "world-class"
- "synergy", "ecosystem", and similar corporate jargon
- Hyperbole without a number behind it

### Prefer

- Specific numbers (`±0.02mm`, `$21.99/kg`, `ships in 24h`)
- Active voice
- Sentences that fit on one line

---

## 6. Key value props

1. Ships from Utah — fast domestic shipping
2. Free shipping over $49
3. Fast support from real makers
4. Trusted by print farms
5. ±0.02mm tolerance standard

---

## 7. Target markets

- **Education** — classrooms, makerspaces
- **Engineering** — rapid prototyping
- **Creative** — art, design
- **Manufacturing** — jigs, fixtures, end-use parts
- **Healthcare** — medical models, assistive devices
- **Hobby & makers**

---

## 8. Products

| Product | Status | Price |
|---|---|---|
| PLA | Live | From $21.99/kg |
| PETG | Coming soon | TBD |
| ABS | Coming soon | TBD |
| TPU | Coming soon | TBD |
| Hardware | Bambu printer partnerships | — |

---

## 9. Tech stack

- Headless **Shopify** (React / Hydrogen)
- **Tailwind CSS**
- Hosted on **Shopify Oxygen** CDN
- Built by **Elevation Tech** (Ver 3.1.0-stable_rebuild)

---

## 10. Email / newsletter assets

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

## 11. Social

- TikTok — [@forgely](https://tiktok.com/@forgely)
- Instagram — [@forgely](https://instagram.com/forgely)
- Facebook — Forgely Inc.
