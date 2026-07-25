# Reconciliation notes — brand consolidation sync (2026-07-24)

This sync gathered brand material scattered across the product repos
(`forgely-hydrogen` + variants, `forgely-roy`, `forgely-growth`, `ember-ops`) into
this canonical repo. Along the way we found real **drift** between sources. This
file records what conflicted and how it was resolved, so the next person doesn't
re-litigate it.

## Ground truth used

- **Colors / fonts:** the live storefront CSS (`forgely-hydrogen/app/styles/app.css`)
  and the deployed `/brand-guidelines` page (`app/routes/brand-guidelines.tsx`).
- **Copy compliance:** `forgely-growth/config/forbidden_phrases.json` (actively enforced).
- **Company facts:** the CAN-SPAM footer address + storefront identity copy.

## Resolved conflicts

| Item | Stale value found | Canonical (kept) | Where the stale value lives |
|---|---|---|---|
| Brand orange | `#FF6B35` | **`#ff4f00`** | `*/public/brand-guidelines.json`, `*/public/brand-guidelines.html` |
| Charcoal | `#2C2C2C` | **`#121212`** | same JSON/HTML |
| Secondary color | "Deep Blue `#1A3A52`" | **none** — not in live CSS or on the live page | same JSON/HTML |
| Headline font | "Venite Adoremus" (as general brand font) | **Space Grotesk**; Venite Adoremus is the **logo-wordmark-only** font | same JSON/HTML |
| Accent font | "Montserrat" | **none** — not used on live site | same JSON/HTML |

### The stale `brand-guidelines.json` / `.html`

Every Hydrogen checkout (`forgely-hydrogen`, `-c4`, `-c7`, `-f5`) ships a
`public/brand-guidelines.json` (and matching `.html`) describing an **old identity
that never actually shipped** — wrong orange (`#FF6B35`), a phantom "Deep Blue"
secondary, Montserrat, and Venite Adoremus mislabeled as a headline font. The live
`/brand-guidelines` **page** (the `.tsx` route) is correct and does **not** read that
JSON.

**Recommendation (not done in this PR):** delete or regenerate those `brand-guidelines.json`
/ `.html` files from this repo so they stop contradicting the live site. Left out of
this PR because it's a change to the *product* repos, not this one.

## Net-new material pulled in

- **Safety Yellow `#ffd700`** — real accent on the live `/brand-guidelines` page; added to tokens + guide.
- **Venite Adoremus (Chequered Ink)** — licensed logo-wordmark font; documented with license note.
- **Production logo set** — `forgely-logo-color`, `forgely-logo-white`, `forgely-icon-color`, `forgely-icon-white` (from `forgely-hydrogen/public`, refreshed 2026-07-02).
- **Company facts** — founded 2023; manufacturing in Ogden, UT (2675 S Industrial Dr, 84401); retail in Roy, UT.
- **Brand values, messaging pillars, video guidelines** — from the (otherwise-stale) brand-guidelines JSON; these text fields were still accurate.
- **Copy-compliance rules** — from `forgely-growth` (`docs/copy-compliance.md`).
- **Forgely Roy sub-brand** — `#e64600` dark-orange variant, light-mode-first retail site.

## Minor discrepancies flagged, not "fixed"

- **Light Gray:** live page renders `#f5f5f0`; token here is `#f5f5f5`. Kept `#f5f5f5` as
  canonical (it matches the storefront's `--color-light-bg`). Worth a designer's call.
- **Logo naming:** repo previously used `forgely-logo-orange.png`; production uses
  `forgely-logo-color.png`. Both retained (byte-identical); `-color` is now canonical.
