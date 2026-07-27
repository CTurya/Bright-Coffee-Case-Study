d# Bright Coffee Shop Sales Analysis — Case Study

## Overview

Bright Coffee Shop's newly appointed CEO set a mandate to grow revenue and improve product performance. This project takes six months of raw transactional data and turns it into concrete, actionable insight in support of that goal.

The dataset covers **149,116 transactions** across **3 New York store locations** (Hell's Kitchen, Astoria, Lower Manhattan) over a 6-month window (Jan–Jun 2023). This project takes that raw data through cleaning, analysis, and dashboarding, and ends with a set of specific recommendations for product mix, promotional timing, and revenue growth.

## How the case study was done

1. **Data cleaning & transformation** — resolved inconsistent `unit_price` formatting (e.g. `'3,1'` → `3.1`), computed `total_amount = unit_price * transaction_qty`, and derived a `transaction_time_bucket` column grouping sales into Morning / Afternoon / Evening windows. Additional fields were derived for transaction hour, day of week, month, and weekday/weekend classification.
2. **Excel analysis** — a fully formula-driven workbook (`SUMIF`/`COUNTIF`, no hardcoded numbers) covering 4 pages: **Dashboard**, **Product Analysis**, **Time Analysis**, and **Store & Trend Analysis** — plus a separate raw-data workbook to keep the dashboard file lightweight and fast to open.
3. **Presentation** — a CEO-facing summary covering product performance, time-of-day and weekly trends, store comparison, revenue growth, and final recommendations.

## What was found

- **Coffee and Tea drive the business**: together they generate **67% of total revenue** ($269,952 and $196,406 respectively) — the clear core of the product mix.
- **Mornings are king**: the 6am–11am window accounts for **55.6% of all revenue**, with **9–10am the single busiest hour** of the day.
- **Revenue more than doubled** over the period, from **$81,678 in January** to **$166,486 in June**.
- **Weekday vs weekend demand is nearly identical** (~$3,874/day vs ~$3,828/day) — sales are consistent across the week rather than weekend-driven.
- **All three stores perform within 3% of each other** ($236,511 / $232,244 / $230,057) — no location is underperforming, so growth initiatives should be rolled out chain-wide rather than store-specific.
- **Barista Espresso, Brewed Chai Tea, and Hot Chocolate** are the top 3 revenue-generating products; **Green Beans, Green Tea, Organic Chocolate, Sugar Free Syrup, and Black Tea** are the lowest performers and are candidates for bundling, promotion, or review.

Full detail, numbers, and the resulting recommendations are in the Dashboard workbook and the final presentation.

## Tools used

- **Microsoft Excel** — formula-driven analysis and native charts
- **Python (pandas)** — data cleaning and transformation (unit price casting, time-bucket derivation, aggregation)
- **PowerPoint** — final stakeholder presentation
- **Miro** — project planning flowchart (data flow & architecture)

## Repository structure

```
Bright_Coffee_Shop_Case_Study/
├── README.md
├── 01_Project_Description_and_Raw_Data/
│   ├── Project_Description.pdf
│   └── raw_data/
│       └── Bright_Coffee_Shop_Raw_Data.xlsx
├── 02_Project_Planning/
│   ├── Bright_Coffee_Gantt_Chart.xlsx
│   └── Miro_Flowchart.md  (+ exported image)
├── 03_Data_Processing/
│   ├── Bright_Coffee_Analysis.sql
│   └── Bright_Coffee_Shop_Dashboard.xlsx
└── 04_Project_Presentation/
    └── Bright_Coffee_Shop_CEO_Presentation.pptx
```

## About

Data analytics case study analyzing Bright Coffee Shop transaction data — Excel, Python, and PowerPoint — with CEO-facing revenue and product performance recommendations.
