# Tech Stack Overview

> Principle: minimum viable stack pre-revenue; upgrade each piece only when revenue
> or job volume justifies it. Every tool must either speed up lead response,
> capture data, or remove Christian from a repeated task.

## Current stack (pre-launch → Month 1)

| Function | Tool | Monthly cost | Status |
|---|---|---|---|
| Business phone | OpenPhone or Twilio number | ~$15 | to set up |
| Automation | n8n (existing skill) | $0–20 | to set up |
| Lead/job log | Google Sheets → data/*.csv | $0 | to set up |
| Quoting | Google Earth satellite view + 3-tier phone pitch | $0 | process, not tool |
| Payments | Stripe or Square (tap-to-pay on phone) | % per txn | to decide |
| Google Business Profile | GBP | $0 | to create |
| Notifications | Telegram bot (existing infra) | $0 | to wire up |
| AI consultant/analyst | Claude Code + this repo | existing | live |

## Month 2 additions (revenue-gated)
- **CRM: leaning Jobber** (~$39–129/mo) — final decision pending (see 00-status/open-questions.md).
  Decision criteria: webhook/n8n integration quality, quote→invoice→review flow,
  route scheduling. Alternative: Housecall Pro. Anti-goal: paying for CRM seats pre-revenue.
- QuickBooks Online + bank feed (once LLC + business account exist)
- CallRail or OpenPhone analytics for call tracking by source
- Review-request automation (n8n)

## The "most tech-advanced PW company" roadmap (post-traction)
Sequenced AFTER cash flow is real — ambition is the destination, not the week-1 build:
1. Full speed-to-lead V2 (drips, missed-call textback, auto-quote assist)
2. Auto-generated satellite quotes w/ AI-assisted property measurement
3. Claude-powered weekly finance/ops review on live CRM + ads + QBO data
4. ZIP-level demand heatmap from own jobs data (feeds ad geo-targeting)
5. Route optimization once 3+ jobs/day
6. AI phone answering/booking for after-hours calls
7. Customer database reactivation engine (annual rewash campaigns — the recurring
   revenue flywheel that makes this business sellable)
