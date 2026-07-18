# Google PPC + LSA

> UPDATED 2026-07-18: PPC promoted from "deferred to Month 2–3" to **the primary
> launch channel** (paid-first pivot — see decisions-log). LSA is DEFERRED, not
> apply-now — it needs GBP verified + reviews in place first (see below). GBP
> created, verification pending.

## Search Ads (PPC) — PRIMARY LAUNCH CHANNEL

**Budget:** $1,000 initial at **$35–50/day**. Kill criterion: if CPL exceeds ~$120
after ~$400 of post-learning-phase spend, pause and diagnose before continuing.

**Why this leads:** highest-intent traffic in the space, zero creative dependency
(no photo/video library needed — the thing blocking Meta), and it runs on Christian's
strongest skills: PPC, landing pages, ad copy, speed-to-lead, phone closing.

**Realistic expectations (calibrated 2026-07-17, verify against actuals):**
- CPC $6–15 (S. FL metro), blended ~$8–12 with decent Quality Score
- Landing page conversion 8–15% at launch (no reviews yet = trust drag)
- CPL ~$55–100 → 10–18 leads from the first $1,000
- Close 25–40% of real conversations with fast follow-up → **3–7 jobs**
- Break-even CPA per job ≈ $480 — the economics forgive a rough start

**Build requirements before launch:**
- [ ] Landing page: local proof, clear 3-tier offer, click-to-call + short form,
      mobile-first (most searches are mobile)
- [ ] Dedicated OpenPhone number on all ads; UTM-tagged forms (CallRail deferred —
      basic OpenPhone plan + UTMs = ~90% of attribution at $0)
- [ ] Speed-to-lead live: missed-call instant textback + loud notification
      (see `../07-tech-stack/speed-to-lead-system.md`)
- [ ] Tight keyword list (exact/phrase), negative keywords from day 3 —
      block "rental", "repair", "how to", job-seeker and DIY queries
- [ ] Geo: target ZIP shortlist only, not a radius blob

**Discipline rules:**
- Don't judge performance before ~$300–400 spend (new-account learning phase)
- Log every lead in `data/leads.csv` with source=`google_ppc` (or `lsa`/`gbp` as
  appropriate); track response_time_min on every row
- Weekly: CPL, CPJ, close rate by keyword → feed the weekly review

## Local Services Ads (LSA) — DEFERRED (2026-07-18)
- Not being applied for yet. LSA ranking depends heavily on GBP reviews — applying
  before GBP is verified and carrying reviews means launching into a low-rank
  position, which defeats the point of a pay-per-lead placement channel.
- Revisit once GBP is verified and has a real review count (see PPC-generated jobs
  below for how those reviews get built).
- Reference for later: pay-per-lead (calls), "Google Guaranteed" badge. Benchmarks
  to calibrate when the time comes: CPL ~$40–50, close ~50% (high intent).

## Google Business Profile (free — created, verification pending)
- Status 2026-07-17: profile created, awaiting verification. Complete it — cold PPC
  leads WILL Google the business name before calling back; an empty/unverified
  profile is the biggest conversion leak on the ads.
- Category "Pressure washing service"; service area = shortlist ZIPs
- Photos from every job; review link texted on-site at every job
- 10+ reviews = map-pack visibility begins = free lead flow. This compounds — start day 1.