# Card Portfolio Risk & Retention Analytics

## Business Problem
Credit card issuers lose revenue when at-risk customers churn undetected. This project identifies leading indicators of customer attrition across a card portfolio and simulates the retained value of a targeted retention campaign — mirroring the kind of portfolio and campaign-ROI analysis a commercial card analytics team runs.

## Data
10,127 credit card customers, 21 features (demographics, product holdings, activity, and transaction behavior). Source: public Kaggle credit card customer dataset. Zero missing values after removing 2 leftover model-output columns.

## Approach
1. **Data prep** — cleaned raw data, removed non-feature columns, verified category integrity (`02_data_prep/`)
2. **Portfolio dashboard (Power BI)** — 3-page report covering:
   - Overview: portfolio KPIs and churn by income/card segment
   - Risk & Leading Indicators: churn by inactivity, product count, and utilization
   - ROI Simulation: interactive what-if model for a targeted retention campaign
3. **Insights & ROI writeup** — full findings and caveats in `04_insights_and_roi/Insights_and_ROI.md`

## Key Findings
- **Inactivity** and **low product count (≤2)** are the strongest, most reliable churn drivers
- A combined at-risk segment (935 customers, 9% of portfolio) churns at **38%** — 2.4x the portfolio baseline
- Targeting this segment with a retention campaign at a 15–20% success rate could retain **$346K–$461K** in annual transaction value
- Weaker/less reliable signals (income, card tier) are called out explicitly, with small-sample caveats flagged rather than overstated

## Tools
Power BI (DAX measures, What-If parameters), Excel (data cleaning), Python/pandas (validation)

## Files
- `01_raw_data/` — original dataset
- `02_data_prep/` — cleaned dataset
- `03_powerbi_dashboard/` — .pbix file
- `04_insights_and_roi/` — full insights writeup
- `05_screenshots/` — dashboard page exports
