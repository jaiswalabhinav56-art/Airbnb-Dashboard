# Global Airbnb Performance Dashboard

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/6/69/Airbnb_Logo_Bélo.svg" width="100" alt="Airbnb Logo"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Tool-Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"/>
  <img src="https://img.shields.io/badge/Listings-2,79,712-FF5A5F?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Cities-10-00A699?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Reviews-5.3M-484848?style=for-the-badge"/>
</p>

---

##  Project Overview

An end-to-end Power BI analysis of **2,79,712 Airbnb listings** and **5.3 million reviews** spanning **10 global cities** across 4 continents. The dashboard tracks Airbnb's platform evolution from its launch in 2008 through the COVID-19 disruption, and surfaces insights on pricing, market concentration, guest satisfaction, host trust, and booking seasonality.

**Cities covered:** Paris · New York · Sydney · Rome · Rio de Janeiro · Istanbul · Mexico City · Bangkok · Cape Town · Hong Kong


---

##  Key Metrics at a Glance

| Metric | Value |
|---|---|
|  Total Listings | **2,79,712** |
|  Cities | **10** |
|  Property Types | **144** |
|  Total Hosts | **207** (unique host segments tracked) |
|  Average Price | **$609** |
|  Total Reviews | **5,373,143** |
|  Data Range | **2008 – 2021** |

---

## Key Findings & Insights

### 📈 1. Platform Growth Lifecycle — Six Distinct Phases

Airbnb's listing growth followed a textbook product lifecycle curve from 2008 to 2021:

| Phase | Period | What Happened |
|---|---|---|
|  Introduction | 2008–2010 | Slow organic growth, early adopters only |
|  Growth | 2010–2013 | Rapid host acquisition across all room types |
|  Maturity | 2013–2016 | **2015 was the peak year for new listings** |
|  Decline | 2016–2017 | Tightening local regulations dampened growth |
|  Reinvention | 2018–2019 | New growth phase; **2017 was the first full profitable year** |
|  COVID-19 | 2020–2021 | Severe drop across all room types |

> **Insight:** The _Entire Place_ category drove the majority of growth and was also the hardest hit during decline phases, making it the most volatile room type on the platform.

---

### 2. Market Concentration — Three Cities Dominate

The Airbnb market is heavily concentrated in a small number of cities:

- **Paris alone accounts for 23.1%** of all listings — the single largest city on the platform.
- **Paris, New York City, and Sydney together hold 48.4%** of total listings and **48% of all reviews** — nearly half the platform's entire activity.
- The cumulative listing share reaches 76.5% with just the top 5 cities (adding Rome and Rio de Janeiro).

```
Paris         → 23.1%  ████████████
New York      → 36.4%  ██████████████████
Sydney        → 48.4%  ████████████████████████
Rome          → 58.3%  █████████████████████████████
Rio de Jan.   → 67.8%  █████████████████████████████████
...           → 100.0%
```

> **Insight:** Paris's dominance is likely driven by hotel room prices being **twice the Airbnb rate** ($800 vs ~$400), pushing travellers toward Airbnb alternatives more aggressively than in other cities.

---

### 3. Pricing — Room Type Matters More Than City

Average prices by room type across all cities:

| Room Type | Avg Price |
|---|---|
| Hotel Room | **$800** |
| Entire Place | **$673** |
| Shared Room | **$580** |
| Private Room | **$462** |

- **Hotel rooms are 73% more expensive** than private rooms on average.
- **Entire apartments** are the most common listing type at **49.7% of all listings**, followed by private rooms (31.1%).
- City-level median prices vary dramatically — Bangkok and Cape Town have the highest medians (₿1,100 and ₿1,069 in local currency), while Rome and Paris are the most affordable in absolute dollar terms.

> **Insight:** Shared rooms being priced higher than private rooms ($580 vs $462) is counterintuitive and suggests shared room inventory skews toward premium or boutique properties rather than budget options.

---

### 4. Guest Satisfaction — Consistently High Globally

Overall average ratings by city (out of 100):

| Rank | City | Rating |
|---|---|---|
| 🥇 1 | Mexico City | **94.8** |
| 🥈 2 | Rio de Janeiro | **94.6** |
| 🥉 3 | Cape Town | **94.4** |
| 4 | New York | 93.8 |
| 5 | Rome | 93.5 |
| 6 | Sydney | 93.2 |
| 7 | Paris | 93.1 |
| 8 | Bangkok | 93.0 |
| 9 | Istanbul | 91.1 |
| 10 | Hong Kong | 89.7 |

> **Insight:** Mexico City leads on every single rating dimension simultaneously — the only city to do so. Hong Kong and Istanbul consistently score lowest, suggesting either different guest expectations or quality gaps in those markets.

---

---

### 6. Review Behaviour — The One-Time Reviewer Effect

Review patterns reveal a strong single-review concentration:

- **86.2% of all reviewers** wrote only **one review** ever
- **98.8% of reviewers** wrote **3 reviews or less**
- The maximum reviews by a single person was **283** — identified as a data anomaly (a globe-trotter leaving duplicate reviews across Bangkok listings on 13-Oct-2020)

> **Insight:** The review base is overwhelmingly composed of one-time contributors. This means Airbnb's review system is driven by breadth of guests rather than depth of engagement — each listing's rating reflects a wide, non-repeat audience.

---

### 7. Seasonality — European Summer vs Holiday Season

Monthly review share reveals distinct seasonal patterns by city:

- **Paris and Rome dominate review share from April to August**, reflecting peak European summer travel
- **New York spikes in November and December** during the holiday season
- Overall review volume is highest in **October** (552,877 reviews) and lowest in **March** (401,732)

> **Insight:** European cities follow classic summer tourism cycles, while North American cities show winter holiday demand. A host strategy optimised for one market would be suboptimal in the other — pricing and availability should reflect city-specific seasonality.

---

### 8. Host Trust — Strong Verification Compliance

Trust signal breakdown across all 2,79,712 listings:

| Trust Segment | Share |
|---|---|
| Identity Verified + Profile Picture | **71.8%** |
| Not Verified + Has Profile Picture | 27.8% |
| Identity Verified + No Profile Picture | 0.1% |
| Not Verified + No Profile Picture | 0.2% |

> **Insight:** Over **72% of Airbnb hosts are fully verified** with both identity confirmation and a profile photo. Only **0.4% of listings are completely anonymous** (no verification, no photo), meaning the platform has strong trust infrastructure in place. The largest gap is the 27.8% who have a photo but haven't completed identity verification — a potential area for platform-driven nudges.

---

## Data Model

```
Listings (279,712 rows)                Reviews (5,373,143 rows)
─────────────────────────              ────────────────────────
listing_id (PK)          ──────────▶  listing_id (FK)
host_id                               review_id
city                                  date
room_type                             reviewer_id
property_type
price
review_scores_* (6 dims)
host_is_superhost
host_identity_verified
host_has_profile_pic
host_since
```

<p align="center">Built with Power BI · Data sourced from public Airbnb listings (2008–2021)</p>
