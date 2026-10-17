# Sourcing — credit discipline, Apollo mechanics, filter design

Loaded at Stage 1. The client profile supplies the actual filters; this
file is why they are shaped the way they are.

## Credit discipline

**Confirm the credit cost with the user before any spend, every time** — including mid-run, and including a run they already said "go" to for a different step.

The general shape, which holds across data vendors: **discovery is free or cheap, enrichment is the paid step.** So all filter iteration happens in discovery, and enrichment runs last, only on qualified leads, only for contact detail. **Never enrich to obtain a scoring input**, and never enrich to find out whether a search was any good.

On Apollo specifically:

- `apollo_organizations_lookup` — free. All discovery here.
- `apollo_mixed_people_api_search` — free. Obfuscated last names plus `has_email` / `has_direct_phone` coverage flags. Sources buyer access before any spend, and checks whether a named contact still works there.
- `apollo_mixed_companies_search` — 1 credit per call returning results.
- `apollo_people_bulk_match` and the enrich endpoints — ~1 credit per contact.
- `apollo_organizations_job_postings` — 1 credit per company. Never use it to confirm a hiring signal; the free job-title search gives the same answer.

## The mechanical fact that shapes everything

Free discovery returns **only** id, name, domain, website URL, logo. Not employee count, not headcount by department, not location, not category, not contacts. Each of those is a **filter on the call, not a field on the response.**

So you cannot read a company's sales headcount — you can only ask for companies inside a band and see who comes back. **Criteria are scored from set membership.** Run the same base search once per band and record which sets each company appears in. A company in the base pull appearing in none of the bands is above the top band.

This is not an Apollo quirk to work around. It is the reason the whole pipeline costs almost nothing.

## Apollo traps

1. **`apollo_contacts_bulk_create` is destructive** — it overwrites existing records. Read before you write.
2. **Its `label_names` argument silently does nothing.** Measured: 25 records, all returning `label_ids: []`. Apply labels separately with `apollo_labels_add_entity_ids_to_label_names` — non-destructive, creates missing lists — then verify via `contact_label_ids` and `pagination.total_entries`.
3. **The account default sender may not be your client's address.** Override it explicitly on every send or sequence.
4. **Contact ids are hard to re-find** — a search sorted by update time returns other people's contacts out of an account holding tens of thousands. The bulk_create response carries **two** arrays, created and existing; capture ids at creation time.
5. **An unrecognised department key is accepted by the schema and returns nothing** — which reads as "no companies match" rather than "you typed it wrong".
6. **Set both `person_locations` and `organization_locations`.** They are ANDed but independent; the org filter alone returns employees living anywhere in the world, which wastes credits at enrichment.

**Keep duplicate-skip guards ON.** `contacts_finished_in_other_campaigns` and its siblings are the only free signal that a colleague already worked an account.

## Filter design

- **Industry codes narrow the universe; business-model keywords identify the buyer.** Usually both are required. Codes alone return the anti-prospect.
- **Never gate on product category.** Category keywords select for what a company *sells*; model keywords select for *who they sell it to*. On the reference pipeline, gating on the product returned brand owners — the other side of the transaction. Category is a scoring attribute, never a gate.
- **A tight keyword set beats a wide one.** Adding near-synonyms collapsed precision and pulled in four companies from unrelated industries, because everyone uses those phrases.
- **Include the zero band deliberately.** A minimum of 1 on a headcount filter excludes exactly the companies with the biggest gap — usually the highest-value engagement. If a floor of 1 appears where a floor of 0 belongs, treat it as a regression.
- **Inside a single metro, drop the keyword gate.** The tight set is right nationally, where it holds precision across thousands of companies; inside one metro the pool is small enough to triage by hand, and the gate hides real prospects. Measured: 10 companies with the gate, 56 without, and three verified prospects appeared only in the wider set. The wider pull is mostly noise — verification is what makes that payable.
- **Geography needs an explicit place list.** Region names and county names do not work as filters, and discovery returns no location field, so results cannot be filtered afterwards. Enumerate cities. Some territories are small enough to be fully enumerated — check for an empty page 2 before spending calls on pagination.

## Signal layers

Timing signals are detected by **membership in a free filtered search**, not by a paid lookup. Membership is the boost; nothing further needs confirming. The strongest is usually an open job posting for the role the client would replace — it means the company has diagnosed the problem itself and is about to spend a year's salary and ramp on one hire.

## Coverage gap

Every vendor under-represents small, family-owned, low-web-footprint companies, and tags derive from self-description — a company that does the work without marketing it that way is invisible. Name the supplementary sources in the profile (trade directories, association member lists) rather than pretending the vendor is complete.
