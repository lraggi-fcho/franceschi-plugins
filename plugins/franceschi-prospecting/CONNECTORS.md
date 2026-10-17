# Connectors

This plugin does not bundle any MCP servers. It uses connectors authenticated through claude.ai, so each person connects them under their own account and permissions.

| Connector | Used for | Required? |
|---|---|---|
| **Apollo.io** | Company discovery, band searches for scoring, contact enrichment | Required |
| **Gmail** | Collision check, reading replies and bounces, drafting and sending | Required |
| **Google Drive** | The prospect ledger (Google Sheet) and the workbook output | Required |

## Before the first run

1. Connect all three at claude.ai → Connectors.
2. Confirm they are enabled in the chat you are working in.
3. Fill in section 8 of `references/client-franceschi.md`: the send-from address, the signature name, and every mailbox that must never send this outreach.
