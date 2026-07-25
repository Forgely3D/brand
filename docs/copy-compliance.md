# Copy Compliance — enforced outbound rules

Every outbound draft (cold email, blog, social, B2B prospecting) is grep-checked
against this list **before send/publish**. Violations either get stripped and
re-drafted (strict mode) or routed to Bill for manual review.

> Source of truth for automation: `forgely-growth/config/forbidden_phrases.json`
> (checked by `scripts/common/brand_check.py`). This doc mirrors it for humans —
> if you change one, change both.

## Forbidden phrases — all outbound

`I hope this email finds you well` · `I hope this finds you well` · `I hope you're doing well` ·
`dive into` · `delve` / `delving into` · `in today's fast-paced world` · `in today's digital age` ·
`it's important to note` · `it's worth noting` · `it's worth mentioning` · `at the end of the day` ·
`game-changer` · `synergy` · `leverage synergies` · `best-in-class` · `world-class` ·
`cutting-edge` · `revolutionary`

## Forbidden phrases — cold email (first touch)

`quick question` · `circling back` · `just checking in` · `touching base` ·
`per my last email` · `as per my previous`

## Forbidden phrases — long-form content

`in conclusion` · `to summarize` · `without further ado` · `embark on a journey`

## Off-limits topics (claims we haven't cleared)

| Topic | Triggers | Why |
|---|---|---|
| Biodegradability timeline | biodegradable, breaks down in, compostable in, degrades in | PLA is *industrially* compostable under specific conditions — don't hand-wave timelines |
| Medical / dental use | medical use, medical-grade, surgical, dental implant, orthodontic appliance, biocompatible | Regulatory surface we haven't cleared. Models for dental labs OK; **end-use device claims NOT** |
| Food safety | food safe, food-grade, FDA approved | Forgely has not certified materials as food-safe |
| Pricing promises | locked in for 60/90 days, price guaranteed for 6 months | Raw material (NatureWorks) pricing shifts — **don't promise beyond 30 days** |
| Political | Democrat, Republican, Trump, Biden, election, woke, liberal agenda | No political commentary in any customer-facing content |

## Competitors — never name in outbound

Polymaker · Bambu / Bambu Lab / BambuLab · eSun · Sunlu · Creality · Anycubic

Naming any of these routes the draft to **Bill for manual review**.
**Exception:** "Bambu AMS compatible" is allowed — it's a product-compatibility
reference, not disparagement.

## Blocked internal references (hard block)

`office@flyingcolorsgroup.com` · `flyingcolorsgroup` — never leak into customer-facing copy.

## B2B prospector footer (CAN-SPAM)

Cold B2B emails **must** include, verbatim, in the footer:

- Physical address: `2675 S Industrial Dr` (Ogden, UT 84401)
- An opt-out line containing `won't contact you again`

Example: *"Forgely, 2675 S Industrial Dr, Ogden, UT 84401. Reply UNSUBSCRIBE and we won't contact you again."*

## Style blocks

- No ALL-CAPS words (except brand/technical terms: PLA, STL, FDM, PA)
- No chained exclamation points (`!!`)
- No em-dash used as a Twitter-style pause in customer-facing content
