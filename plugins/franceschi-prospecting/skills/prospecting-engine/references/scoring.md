# Scoring and the workbook

Stages 2 and 4. Weights and band mappings come from the client profile.

## Entry conditions are pass/fail and worth zero points

The single most important scoring rule. **Points are spent only on what varies inside the pull.** The source filters already guarantee model, size and geography, so paying points for them re-rewards the entry ticket and flattens everything into the top tier.

Measured on the reference pipeline before this was fixed: entry conditions scored 37 of 100, the floor for anything surviving the filters was 73, and **33 of 37 leads came out Tier A.** A lopsided tier distribution means this failure, not a good pull.

## The three-criterion frame

Weights are the profile's; the frame is the engine's.

- **Commercial gap** — the structural reason this company has the problem the client solves. Usually the core qualification and the heaviest weight.
- **Buyer access** — can we reach a decision-maker.
- **Category relevance** — how close to the client's sweet spot. Never a gate.

**Buyer access must never drop a lead.** It is scored *before* enrichment, and enrichment only runs on qualified tiers — so if thin contact data cut the score, the lead would fall below the threshold and never get the enrichment that would have supplied the data. The deduction causes the outcome it claims to measure. Floor it whenever a decision-maker *role* exists and record the missing channel as a data gap. Score it zero only when no decision-maker role exists at all, which is a signal rather than a gap.

**Missing data is a flag, not a deduction.** A thin lead is mid-tier with a named gap — not a guessed top-tier, and not a quiet score cut.

**Cap the final score** after boosts. A 95 with two boosts is a 100, not a 105.

**Never inflate scores to fill a tier.** Zero top-tier leads means the source search needs refining — say so and name the specific filter to change, not "refine the search". A run that legitimately produces no top-tier leads is a correct result.

## Engagement shape

Assign every lead one of the profile's shapes. It drives the outreach and is not optional. **It is provisional until Stage 2b confirms it** — headcount-by-department signals measure public professional-network visibility, not reality.

How badly that can fail: on a parallel market where profile density is low, 709 of 948 companies fell into a single band. That is not a finding about those companies, it is an artifact meaning "we cannot see their team". Treat every shape as a hypothesis to be checked against the company's own site.

## Write-back

Append every **verified** company to the ledger — including ones disqualified at verification, with the reason. They are not leads, but the verification that rejected them was real work and must not be repeated. Measured: a company verified as out-of-profile in the morning, never written down because it was never scored, resurfaced in the afternoon pull to be verified from scratch.

Update existing rows in place rather than duplicating. **The user's own columns are theirs** — outcome, date contacted, notes, re-surface — and are never overwritten.

# Stage 4 — Workbook

Read `/mnt/skills/public/xlsx/SKILL.md` before generating. File name `{client}_prospects_{YYYY-MM-DD}.xlsx`, into the profile's folder.

**Tab 1 — All Leads.** One row per company, tier then score descending. Beyond the obvious columns, these carry the pipeline's judgement and must be present: **Engagement Shape · Sales Headcount (band) · Signal · Data Gaps · Address Grade · Collision Flag · Duplicate Flag · Next Action · Status** (blank, for the user). Tier fills: A green `#C6EFCE`, B yellow `#FFEB9C`, C grey `#D9D9D9`. Bold header, frozen row 1, auto-filter on.

**Tab 2 — This Week.** **Sort by signal before score:** a 70-point company actively hiring for the role we replace outranks an 80-point company with no timing signal, because the first has a closing window. Size to the profile's weekly volume.

**Tab 3 — Summary.** Counts per tier and shape · each timing signal · excluded as already worked · duplicate and collision counts · **verification cull count and rate** · data-gap count · **ledger rows corrected at Stage 0** · which band searches were run · any UNSET config and what it affected · 2–3 specific next-search suggestions naming the filter to change, if top-tier yield was low.

**Never drop a lead.** Every input row appears, disqualified ones included, with the reason. Ledger-excluded companies are the one exception and are counted in Summary. Deliver the updated ledger alongside the workbook — two files, every run. Verify the file opens before delivering.
