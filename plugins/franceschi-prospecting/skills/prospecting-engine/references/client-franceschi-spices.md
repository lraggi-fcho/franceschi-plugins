# Client profile — Franceschi Chocolate: spices, seasonings and specialty ingredients

**Fourth ICP, defined by Luisina on 2026-10-16.** Shared rules (outreach structure, sender, drafts only, exclusions, collision sources, record-keeping) live in `client-franceschi.md`, sections 8 to 11. Anything below that conflicts with those shared sections is wrong.

**Override to note:** the main profile excludes distributors. **For this ICP, wholesale and B2B distributors are prospects**, because the ICP asks for "wholesale spice companies" with "B2B distribution and bulk purchasing potential". Retailers that sell only to end consumers stay excluded. Every other exclusion still applies.

**Status:** partially filled. **UNSET** items come from Luisina. **UNTESTED** items are hypotheses until the first run.

---

## 1. Identity

- **Client:** Franceschi Chocolate. Premium Venezuelan cacao, sold B2B, in all formats (see `client-franceschi.md`, sections 1 and 1b).
- **Language:** English. US only.

## 2. The thesis

**Approach principle (Luisina, 2026-10-16):** first learn what the prospect offers and what it needs. Then match that to our lines, using the catalogue as the map. Do not limit the search to what we assume they buy, because they may surprise us. Products are the match at the end, not the starting filter.

- **Prospect:** U.S.-based wholesale spice companies, seasoning manufacturers, and specialty ingredient suppliers. They produce or distribute spices, seasoning blends, baking ingredients and specialty powders, and either already carry cocoa powder or chocolate-based products, or have a portfolio where adding them is a natural fit. Examples of fit: cocoa powder, hot chocolate mixes, chocolate-flavored spice blends, cacao-based preparations.
- **Seed look-alikes** (for Apollo similar-company search): **UNSET.** Luisina has not named any. Ask for two or three names before the first search.
- **Priority:** B2B distribution and bulk-buying potential first. Manufacturers that make their own blends second. End-consumer retailers excluded.
- **Anti-prospect (looks identical in the data):** retailers that sell only to consumers; spice shops and gift-shop brands; cacao importers, brokers and traders; other cocoa or chocolate suppliers (competitors).
- **Why the prospect has the problem (hypothesis, to validate):** a wholesale spice business sells by spec and by price, so a supplier that brings origin, consistency and a range of cocoa and chocolate products can add a line without new suppliers. **Validate on the first batch:** does the buyer's catalogue already include cocoa or chocolate products, and is there a purchasing contact?

## 3. Entry conditions — pass/fail, zero points

- **Business model:** wholesale or B2B distribution of spices, seasonings or specialty ingredients, or manufacturing of them. Consumer-only retailer → Tier C.
- **Size:** 1–250 employees. 251–500 caps at Tier B with "REVIEW — size band, confirm production scale".
- **Geography:** US headquarters and US operations.
- **Other hard gates:** not a cacao, chocolate or cocoa supplier, importer or broker. Not a trade association or trade media. Not THE COFFEE CORP or any related entity (main profile, section 9).

## 4. Source filters — all UNTESTED

```
organization_naics_codes:          ["424490", "424450", "311942", "311941"]
q_organization_keyword_tags:       ["spices wholesale", "seasoning blends", "specialty ingredients", "cocoa powder", "hot chocolate mix"]   # tight set; test first
organization_num_employees_ranges: ["11,50", "51,200", "201,500"]
organization_locations:            ["United States"]
person_locations:                  ["United States"]
```

NAICS: 424490 other grocery and related products wholesalers (spices and seasonings sit here) · 424450 confectionery wholesalers · 311942 spice and extract manufacturing · 311941 sauce and seasoning manufacturing. Verify each code on the first run.

- **Filters that look right and are not (hypotheses):** a bare `spices` keyword returns retail spice shops and gift brands. `cocoa` alone returns importers and cocoa traders, which are the anti-prospect. A 424490 wholesaler may carry no cocoa at all, so the site check decides, not the code.
- **Band searches:** the same base search, varying only the employee bands.
- **Known coverage gap:** small regional spice wholesalers are thin in Apollo. Supplement with specialty food association member lists and foodservice distributor directories, after checking each list is current.
- **Florida priority band (UNTESTED):** enumerate Miami-area cities explicitly. Drop the keyword gate inside one metro.

## 5. Scoring — PROVISIONAL

| Criterion | Weight | Mapping |
|---|---|---|
| Segment fit (B2B distribution or manufacture of spices, seasonings or specialty ingredients) | 35 | already carries cocoa or chocolate products 35 · B2B distributor or manufacturer with a fitting portfolio 25 · consumer-only retailer → excluded |
| Buyer access | 35 | procurement, sourcing or purchasing director plus a founder or product contact → 35 · one channel → 18 · decision-maker role present, coverage unclear → 8 · none → 0 |
| Category relevance | 15 | keyword tag match (spices wholesale, seasoning blends, cocoa powder, hot chocolate mix) → 15 · adjacent tag → 8 · none → 0 |

**Timing boosts:** +10 active posting for purchasing director, procurement or product development manager (free, via job-title search). +5 headcount growth of 10% or more over 12 months.

**Tiers:** A 75–100 · B 50–74 · C 0–49. Capped at 100.

**Buyer titles** (one per company, the best decision-maker):
`["purchasing director","procurement manager","sourcing manager","product development manager","R&D manager","founder","CEO","owner","president"]`
Seniorities: `["owner","founder","c_suite","vp","director","manager"]`.

## 6. Engagement shapes

| Shape | Condition | The angle |
|---|---|---|
| **Wholesale distributor** | Sells spices or ingredients in bulk to other businesses | A range of cocoa and chocolate products that fits their catalogue. Angle text: **UNSET.** |
| **Manufacturer with a fitting portfolio** | Makes blends or powders for other businesses | An ingredient for their blends or hot chocolate mixes. Angle text: **UNSET.** |

**What flips a shape at verification:** the company already sells cocoa or chocolate (it is a competitor or an existing supplier; REVIEW before contact); a named procurement or purchasing role on the site (the buyer is that person).

## 7. Verification — what counts as proof

- **Verdicts:** BUYER_CONFIRMED · RESELLER · COMPETITOR · NOT_RELEVANT · UNCLEAR.
- **A qualifying sentence:** on the company's own site, a statement that it sells to businesses in bulk (wholesale, foodservice, B2B), or that it makes blends or powders for other businesses, in its own words. Quote it with its URL. No quote, no top tier.
- **Record the category:** note whether the company already sells cocoa or chocolate, because that changes the angle.
- **Where the proof hides:** the wholesale or "for business" page, the product catalogue, the About page.
- **Cull rate:** **UNMEASURED.** Assume 25%, and over-select by a third.

## 8. Outreach

Shared rules apply (main profile, section 8): sender lraggi@franceschichocolate.com, drafts only, no pricing, no dates, no origin or certification claims that are not in Luisina's approved text. The positioning paragraph and close are **UNSET** and come from the approved Franceschi text.

## 9. Collision and record-keeping

Shared rules apply (main profile, sections 9 and 10). Add this segment to the ledger as its own tab, and check against all Franceschi sequences listed in the main profile.
