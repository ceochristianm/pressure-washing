# KPI Dashboard — Build Spec

> Status: NOT BUILT. Track from job #1. V1 is deliberately low-tech; the discipline
> of logging matters more than the tooling.

## The metrics that matter (in order)

### Survival metrics (weekly, from day 1)
1. **Cash position vs. Amex payback clock** — dollars available vs. balance due and days remaining
2. **Revenue (collected, not booked)**
3. **Total spend** vs. $3,000 ceiling

### Growth metrics (weekly once leads flow)
4. **Leads by source** (Google PPC / LSA / GBP / Marketplace / door hanger / realtor / referral)
5. **Speed-to-lead** — median minutes from lead-in to first human call
6. **Close rate** = booked jobs / real conversations (by source)
7. **Cost per booked job** (paid channels) — the number that decides ad scaling
8. **Average job size** — target $550+; below $450 = upsell system is failing
9. **Upsell attach rate** — % of jobs where test-patch upsell was attempted / closed

### Efficiency metrics (Month 2+)
10. Jobs per day capacity, drive time between jobs, chemical cost per job
11. Review count + GBP ranking position
12. Repeat/referral rate (the long-term database value)

## V1 (now): Google Sheets + Claude Code
- One spreadsheet, 4 tabs mirroring `data/*.csv` (leads, jobs, ad-spend, expenses)
- VA or Christian logs each lead/job same-day (5 min/day max)
- Weekly: export CSVs into `data/`, commit, then ask Claude Code for the weekly review
  (computes everything above, writes analysis to `docs/06-finance/monthly-reviews/`)

## V2 (Month 2, with CRM + revenue)
- Jobber/CRM as source of truth, n8n auto-syncs to Sheets nightly
- Meta Ads + Google Ads spend pulled via API into ad-spend log
- QuickBooks Online connected for true P&L
- Optional: Looker Studio dashboard on top of the Sheets for visual daily glance

## The weekly review ritual (non-negotiable)
Every Sunday or Monday: update data → ask Claude Code:
"Run the weekly review" → output covers the 6 standing questions in CLAUDE.md
(cash clock, revenue vs target, CPL/CPJ by channel, close rate + speed-to-lead,
avg job size, biggest leak + highest-leverage action).
