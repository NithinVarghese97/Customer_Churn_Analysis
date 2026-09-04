# Training and Testing Sets — Documentation

## Source
Derived from `Dataset_ATS_v2_preprocessed.csv` after data cleaning (duplicate removal,
logical consistency fixes) and categorical encoding.

## Split Method
- **Ratio:** 80% training / 20% testing
- **Method:** `sklearn.model_selection.train_test_split`
- **Stratified on:** `Churn` (ensures both sets have the same churn rate as the full dataset)
- **Random state:** 42 (fixed, for reproducibility)

## Size and Composition

| Set | Rows | Columns | Churn Rate |
|---|---|---|---|
| Full (cleaned) dataset | 6,741 | 12 | 26.6% |
| Training set (`train_set.csv`) | 5,392 | 12 | ~26.6% |
| Testing set (`test_set.csv`) | 1,349 | 12 | ~26.6% |

## Columns

| Column | Description | Type |
|---|---|---|
| gender | 0 = Female, 1 = Male | Encoded binary |
| SeniorCitizen | 0 = No, 1 = Yes | Binary |
| Dependents | 0 = No, 1 = Yes | Encoded binary |
| tenure | Months as a customer (scaled) | Scaled numeric |
| PhoneService | 0 = No, 1 = Yes | Encoded binary |
| MultipleLines | 0 = No, 1 = Yes | Encoded binary |
| InternetService | 0 = DSL, 1 = Fiber optic | Encoded binary |
| MonthlyCharges | Monthly bill amount (scaled) | Scaled numeric |
| Contract_Month-to-month | One-hot indicator | Binary |
| Contract_One year | One-hot indicator | Binary |
| Contract_Two year | One-hot indicator | Binary |
| Churn | 0 = No, 1 = Yes (target variable) | Encoded binary |

## Notes
- `tenure` and `MonthlyCharges` were scaled using `StandardScaler`, fit on the training
  set only and applied to both sets (prevents data leakage).
- Full methodology is documented in `Scaling_Techniques_Documentation.docx` and
  `Data_Preprocessing_Pipeline.ipynb`.
