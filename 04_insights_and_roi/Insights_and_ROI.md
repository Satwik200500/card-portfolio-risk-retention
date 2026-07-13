# Insights & ROI — Card Portfolio Risk & Retention Analytics

## Dataset
10,127 credit card customers, 21 features, 0 missing values. Overall churn (attrition) rate: **16.07%**.

## Key Insights

### 1. Inactivity is the strongest early-warning signal
Churn rises sharply as a customer's inactive months increase — from ~4.5% churn among customers inactive just 1 month, up to ~30% among those inactive 4 months (based on 435 customers, a reliable sample size). This makes `Months_Inactive_12_mon` the single strongest leading indicator in the dataset.
*(Note: the 0-months-inactive bar shows 51.7% churn, but on only 29 customers — too small a sample to treat as a reliable pattern; excluded from headline claims.)*

### 2. Fewer products = higher churn risk
Customers with only 1–2 products churn at 26–28%, roughly double the churn rate of customers with 4+ products (~11–12%). Product depth (cross-sell) is a strong retention lever — this is a classic "share of wallet" signal relevant to GCS's card + non-card business.

### 3. Utilization has a U-shaped relationship with churn
Customers with 0% utilization (inactive spenders, 2,470 customers) churn at 36.2% — the highest of any group. Mid-range utilization (21–80%) is the healthiest zone, with churn as low as 6.4%. Very high utilization (81–100%, 467 customers) churns at 20.3%, likely reflecting financial strain. This means both disengaged and overextended customers are flight risks — a dashboard for GCS should watch both tails, not just one.

### 4. Income and card tier show weaker, less reliable signals
Churn is fairly flat across income bands (13.5–17.3%) — not a strong standalone driver. Card tier shows Platinum at 25% churn, but on a sample of only 20 customers — directionally interesting, not statistically reliable. Blue cardholders (93% of the portfolio, 9,436 customers) sit at a stable ~16.1%, matching the overall baseline.

## ROI Simulation: Targeted Retention Campaign

**At-risk segment definition:** customers inactive 3–4 months AND holding ≤2 products — the two strongest, most reliable churn drivers combined.

- At-risk population: **935 customers** (9.2% of portfolio)
- At-risk churn rate: **37.97%** (355 churned) vs. 16.07% baseline — **2.4x** the overall rate
- Average annual transaction value in this segment: **$6,499**

| Retention improvement | Customers retained | Value retained |
|---|---|---|
| 10% | 35.5 | $230,725 |
| 15% | 53.2 | $346,087 |
| 20% | 71.0 | $461,449 |
| 30% | 106.5 | $692,174 |

**Takeaway:** A retention campaign targeting this 9% slice of the portfolio, even at a modest 15–20% success rate, could retain $346K–$461K in annual transaction value — demonstrating how a narrowly targeted intervention (vs. a broad, unfocused campaign) can concentrate ROI.

## Caveats (worth stating upfront in an interview)
- This is a simulation on historical, single-snapshot data — not a live experiment with a control group, so the ROI figures are illustrative, not causal.
- Small-sample segments (Platinum/Gold card tiers, 0-month-inactive group) are flagged and excluded from headline conclusions.
- Retention improvement % is a scenario input (parameter), not a modeled prediction — a real campaign would need an actual pilot/A-B test to validate response rates.
