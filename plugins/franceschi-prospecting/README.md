# franceschi-prospecting

The prospecting protocol for Franceschi Chocolate: finding US buyers of premium Venezuelan cacao and writing the first touch and follow-ups.

Adapted from a prospecting pipeline built for another book. The engine is client-agnostic. All Franceschi facts live in one profile: `skills/prospecting-engine/references/client-franceschi.md`.

## Install

1. Cowork → Plugins → Add marketplace → paste this repository's URL (or `owner/repo` on GitHub).
2. Install **franceschi-prospecting** from the list.
3. Connect Apollo, Gmail and Google Drive — see `CONNECTORS.md`.

## Use

- "Run the pipeline for Franceschi"
- "Prepare this week's batch"
- "Send the follow-ups that are due"
- "Set up a client profile for {new product line}"

## Before the first real run

1. **Fill the UNSET items in the profile**, especially the positioning paragraph, the close, the proof cases and the weekly volume. The protocol will not invent Franceschi's approved text.
2. **Merge the three existing Apollo campaigns into the ledger** (see section 9 of the profile). Otherwise the same company can get two sequences.
3. **Run one segment, a small batch of 3–4 companies,** and compare the drafts before scaling. Record each filter's real result in the profile.
4. Bump `version` in `plugin.json` each time you change the plugin, or Cowork will not offer the update.
