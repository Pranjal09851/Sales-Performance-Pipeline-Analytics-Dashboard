# Sales-Performance-Pipeline-Analytics-Dashboard

A one-page, interactive Power BI dashboard that helps sales leaders track revenue, win rate, pipeline health and team performance.

## 🎯 Business Questions
- How is revenue performing against target?
- What is the win rate, and how does it vary by region, product and team?
- How healthy is the sales pipeline at each stage?
- Which agents, managers, products and offices perform best?

## 📈 Headline Results
| Metric | Value |
|---|---|
| Total Revenue | ~$10.0M |
| Win Rate | 63.2% |
| Avg Sales Cycle | ~52 days |
| Target Achievement | 101% |
| Top Product | GTX ($7.3M) |
| Top Office | West ($3.6M) |

## 🛠️ Tools
Power BI Desktop · Power Query · DAX · Data Modeling

## 🗂️ Data
CRM Sales Opportunities dataset (Maven Analytics): `sales_pipeline`, `accounts`, `products`, `sales_teams`.
Quarterly revenue targets are **assumed** for demonstration, since the dataset has none.

## 🧱 Data Model
Star schema: `sales_pipeline` is the fact table, with `accounts`, `products`, `sales_teams` and a `Date` table as dimensions. A separate `Targets` table is linked through a DAX measure (`TREATAS`).

## 🧹 Data Cleaning (Power Query)
- Set correct data types for dates and values
- Fixed mismatched product names between tables (e.g. "GTXPro" vs "GTX Pro")
- Removed a repeated header row from `sales_teams`
- Kept open deals (no close date) in the pipeline for funnel analysis

## 📐 Key DAX Measures
Total Revenue · Deals Won · Win Rate % · Avg Deal Size · Avg Sales Cycle (Days) · Revenue Target · Target Achievement % · QoQ Growth % · Agent Rank

## 🖥️ Dashboard Features
- KPI cards: revenue, deals won, win rate, avg deal size, target achievement
- Revenue vs Target by quarter
- Pipeline funnel by deal stage
- Top 10 agents, revenue by product and by office
- Manager performance table
- Slicers (date range, office/manager), metric switcher and a "Clear all slicers" button

## 🔍 Key Insights
- GTX generates about 73% of total revenue ($7.3M of $10.0M).
- West is the highest-revenue office ($3.6M), followed by Central ($3.3M) and East ($3.1M).
- Overall win rate is 63.2%, with an average sales cycle of about 52 days.
- [Add one more finding of your own, e.g. top agent or best quarter]

## 📷 Screenshot
![Dashboard]<img width="1917" height="981" alt="image" src="https://github.com/user-attachments/assets/b7d41341-d76a-43ec-a275-78ea9ae1d692" />


## 🚀 How to Use
1. Download the CRM Sales Opportunities CSVs from Maven Analytics.
2. Open `sales_pipeline_dashboard.pbix` in Power BI Desktop.
3. Update the data source paths to your local folder and refresh.
