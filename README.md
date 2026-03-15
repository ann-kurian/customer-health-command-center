# Customer Success Early-Warning System
### Customer Health Command Center — Interactive Dashboard

![HTML](https://img.shields.io/badge/Built%20with-HTML%20%2F%20JS-1C2B4A)
![Chart.js](https://img.shields.io/badge/Charts-Chart.js-1A7A6E)
![AI](https://img.shields.io/badge/AI-Claude%20API-C4873A)
![Dataset](https://img.shields.io/badge/Data-IBM%20Telco%20Churn%20%28Kaggle%29-blue)
![Status](https://img.shields.io/badge/Status-Live-22C55E)

---

## Overview

A live, interactive Customer Health Command Center that scores 100 B2B SaaS accounts by churn risk — built to demonstrate the kind of operational analytics a Customer Success Strategy & Planning analyst would own.

Accounts are statistically generated from the real IBM Telco Customer Churn dataset (Kaggle, n=7,043) distributions — not hand-picked. The generated churn rate (26.0%) and contract-level rates closely match the Kaggle actuals.

**[→ Launch Live Dashboard](https://ann-kurian.github.io/customer-health-command-center/)**
**[→ Read Case Study](case_study.html)**

---

## Key Findings

- Month-to-month contracts churn at **45.8%** — vs. 15.4% for annual and 0% for two-year
- Accounts with **5+ features** adopted have 2.4× higher health scores
- The **first 6 months** of tenure carry the highest churn risk — a time-to-value problem
- Contract conversion from M-t-M to annual moves churn probability from ~45% to ~11%

---

## Health Scoring Model

| Dimension | Weight | Signal |
|---|---|---|
| Feature Adoption | 30% | Strongest long-term retention predictor |
| NPS Score | 25% | Direct sentiment signal |
| Contract Type | 20% | Multi-year=100 · Annual=65 · Monthly=25 |
| Tenure | 15% | Months active, capped at 48 |
| Support Burden | 10% | Inverted ticket volume |

---

## Dashboard Screens

**Screen 1 — Executive Overview**
KPI cards + 4 Chart.js visualisations: health donut, churn by contract type, tenure vs. spend scatter, ARR-at-risk stacked bar

**Screen 2 — Account Health Table**
Sortable, searchable, filterable table of 100 accounts with health bars, risk badges, and click-to-drill rows

**Screen 3 — 90-Day Renewal Pipeline**
Month-to-month accounts renewing within 90 days, bucketed by risk tier with ARR visibility

**Screen 4 — AI Strategy Engine**
Live Claude API integration — 6 quick-prompt buttons, 12 at-risk account pills, free-text input. System prompt calibrated to the dataset distributions.

---

## Data Engineering

Accounts generated from documented IBM Telco Churn distributions (seed=42, fully reproducible):

| Metric | Generated | Kaggle Actual |
|---|---|---|
| Overall churn rate | 26.0% | 26.5% |
| M-t-M churn | 45.8% | 42.7% |
| One-year churn | 15.4% | 11.3% |
| Two-year churn | 0.0% | 2.8% |
| Avg. monthly charges | $66.63 | $64.76 |

---

## Tools

`HTML` `CSS` `JavaScript` `Chart.js` `Claude API` `IBM Telco Churn (Kaggle)`

---

*Portfolio project by Ann Mary Kurian — MS Marketing Intelligence, University of San Francisco*
