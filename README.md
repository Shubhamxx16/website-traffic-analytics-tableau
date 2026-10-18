# Website Traffic & Conversion Analytics (Tableau)

An interactive Tableau story analysing 30,110 website sessions for Swiggy: which traffic sources, campaigns, devices and states drive conversions, where visitors drop off, and what to do about it.

**[View the live dashboard on Tableau Public](https://public.tableau.com/shared/SJ9YST47G?:display_count=n&:origin=viz_share_link)**

![Overview and KPI sheet](tableau/screenshots/01_overview.png)

## Dataset at a glance

| | |
|---|---|
| Records | 10,000 rows (30,110 sessions, 48,410 page views) |
| Period | 16 July 2024 to 14 October 2024 |
| Conversion rate | 41.2% of rows marked Converted |
| Bounce rate | 32.7% of rows marked Bounced |
| Dimensions | Traffic source, campaign, device, browser, OS, state, landing page, exit page, new vs returning, day of week |

## The story: 5 views

1. **Overview:** KPI sheet by traffic source (sessions, conversion rate, bounce rate, session duration, page views) and traffic mix.
2. **Traffic sources:** sessions, conversion, bounce and session duration by source.
3. **User behaviour:** device split, new vs returning visitors, browser mix, device performance and conversion by day of week.
4. **Campaigns and geography:** conversion and sessions by campaign, top states by sessions, and conversion rate by state.
5. **Insights and recommendations:** the findings below, with a recommended action for each traffic source.

| | |
|---|---|
| ![Traffic sources](tableau/screenshots/02_traffic_sources.png) | ![User behaviour](tableau/screenshots/03_user_behaviour.png) |
| ![Campaigns and geography](tableau/screenshots/04_campaigns_and_geography.png) | ![Insights and recommendations](tableau/screenshots/05_insights_and_recommendations.png) |

## Key insights

- **Organic is the backbone.** It drives 49.8% of sessions (15,007), with a 41.3% conversion rate and the lowest bounce rate (32.3%).
- **Maharashtra: high volume, low conversion.** It sends the most sessions (5,246) but converts at 37.6%, 6.5 pp below West Bengal (44.1%).
- **Newsletter beats Product Launch.** Newsletter campaigns convert at 42.0% vs 39.9% for Product Launch.
- **Returning visitors convert slightly better:** 41.7% vs 40.9% for new visitors, though they are only 30.1% of traffic.
- **Tuesday and Friday are the peak days** for conversion (42.3% each); Sunday is the lowest (39.0%).
- **Paid and Referral bounce more:** both at 34.1%, 1.8 pp higher than Organic and Direct.

## Recommendations

| Area | Recommendation |
|---|---|
| Organic | Scale up. Invest in SEO and content, which compound at near-zero marginal cost |
| Direct | Nurture existing visitors |
| Paid and Referral | Fix landing pages to cut the higher bounce rate |
| Maharashtra | Geo-targeted landing page optimisation for its urban audience |
| Campaigns | Shift budget toward informational, value-driven (Newsletter-style) content |
| Returning visitors | Loyalty incentives and re-engagement emails to grow this higher-converting segment |

## How to read these results

Most differences between segments are small, in the range of 1 to 3 percentage points. A simple significance test on this data shows Maharashtra's lower conversion is the clearest signal. The Newsletter vs Product Launch, returning vs new, and Organic vs Paid gaps are within normal variation, so treat those as directional and worth testing rather than proven.

## Data

[`data/website_analytics.csv`](data/website_analytics.csv): 10,000 rows, 15 columns. See the [data dictionary](data/README.md).

### Data quality notes

- The column `Geographic Data - Country` actually contains Indian states and union territories, not countries.
- One row has no geography value.
- 498 rows have `Sessions` = 0 while still showing page views, and 60 rows have `Page Views` = 0. These were left as provided.
- No duplicate rows.

## Tools

Tableau Public

## Repository structure

```
├── data/                 website_analytics.csv + data dictionary
├── tableau/screenshots/  the five story views
└── README.md
```

## About me

**Shubham Meena**: operations professional (petroleum industry) moving into data analytics.  
LinkedIn: _add your URL_ · Email: _add your email_
