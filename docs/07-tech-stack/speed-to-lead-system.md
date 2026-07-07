# Speed-to-Lead System — Build Spec

> Status: NOT BUILT. Build before turning on paid ads. Owner: Christian (n8n experience
> from Conversion Consulting transfers directly).
> Goal: every lead gets an instant automated touch + Christian gets notified loudly,
> so the human callback happens in 1–5 minutes.

## Why this is the #1 automation

Speed-to-lead is the single biggest close-rate lever in local services. Calling a form
lead within the first minutes vs. 15+ minutes plausibly doubles close rate. This system
makes fast response the default instead of depending on watching a phone.

## V1 Architecture (build this week — minimal, no CRM dependency)

```
[Meta Lead Form]           [Missed call to biz number]
      │                            │
      ▼                            ▼
[n8n webhook / Meta            [OpenPhone/Twilio
 lead retrieval]                missed-call trigger]
      │                            │
      ├──► 1. INSTANT SMS to lead (within seconds):
      │    "Hi {name}, this is Christian with {Business Name} — just got your
      │    request for a quote on your home. I'm pulling your property up on
      │    satellite right now and will call you in the next few minutes.
      │    What's the best time if I catch you busy?"
      │
      ├──► 2. LOUD notification to Christian: Telegram bot message (existing
      │    Telegram infra) + SMS, containing name/phone/address/source/timestamp
      │
      └──► 3. Log row → Google Sheet `leads` (later: CRM) with source + timestamp
           (response-time tracking starts from this timestamp)
```

## Components & cost

| Piece | Tool | Cost |
|---|---|---|
| Business phone # w/ API + missed-call webhook | OpenPhone (~$15/mo) or Twilio (~$1/mo + usage) | ~$15/mo |
| Automation engine | n8n (existing skill; self-host or cloud) | $0–20/mo |
| Meta lead retrieval | Meta Lead Ads → webhook (or Zapier fallback) | $0 |
| Notification | Telegram bot (already have infra) + SMS | ~$0 |
| Lead log | Google Sheets → export to `data/leads.csv` weekly | $0 |

Total: roughly **$15–35/month.** Fits pre-revenue budget.

## V2 (after CRM decision, ~Month 2)

- CRM (Jobber or chosen alternative) becomes the system of record; n8n syncs both ways
- Auto-quote assist: address → note prompting the satellite-view quote workflow
- No-answer drip: if no booking after first call, automated SMS at +1hr, +1day, +3days
- Review-request automation: job marked complete → SMS with direct Google review link
- Missed-call textback on the business line for ALL callers (not just form leads)

## Response-time KPI (tracked from day 1)

- Timestamp lead-in → timestamp first human call
- Target: median < 5 minutes during working hours
- This metric goes on the KPI dashboard and gets reviewed weekly — if close rate is
  low, response time is the first suspect to check.
