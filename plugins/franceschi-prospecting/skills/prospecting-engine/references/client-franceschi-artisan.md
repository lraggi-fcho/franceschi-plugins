# Client profile — Franceschi Chocolate: artisan and premium chocolate

**Second ICP, defined by Luisina on 2026-10-16.** Shared rules (outreach structure, sender, exclusions, collision sources, record-keeping, drafts-only) live in `client-franceschi.md`, sections 8 to 11. Anything below that conflicts with those shared sections is wrong.

**Status:** partially filled. **UNSET** items come from Luisina. **UNTESTED** items are hypotheses until the first run.

---

## 1. Identity

- **Client:** Franceschi Chocolate. Premium Venezuelan cacao, sold B2B.
- **Product catalogue:** see `client-franceschi.md`, section 1b, for SKUs and approved claims. Relevant products for this ICP: **Signature Line, the premium real chocolate made with real cacao** (chunks and mini bars in Venezuelan Blend and Carenero), cocoa butter, the FCH compound line, and custom development from the gourmet line. **Approach principle (Luisina, 2026-10-16):** learn what the prospect offers and needs first, then match it to our lines. Do not assume what they buy. **Which line to offer depends on what the prospect makes:** a chocolatier making bonbons from real chocolate gets the Signature Line; a chocolatier making bonbons with compound gets the FCH line. Both are valid fits for this ICP.
- **What we sell (confirmed by Luisina, 2026-10-16):** real chocolate and couverture, compound chocolate, cocoa butter and cocoa powder, in all formats, including drops, chips, chunks and wafers.
- **Language:** English. US only.

## 2. The thesis

- **Prospect:** U.S.-based premium chocolate brands, artisan chocolatiers, and boutique confectionery manufacturers. They make handcrafted chocolates, bonbons, truffles, pralines, chocolate bars and gourmet confectionery, and they buy chocolate, couverture, cocoa butter or cocoa powder as production ingredients.
- **Seed look-alikes** (for Apollo similar-company search): Lula's Chocolate, Hakan Chocolatier.
- **Priority:** artisan and premium manufacturers first. Retailers that only resell finished chocolate are excluded.
- **Anti-prospect (looks identical in the data):** chocolate shops and cafés that buy finished bonbons and do not make them; retailers and gift-box resellers; distributors; cacao importers, brokers and traders; other chocolate suppliers (competitors).
- **Product line follows the prospect's ingredient, not the other way round.** Verification must record which ingredient the prospect uses (real chocolate, compound, or both) before choosing the angle.
- **Two sub-segments, both count:**
  1. **Bean-to-bar and craft makers** (make chocolate from cacao beans). Angle: origin and flavor.
  2. **Chocolatiers and confectioners** (make bonbons, truffles, pralines from purchased couverture). Angle: consistency and a reliable ingredient.
- **Why the prospect has the problem (hypothesis, to validate):** a chocolatier's product is only as good as its chocolate, and most buy by spec from a distributor. **Validate on the first batch:** does the buyer's site describe its ingredients or origin, and does that lead to a purchase conversation?

## 3. Entry conditions — pass/fail, zero points

- **Business model:** manufactures its own chocolate or confectionery product. Retail-only, café-only or reseller-only → Tier C.
- **Size:** 1–250 employees. 251–500 caps at Tier B with "REVIEW — size band, confirm production scale".
- **Geography:** US headquarters and US production or commercial base.
- **Other hard gates:** not a cacao, chocolate or cocoa supplier, importer or broker. Not a trade association or trade media. Not THE COFFEE CORP or any related entity (main profile, section 9).

## 4. Source filters — all UNTESTED

```
organization_naics_codes:          ["311351", "311352", "311340"]
q_organization_keyword_tags:       ["artisan chocolate", "handcrafted chocolate", "bean-to-bar", "truffles", "bonbons"]   # tight set; test first
organization_num_employees_ranges: ["1,10", "11,50", "51,200"]
organization_locations:            ["United States"]
person_locations:                  ["United States"]
```

NAICS: 311351 chocolate from cacao beans · 311352 confectionery from purchased chocolate · 311340 non-chocolate confectionery (check whether the company makes any chocolate).

- **Filters that look right and are not (hypotheses):** a bare `chocolate` keyword returns mass-market makers and retailers. `gourmet` returns food shops and gift boxes. NAICS 311352 may return firms that only pack bonbons bought elsewhere; check the site before counting them.
- **Band searches:** the same base search, varying only the employee bands.
- **Known coverage gap:** small artisan makers are thin in Apollo. Supplement with craft chocolate maker directories and chocolate trade association member lists, after checking each list is current.
- **Florida priority band (UNTESTED):** enumerate Miami-area cities explicitly. Drop the keyword gate inside one metro.

## 5. Scoring — PROVISIONAL

| Criterion | Weight | Mapping |
|---|---|---|
| Segment fit (makes chocolate or confectionery in-house) | 35 | bean-to-bar or makes chocolate from beans 35 · chocolatier or confectioner from couverture 30 · confectionery with chocolate 20 · reseller only → excluded |
| Buyer access | 35 | owner, founder or head chocolatier plus an ops or purchasing contact → 35 · one channel → 18 · decision-maker role present, coverage unclear → 8 · none → 0 |
| Category relevance | 15 | keyword tag match (artisan, bean-to-bar, truffles, bonbons) → 15 · adjacent tag → 8 · none → 0 |

**Timing boosts:** +10 active posting for production manager, procurement or head chocolatier (free, via job-title search). +5 headcount growth of 10% or more over 12 months.

**Tiers:** A 75–100 · B 50–74 · C 0–49. Capped at 100.

**Buyer titles** (one per company, the best decision-maker):
`["owner","founder","co-founder","head chocolatier","production manager","procurement manager","purchasing manager","R&D manager","product development manager"]`
Seniorities: `["owner","founder","c_suite","vp","director","manager"]`.

## 6. Engagement shapes

| Shape | Condition | The angle |
|---|---|---|
| **Bean-to-bar** | Makes chocolate from beans | Origin and flavor. Angle text: **UNSET** (needs Luisina's approved line). |
| **Chocolatier** | Makes bonbons, truffles or pralines from purchased chocolate | Consistency and a reliable ingredient. Angle text: **UNSET**. |

**What flips a shape at verification:** a named head chocolatier or production role on the site (the buyer is that person); the company says it buys its chocolate from a named supplier (REVIEW, probably locked to a competitor).

## 7. Verification — what counts as proof

- **Verdicts:** BUYER_CONFIRMED · RESELLER · COMPETITOR · NOT_RELEVANT · UNCLEAR.
- **A qualifying sentence:** on the company's own site, a statement that it makes its own chocolate or confections, in its own words, for example "handmade in our kitchen", "bean-to-bar", "we make our truffles". Quote it with its URL. No quote, no top tier.
- **Where the proof hides:** the About or Our Story page, product pages, the ingredients or "how we make it" page.
- **Cull rate:** **UNMEASURED.** Assume 25%, and over-select by a third.

## 8. Outreach

Shared rules apply (main profile, section 8): sender lraggi@franceschichocolate.com, drafts only, no pricing, no dates, no origin or certification claims that are not in Luisina's approved text. The positioning paragraph and close are **UNSET** and come from the approved Franceschi text.

## 9. Collision and record-keeping

Shared rules apply (main profile, sections 9 and 10). Add the artisan segment to the ledger as its own tab, and check against all Franceschi sequences listed in the main profile.
