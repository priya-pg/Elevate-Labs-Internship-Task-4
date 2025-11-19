# Elevate-Labs-Internship-Task-4

## Overview

This task uses the Global_Superstore2 dataset (Apoorva Mahalingappa) to create a multi-page interactive Power BI dashboard for analyzing sales, profit, customer behavior, and product performance.

## Data Preparation

- Converted Order Date from text → Date.
- Created a proper Date Table (Year, Month, Quarter, YearMonth).
- Marked it as the official date table.
- Linked: Date[Date] → Global_Superstore2[Order Date].
- Added a Measures Table to keep all DAX metrics organized.

## Key Measures

- Total Sales
- Total Profit
- Total Orders
- Profit Margin
- Sales PY (previous year)
- YoY Sales Growth
- YoY Formula:

Sales Growth YoY =
VAR CurrYear = SELECTEDVALUE('Date'[Year])
VAR PrevYear = CurrYear - 1
RETURN
DIVIDE([Total Sales] - CALCULATE([Total Sales], 'Date'[Year] = PrevYear),
       CALCULATE([Total Sales], 'Date'[Year] = PrevYear))

## Dashboard Structure (6 Pages)

Each page includes the same 5 KPI cards + navigation menu.

1. Overview

- High-level KPIs with a clean summary layout.

2. Sales Performance

- Sales by Regions
- Sales by Year bar chart

3. Profit & Margins

- Profit vs Discount scatter
- Profitability breakdown

4. Customer Insights

- Top customers
- Customer segments & regions

5. Product Performance

- Category/Subcategory sales
- Top products

6. Forecasting

- Time-series forecast using analytics pane

## Design

Clean, modern UI (inspired by ZoomCharts)

Consistent palette

Smooth navigation

Tooltips added to KPI cards

## Outcome

A clear, structured, and interactive dashboard enabling stakeholders to explore sales trends, profitability, customer behavior, and product performance with ease.
