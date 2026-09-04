# Exploratory Data Analysis (EDA)

## Summary of Key Findings

1. **Class imbalance:** ~27% churn rate overall — worth factoring into model evaluation
   (e.g. use F1/recall alongside accuracy, consider class weighting).
2. **Tenure is the strongest predictor:** new customers churn far more than long-tenured
   ones (correlation ≈ -0.36). Retention efforts are likely most valuable in a customer's
   first several months.
3. **Monthly charges** show a mild positive relationship with churn — pricier plans churn
   slightly more (correlation ≈ 0.19).
4. **Contract type and internet service** show only modest differences in this dataset —
   month-to-month and DSL customers churn slightly more.
5. **Senior citizens** and customers **without dependents** churn at higher rates.

## Contents
- `EDA_Analysis.ipynb` — full notebook with code and embedded charts
- `01_churn_distribution.png` through `07_churn_senior_dependents.png` — exported charts

These findings feed directly into the Clustering Analysis stage — tenure and monthly
charges look like strong candidate features for K-Means segmentation.
