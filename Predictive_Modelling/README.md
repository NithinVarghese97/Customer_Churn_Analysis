# Predictive Modelling – Customer Churn

## Project Overview

This project focuses on predicting customer churn using machine learning classification models.

The objective is to identify customers who are likely to churn and compare predictive model performance.

## Models Used

Two classification models were developed:

1. Logistic Regression
2. Random Forest

## Model Performance

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 72.94% | 49.37% | **76.54%** | **60.02%** | **81.79%** |
| Random Forest | **75.76%** | **54.34%** | 54.19% | 54.27% | 78.26% |

## Best Model

Logistic Regression was selected as the preferred model because it achieved the highest:

- Recall: **76.54%**
- F1 Score: **60.02%**
- ROC-AUC: **81.79%**

Although Random Forest achieved higher accuracy and precision, Logistic Regression was better at identifying customers who were likely to churn.

## Churn Risk

The predictive model generates customer churn probabilities and categorises customers into:

- Low Risk
- Medium Risk
- High Risk

These predictions can support targeted customer retention strategies.

## Files

- `ATS_Predictive_Modelling_TRUE_WORKING.ipynb` – Complete predictive modelling analysis
- `ATS_customer_churn_predictions.csv` – Customer churn predictions and risk levels
- `README.md` – Project documentation

## Tools

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook / Google Colab
- GitHub

## Conclusion

The project demonstrates how predictive modelling can be used to identify customers at risk of churn and support data-driven customer retention decisions.
