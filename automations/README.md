# Automations

Buildable code lives here: n8n workflow exports (JSON), scripts, configs.

## Build queue (priority order)
1. speed-to-lead-v1/ — Meta lead webhook → instant SMS + Telegram notify + Sheets log
   (spec: docs/07-tech-stack/speed-to-lead-system.md)
2. review-request/ — job complete → SMS with GBP review link
3. weekly-data-sync/ — Sheets → data/*.csv export helper
4. (later) missed-call-textback, no-answer drips, CRM sync

Convention: one folder per automation with the n8n JSON export + a README covering
trigger, flow, credentials needed, and failure behavior.
