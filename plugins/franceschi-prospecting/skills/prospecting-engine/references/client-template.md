# Client profile — {CLIENT NAME}

The prospecting engine reads this file at the start of every run. Everything
client-specific lives here; the engine holds no client facts of its own.

Anything marked **UNSET** must be asked for, never defaulted.
Anything marked **LOCKED** is sent verbatim and may not be reworded.

---

## 1. Identity

- **Client:** {who we are prospecting on behalf of}
- **What they sell:** {the service, in one sentence}
- **Proof cases:** {existing accounts that prove we do this — one line each}
- **Language:** {English / Spanish}
- **Territory:** {country, and any territory that matters}

## 2. The thesis — who is the buyer, who is the anti-buyer

State the distinction that decides whether a company is a prospect. Be
explicit about the look-alike that is NOT a prospect, because that is the
error that wastes whole outreach cycles.

- **Prospect:** {…}
- **Anti-prospect (looks identical in the data):** {…}
- **Why the prospect has the problem we solve:** {the structural reason}

## 3. Entry conditions — pass/fail, worth zero points

- **Business model:** {…}
- **Size:** {employee range}
- **Geography:** {…}
- **Other hard gates:** {…}

## 4. Source filters

```
{the exact working Apollo filter block, or the equivalent for another source}
```

- **Filters that work:** {…}
- **Filters that look right and are not:** {the traps, with what they returned}
- **Band searches that produce scoring inputs:** {…}
- **Known coverage gap and how to supplement it:** {…}

## 5. Scoring

| Criterion | Weight | Mapping |
|---|---|---|
| Commercial gap | {n} | {band table} |
| Buyer access | {n} | {…} |
| Category relevance | {n} | {…} |

**Timing boosts:** {signal → points, and how each is detected for free}

**Tier bands:** A {..}–100 · B {..}–{..} · C 0–{..}

## 6. Engagement shapes

| Shape | Condition | The angle |
|---|---|---|
| {…} | {…} | {…} |

**What flips a shape at verification:** {client-specific tells}

## 7. Verification — what counts as proof

- **Verdicts:** {the allowed set}
- **What a qualifying sentence looks like on a site in this vertical:** {…}
- **Where the proof usually hides:** {…}
- **Observed cull rate:** {n}% — over-select accordingly

## 8. Outreach

- **Send from:** {address}
- **Never send from:** {every other address reachable by the same tools}
- **Signature — LOCKED:**
  ```
  {…}
  ```
- **Subject pattern:** {…}
- **Positioning paragraph — LOCKED, verbatim:**
  > {…}
- **Close — LOCKED, verbatim:**
  > {…}
- **Hard prohibitions:** {e.g. no dates, no durations, no proposed times}
- **Cadence:** {first touch, +n days, +n days, stop}
- **Weekly volume:** {n new companies; select {n} candidates}

## 9. Collision sources

Other people or systems prospecting the same book from the same mailbox or
CRM. Each one must be checked before drafting.

- {system / colleague} — {how to detect their sends}

## 10. Record-keeping

- **Ledger:** {path / filename}
- **Workbook output folder:** {path}
- **CRM:** {live source, static export, or none}
- **Authoritative record:** {normally the mailbox}

## 11. Vertical-specific noise — disqualify on sight

{the recurring false positives in this vertical}
