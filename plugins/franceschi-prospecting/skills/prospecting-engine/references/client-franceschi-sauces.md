# Client profile — Franceschi Chocolate: sauces, toppings, syrups and spreads

**Third ICP, defined by Luisina on 2026-10-16.** Shared rules (outreach structure, sender, drafts only, exclusions, collision sources, record-keeping) live in `client-franceschi.md`, sections 8 to 11. Anything below that conflicts with those shared sections is wrong.

**Status:** partially filled. **UNSET** items come from Luisina. **UNTESTED** items are hypotheses until the first run.

---

## 1. Identity

- **Client:** Franceschi Chocolate. Premium Venezuelan cacao, sold B2B, in all formats (see `client-franceschi.md`, section 1 and 1b).
- **Language:** English. US only.

## 2. The thesis

**Approach principle (Luisina, 2026-10-16):** first learn what the prospect offers and what it needs. Then match that to our lines, using the catalogue as the map. Do not limit the search to what we assume they buy, because they may surprise us. Products are the match at the end, not the starting filter.

- **Prospect:** U.S.-based food brands and manufacturers making chocolate fudge, dessert sauces, chocolate syrups, ganache and toppings, and sweet spreads, for ice cream, bakery, desserts and foodservice. Priority goes to companies that **manufacture their own** sauces, toppings or spreads, and that use cocoa powder, chocolate or other cacao ingredients as raw materials.
- **Seed look-alikes** (for Apollo similar-company search): Sunday Night's.
- **Priority:** manufacturers first. Retailers and businesses that only resell finished products are excluded.
- **Co-packed brands count** (same decision as the main profile): a brand that outsources manufacturing is a prospect, scored on the product it sells.
- **Anti-prospect (looks identical in the data):** retailers and gift-shop brands that resell finished sauces; distributors; cacao importers, brokers and traders; other chocolate or cocoa suppliers (competitors); ice cream shops and cafés that buy finished toppings and do not make them.
- **Why the prospect has the problem (hypothesis, to validate):** a sauce or topping is mostly its chocolate flavor, and the buyer needs that flavor to be consistent at scale. **Validate on the first batch:** does the buyer's site talk about flavor or its ingredients, and does that lead to a purchase conversation?

## 3. Entry conditions — pass/fail, zero points

- **Business model:** manufactures its own sauce, topping, syrup or spread that contains or could contain cocoa or chocolate. Reseller-only → Tier C.
- **Size:** 1–250 employees. 251–500 caps at Tier B with "REVIEW — size band, confirm production scale".
- **Geography:** US headquarters and US production or commercial base.
- **Other hard gates:** not a cacao, chocolate or cocoa supplier, importer or broker. Not a trade association or trade media. Not THE COFFEE CORP or any related entity (main profile, section 9).

## 4. Source filters — all UNTESTED

```
organization_naics_codes:          ["311941", "311930", "311999", "311520"]
q_organization_keyword_tags:       ["chocolate sauce", "dessert sauce", "chocolate syrup", "fudge", "ganache", "toppings"]   # tight set; test first
organization_num_employees_ranges: ["1,10", "11,50", "51,200"]
organization_locations:            ["United States"]
person_locations:                  ["United States"]
```

NAICS: 311941 sauce and dressing manufacturing · 311930 flavoring syrup and concentrate · 311999 misc. food (spreads, fudge) · 311520 ice cream (when the company makes its own toppings). Verify each code on the first run.

- **Filters that look right and are not (hypotheses):** a bare `chocolate` keyword returns mass-market brands and ice cream shops. `sauce` alone returns many non-chocolate sauce makers, which is the wrong pool. Check the site before counting a company that only lists chocolate as a flavor.
- **Band searches:** the same base search, varying only the employee bands.
- **Known coverage gap:** small topping and syrup makers are thin in Apollo. Supplement with specialty food association member lists and ice cream topping supplier directories, after checking each list is current.
- **Florida priority band (UNTESTED):** enumerate Miami-area cities explicitly. Drop the keyword gate inside one metro.

## 5. Scoring — PROVISIONAL

| Criterion | Weight | Mapping |
|---|---|---|
| Segment fit (manufactures a chocolate-based sauce, topping, syrup or spread) | 35 | chocolate fudge, sauce, syrup or ganache as core product 35 · toppings or spreads with cocoa 28 · sauces or toppings with chocolate as one flavor 18 · reseller only → excluded |
| Buyer access | 35 | founder, CEO or procurement plus production contact → 35 · one channel → 18 · decision-maker role present, coverage unclear → 8 · none → 0 |
| Category relevance | 15 | keyword tag match (chocolate sauce, fudge, ganache, syrup) → 15 · adjacent tag → 8 · none → 0 |

**Timing boosts:** +10 active posting for procurement, sourcing or production manager (free, via job-title search). +5 headcount growth of 10% or more over 12 months.

**Tiers:** A 75–100 · B 50–74 · C 0–49. Capped at 100.

**Buyer titles** (one per company, the best decision-maker):
`["founder","CEO","owner","president","procurement manager","sourcing manager","R&D manager","product development manager","production manager"]`
Seniorities: `["owner","founder","c_suite","vp","director","manager"]`.

## 6. Engagement shapes

| Shape | Condition | The angle |
|---|---|---|
| **Sauce and topping maker** | Makes chocolate sauces, fudge, ganache or syrups | Flavor and consistency at scale. Angle text: **UNSET** (needs Luisina's approved line). |
| **Spread maker** | Makes chocolate spreads or nut-and-cocoa spreads | Cocoa powder or chocolate as a raw material. Angle text: **UNSET**. |

**What flips a shape at verification:** a named buyer or production role on the site (the buyer is that person); a named cacao or chocolate supplier already on the site (REVIEW, probably locked to a competitor).

## 7. Verification — what counts as proof

- **Verdicts:** BUYER_CONFIRMED · RESELLER · COMPETITOR · NOT_RELEVANT · UNCLEAR.
- **A qualifying sentence:** on the company's own site, a statement that it makes a sauce, topping, syrup or spread that contains cocoa or chocolate, in its own words. Quote it with its URL. No quote, no top tier.
- **Record the ingredient:** note whether the company uses real chocolate, compound or cocoa powder, because that decides the Franceschi line to offer (see the main profile, section 1b).
- **Where the proof hides:** the product pages, the ingredients list, About or Our Story, the foodservice or "for business" page.
- **Cull rate:** **UNMEASURED.** Assume 25%, and over-select by a third.

## 8. Outreach

Shared rules apply (main profile, section 8): sender lraggi@franceschichocolate.com, drafts only, no pricing, no dates, no origin or certification claims that are not in Luisina's approved text. The positioning paragraph and close are **UNSET** and come from the approved Franceschi text.

## 9. Collision and record-keeping

Shared rules apply (main profile, sections 9 and 10). Add this segment to the ledger as its own tab, and check against all Franceschi sequences listed in the main profile.
