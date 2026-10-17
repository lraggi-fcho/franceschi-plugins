# Outreach — first touch, follow-up, disposition

Stages 3, 3b and 3c. The client profile supplies the locked blocks, the
sender and the cadence; this file supplies the structure and the rules.

# Stage 3 — First touch

## Before drafting: the collision check

**Mandatory. Search sent mail by recipient domain for every company in the batch, against every collision source in the profile.**

Measured: a colleague's system emailed one contact twice before our pipeline emailed him a third time — nine days, one person, two systems, the same service, no coordination.

**Enumerate by domain, never by phrase.** A phrase-based attempt to separate the two systems was contaminated within minutes, because one of our own emails happened to share an opening phrase with theirs. Domain enumeration is the only reliable cut.

On a collision: skip that company and take the next candidate. Do not send anyway because our email is better.

## Sender safety

Send only from the profile's address. **List every other sender reachable by the same tools in the profile and never use them** — in practice that includes other clients' mailboxes connected to the same browser and the data vendor's account default, which applies silently unless overridden.

Strip any CRM BCC that belongs to a retired system before it starts bouncing.

## Address quality — grade every address before sending

| Grade | Source | Use |
|---|---|---|
| Best | Vendor-verified, non-catchall domain | send freely |
| Good | Published on the company's own site or catalog | send, count against a daily cap |
| Weaker than it looks | Vendor-verified on a **catchall** domain | a catchall accepts any address, so "verified" means "will not bounce", not "this mailbox exists" — flag it |
| Never | Pattern-guessed (`firstname.lastname@`) | do not send |

A clean delivery record is a real asset and it compounds. Protect it with a daily cap on ungraded addresses, and **attribute bounces correctly** — the reference pipeline spent a week being cautious about a bounce that belonged to someone else's system entirely.

## The email

Four moving parts and two fixed ones.

1. `Dear {FirstName},`
2. **The observation** — one specific, verified thing about *their* operation, then the gap it implies. Never a generic compliment.
3. **The positioning paragraph** — LOCKED by the profile, verbatim.
4. **The company-specific line** — ONE sentence. "For {Company}, I believe the opportunity is to [one concrete thing tied to what they already have]."
5. **The close** — LOCKED by the profile, verbatim.

Subject line follows the profile's pattern. No attachments, no deck, no pricing.

A length cap set from intuition is usually wrong. The reference pipeline's emails run ~180–200 words because the positioning paragraph earns its length.

**When the model is unconfirmed, ask inside part 2 rather than assuming** — "what I could not tell from the site is whether you…" — and make part 4 conditional on the answer. Inviting a no ("if the answer is no, say so and I will leave it there") makes replying cheap and turns either answer into a qualification.

## Outreach rules

- **Never fabricate.** If the data does not support a personalization, drop it — a generic line beats a wrong one.
- **Re-check every specific claim before it ships**, especially one a subagent found. Measured: a draft claimed a certification where the site said the certification was *"Available"* — available on request, not held. Certifications, tonnages, award counts and product names all need the exact wording, because the reader knows their own operation and one overstatement costs the whole email.
- **Never state a figure the data cannot support.** Headcounts from band searches are bands, not counts.
- **Never assert something favourable on the company's behalf** unless their own site says it. "You don't compete with your customers" is a fabrication if they run house brands.
- **Never promise pricing, terms, commission or timelines.** The user sets those.
- **One person per company.** Best decision-maker only: owner or president > VP sales > director of business development > national account manager. Plant managers and operations directors are the wrong buyer — they do not own the commercial problem. Keep a second name in reserve as the escalation. A competing system that emails four contacts per company collided with our pipeline twice; that is the cost.
- If the engagement shape is unset, go back and score it — do not guess at the writing stage.


# Stage 3b — Follow-up

Cadence comes from the profile. The rules below do not.

## Check the mailbox before writing

Never follow up blind. Read each thread:

- **Human reply** → stop, hand to Stage 3c. Follow-ups are for silence only.
- **Out-of-office naming an alternate** → Stage 3c decides; do not silently email both.
- **Bounce** → stop, downgrade the address grade.
- **Silence** → proceed.

Thread it as a reply so the original is quoted beneath. If a draft tool detaches it from its thread, rebuild it as a proper reply rather than sending a bare "Re:".

## Structure — same job, never the same words

1. **A short opener that signals this is bounded** — "One more note on this and then I will leave you be."
2. **Re-anchor on the single most specific verified thing**, phrased differently from the first email — a different facet, or the same fact from another angle. Then hand them an easy exit: if they already have more qualified conversations than they can work, say so and we stop.
3. **An open invitation**, obeying the profile's prohibitions.

## The no-repeat rule

**No sentence may appear in more than one follow-up, and no follow-up may reuse a sentence from that recipient's own first email.**

This is the one place the locked-block logic inverts. A locked paragraph is right in a *cold* email — each company reads it once. The same block repeated across seven follow-ups is a mail merge, and it reads as one to anyone who forwards it to a colleague or compares notes with a peer. It happened: seven follow-ups sharing three sentences word for word, plus a block already sent to three other companies days earlier. The user caught it, not the protocol.

Before sending a batch, **list the openers, the outs and the closes side by side and check for collisions.** If two match, rewrite one.

The last touch stays shorter than the one before. It should read as closing the loop, not as chasing.


# Stage 3c — Disposition

Every send ends in one of these. Record it and act — an undecided outcome sits parked for days.

| What came back | Action |
|---|---|
| **Reply, interested** | Stop the cadence. Hand to the user immediately — this is their conversation now, not the pipeline's. |
| **Reply, not interested** | Stop. Mark declined, do not re-surface, do not argue. A competing system got exactly one real reply in ~130 emails and it was a polite no; that is a result, not a failure. |
| **Out-of-office naming an alternate** | Do not email both. Ask once, note the alternate. Left unowned, this decision sat for five days. |
| **Bounce** | Stop. Downgrade the address grade and note whether the source was unreliable. |
| **Silence after the last touch** | Mark no response; re-surfacing is the user's call. |
| **Signal a colleague already worked it** | Stop and tell the user. |
