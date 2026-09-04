# Customer Churn Analysis

## Project Overview
This repository contains the Stage 2 deliverables for the Customer Churn Analysis
project, completed as part of the ACS Professional Year Program. Stage 2 covers
data preparation and clustering analysis, laying the groundwork for churn prediction
modelling.

## Repository Structure

```
.
├── Data_Preparation/
│   ├── Preprocessed_Dataset/
│   │   └── Dataset_ATS_v2_preprocessed.csv   # Cleaned & encoded dataset
│   ├── Training_Testing_Sets/
│   │   ├── train_set.csv                     # 80% split, scaled
│   │   ├── test_set.csv                      # 20% split, scaled
│   │   └── README.md                         # Size/composition documentation
│   └── Scaling_Documentation/
│       └── Scaling_Techniques_Documentation.docx
│
└── Clustering_Analysis/
    ├── Optimal_Clusters/                     # Elbow method results & visuals
    ├── Trained_Model/                        # K-Means model + training code
    └── Cluster_Visualisation/                # Labelled cluster plots & insights
```

## Stage 2 Deliverables

### 1. Data Preparation
- Preprocessed dataset with missing data handled and categorical variables encoded
- Data split into training (80%) and testing (20%) sets, stratified on `Churn`
- Feature scaling applied (`StandardScaler`) to numeric features, fit on training
  data only to avoid data leakage
- Full write-up: `Data_Preparation/Scaling_Documentation/Scaling_Techniques_Documentation.docx`

### 2. Clustering Analysis
- Optimal number of clusters identified via the elbow method
- K-Means model trained on the prepared dataset
- Resulting clusters visualised and labelled for interpretation

## Team
- **Data Engineer:** Nithin Varghese — data preparation, preprocessing, EDA
- **Data Scientist:** _[teammate name]_ — clustering analysis
- **Project Manager:** _[teammate name]_ — repository submission, coordination

## How to Reproduce
1. Clone this repository
2. Install dependencies: `pip install pandas numpy scikit-learn matplotlib seaborn`
3. Run `Data_Preprocessing_Pipeline.ipynb` to regenerate the preprocessed dataset
   and train/test splits
4. Run the clustering notebook (see `Clustering_Analysis/`) to reproduce the
   K-Means results
