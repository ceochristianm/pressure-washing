# Data Layer — Format Spec

> The actuals live here. Update weekly minimum (daily is better during launch).
> Claude computes CAC, close rates, CPJ, AJS, channel ROI, and margin from these files.
> Rule: log SAME-DAY while memory is fresh. A half-filled row beats a perfect memory tomorrow.

## leads.csv — every lead, every source
date,source,name,phone,zip,response_time_min,conversation,quoted_tier,quoted_amount,outcome,booked_date,notes
- source: google_ppc|lsa|gbp|marketplace|yard_sign|door_hanger|door_knock|realtor|meta_ad|referral|other
- outcome: booked|lost_price|lost_ghost|not_qualified|pending

## jobs.csv — every completed job
date,zip,source,services,tier,price,upsell_attempted,upsell_closed,upsell_amount,chem_cost,fuel_cost,other_cost,hours_onsite,payment_method,review_asked,review_received,notes

## ad-spend.csv
date,platform,campaign,spend,impressions,leads,notes

## expenses.csv — everything non-job-variable
date,category,item,amount,payment_source,notes
- category: equipment|insurance|software|marketing|fuel_general|chemicals_bulk|legal|labor|other

## weekly-snapshots/ — one file per week (YYYY-MM-DD.md), 5 minutes
- Cash on hand / Amex balance / days to due date
- Jobs done this week, revenue collected
- Pipeline (booked ahead)
- One sentence: how it actually felt / biggest problem
