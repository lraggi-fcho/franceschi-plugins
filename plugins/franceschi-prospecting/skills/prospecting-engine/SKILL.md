---
name: prospecting-engine
description: Client-agnostic B2B prospecting protocol driven by a client profile. Use to run or set up a prospecting pipeline — source, score, verify, write first touch and follow-ups, track disposition, build the workbook — and to stand up a profile for a new client or product line. Triggers include "run the pipeline for Franceschi", "prepare the batch", "send the follow-ups", "set up prospecting for {client}", "build a client profile", "who should I work this week".
---

# Prospecting engine

The machinery, with no client in it. Every client fact — ICP, filters, scoring weights, voice, sender, cadence — lives in a **client profile** in `references/`.

The rules below were built and measured on a different book (a contract-manufacturing prospecting pipeline). The numbers are kept as evidence for why each rule exists. They are not Franceschi measurements. **Re-measure on the first Franceschi batch and write the new numbers into the profile.**

**Stages:** 0 reconcile → 1 source → 2 score → 2b verify → 3 first touch → 3b follow-up → 3c disposition → 4 workbook. Each runs standalone.

## Load the client profile first

Ask which profile, then read `references/client-<name>.md`. Currently: `client-franceschi.md`.

**No profile, no run.** If one does not exist, build it from `references/client-template.md` following "Standing up a new client" below. Never substitute another client's values, and never infer an ICP from a company website and proceed on it — a guessed ICP produces a confident wrong list, which is worse than no list.

**UNSET** values are asked for once, at the start of the stage that needs them. On an unattended run, deliver without them and say what was missing.

**LOCKED** blocks ship verbatim. They are locked because they were tested under the client's name; rewording them to sound fresher is how a pipeline is quietly degraded. A LOCKED block that is still UNSET is never invented: the stage that needs it stops and asks for the official text.

## Running

Single rep, one client at a time. Still keep the rules that protect a shared book: one credit pool, one sending domain, one ledger.

## Stage 0 — Reconcile

**The record is the one the sending system holds.** For this profile that is Apollo: sequences, replies and bounces. The ledger is a copy that drifts. Measured on the reference pipeline: the ledger said 7 companies contacted; sent mail said 19.

Check the profile's exclusion rules in Apollo first (replies are permanent). Then search sent mail in Gmail by recipient **domain** as a second check — never by subject or phrase. Fix any row the mailbox contradicts and report how many were wrong. Only then use the ledger as the exclusion list. The profile lists the other outbound campaigns that must be merged into this check (see Collision sources).

Match on a **stable machine id** (Apollo Organization ID), never company name — vendor names are self-descriptions and drift. Rows flagged to re-surface are not excluded. Everything else is excluded and **counted** in the summary, never silently dropped.

## Stage 1 — Source

Read `references/sourcing.md`. The short version:

**Confirm credit cost before any spend, every time** — including mid-run, and including a run already approved for a different step.

**Discovery is free; enrichment is the paid step.** All filter iteration happens in discovery. Enrichment runs last, only on qualified leads, only for contact detail. Never enrich to obtain a scoring input, and never enrich to find out whether a search was any good.

**Free discovery returns only id, name, domain, website URL, logo.** Everything else is a *filter on the call, not a field on the response* — so criteria are scored from **set membership**, by running the same base search once per band.

## Stage 2 — Score

Read `references/scoring.md`.

**Entry conditions are pass/fail and worth zero points.** Points are spent only on what varies inside the pull; the filters already guarantee model, size and geography. Measured before this was fixed on the reference pipeline: entry conditions scored 37 of 100 and 33 of 37 leads came out Tier A. A lopsided tier distribution means this failure, not a good pull.

**Buyer access must never drop a lead** — it is scored before enrichment, so a deduction there causes the outcome it claims to measure.

**Missing data is a flag, not a deduction.** **Never inflate scores to fill a tier** — zero top-tier leads means naming the specific filter to change.

The engagement shape is **provisional until Stage 2b**.

## Stage 2b — Verify

Read `references/verification.md`. Five jobs in one pass, all free: the verdict, harvest published contacts before spending, reconcile the shape, check ownership, check the domain belongs to the company.

**No verbatim quote from the company's own site means no top tier.** Vendor keyword tags are wrong in both directions.

**Budget for the cull: 25%.** To contact 8, select 12.

**Telling someone their business does not buy what they buy is the most damaging error this pipeline can make.** Verification exists to stop it.

## Stage 3 / 3b / 3c — Outreach

Read `references/outreach.md`.

**The collision check is mandatory before drafting** — the ledger, sent mail by domain, and every other outbound campaign listed in the profile.

**Grade every address before sending.** Vendor-verified non-catchall > site-published > vendor-verified on a catchall (which means "will not bounce", not "this mailbox exists") > pattern-guessed, which is never sent.

**Follow-ups: no sentence may appear in more than one, or reuse a sentence from that recipient's first email.**

Every send gets a disposition. An undecided outcome sits parked for days.

## Stage 4 — Workbook

Read `references/scoring.md`, then `/mnt/skills/public/xlsx/SKILL.md`.

## Global invariants

Hold for every client. If a profile contradicts one, the profile is wrong.

- **Entry conditions before points.** A company can score maximum on the core criterion and still be the wrong business model.
- **The mailbox is the record.** Never report a send, delivery or count not verified there.
- **Drafts only, for Franceschi.** The pipeline creates Apollo drafts and nothing else. It never calls send_now, never approves or schedules an email, never enrolls a contact in a sequence (add_contact_ids), and never changes a sequence's status. Luisina reviews each draft in Apollo and sends it herself. Stop and ask if a step appears to require sending.
- **Confirm cost before any spend.**
- **Free before paid, always.**
- **Missing data is a flag, not a deduction.**
- **One company, one row, one person.** Best decision-maker only; warehouse, plant and production managers are the wrong buyer for a commercial offer.
- **Quote, never paraphrase, anything attributed to the prospect.** If the data does not support a personalization, drop it — a generic line beats a wrong one.
- **Never assert something favourable on a company's behalf** unless their own site says it. Never claim a certification, origin or sourcing practice for Franceschi that is not on Franceschi's own approved text.
- **Never state a figure the data cannot support.** Band searches give bands, not counts.
- **A verified negative is worth recording.** Rejecting a company is as valuable as qualifying one and costs the same to repeat.
- **When a measurement contradicts a belief, the measurement wins** — and gets written into the profile with its number.

## Standing up a new client or product line

Copy `references/client-template.md`. Fill in this order; each section constrains the next.

1. **The thesis first.** Who is the buyer, and which look-alike is not. **Settle who buys from whom before anything else** — this decides every filter, weight and email downstream.
2. **Entry conditions**, from the thesis.
3. **Source filters**, tested live and free. Record the filters that *looked* right and were not, with what they actually returned — that list is worth more than the one that works.
4. **Scoring weights.** Do not port another client's numbers without deciding they fit.
5. **Engagement shapes**, if the client has more than one.
6. **Verification proof** — what a qualifying sentence looks like in that vertical, and where it hides.
7. **Outreach blocks.** Use the client's own approved text as the locked paragraphs. Never port another client's positioning paragraph.
8. **Collision sources.** Every other campaign that touches the same accounts, and how to detect them.
9. **Paths, cadence, per-person config.**

Then run a small first batch — three or four companies — and write what you learn back into the profile before scaling.
