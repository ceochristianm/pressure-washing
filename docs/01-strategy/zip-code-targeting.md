# ZIP Code & Neighborhood Targeting — South Florida

> Purpose: research scaffold for ad geo-targeting + route planning while Christian
> learns the area. V1 below is reasoning-based; it gets REPLACED by actuals from
> data/jobs.csv as real jobs accumulate (own-data heatmap > any research).

## What makes a ZIP ideal for this business
1. Median home value $400K+ (premium pricing tolerance)
2. HOA-heavy communities (violation letters = urgency + door-knock density)
3. Home age 5–20 yrs (algae-prone stucco/tile roofs; brand-new = too clean,
   very old = deferred-maintenance owners)
4. Single-family density (drive time between jobs kills margin)
5. Gate access reality (gated = wealthy but needs COI + resident sponsor;
   non-gated affluent = easiest guerrilla access)

## Starting shortlist (validate against actuals)
| Area | ZIPs (approx) | Notes |
|---|---|---|
| Wellington | 33414 | HOA-dense, equestrian money, big lots |
| Royal Palm Beach | 33411 | Middle-affluent, HOA-heavy, high density = short drives |
| Palm Beach Gardens | 33410, 33418 | Affluent, golf communities, tile roofs everywhere |
| Jupiter | 33458, 33478 | High-value coastal, Abacoa area HOA-dense |
| Boca Raton (west) | 33496, 33498 | Very affluent, far south = drive-time cost |
| West Palm (west burbs) | 33411, 33413 | Home base proximity advantage |

## How to use
- **Google Ads (primary channel, added 2026-07-18):** postal code (ZIP) targeting,
  not radius or county — these areas are scattered clusters, not one contiguous
  blob, so radius targeting sweeps in non-target territory between them and
  county-level is far too broad for a $35–50/day budget. Add the shortlist ZIPs
  directly as location targets, set to **Presence** (not "Presence or interest").
  Start concentrated on 2–3 ZIPs closest to home base for route density — full
  campaign setup detail in `../03-sales-marketing/google-lsa-ppc.md`.
- Meta ads (deferred until creative assets exist): start radius-targeted around
  2–3 shortlist areas, not all — same route-density logic
- Yard signs + door hangers: same 2–3 areas — every channel reinforcing the same turf
- Weekly: log each job's ZIP in data/jobs.csv → monthly, ask Claude which ZIPs
  actually produce the best AJS and close rate → reallocate
