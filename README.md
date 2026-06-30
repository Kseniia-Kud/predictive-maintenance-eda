# Predictive Maintenance — EDA & Classification
## AI4I 2020 Manufacturing Dataset

## Overview
This project explores and models the AI4I 2020 Predictive Maintenance 
Dataset from UCI Machine Learning Repository.

## Notebooks
1. **EDA** — Exploratory Data Analysis, statistical testing, and 
   visualisation of failure patterns
2. **Classification** — Logistic Regression vs Random Forest models 
   to predict machine failure, with threshold tuning and cross-validation

## Key Findings
- Dataset contains 10,000 records with 3.39% failure rate
- Heat Dissipation Failure (HDF) is the most common failure type
- Tool Wear and Torque are the strongest predictors of failure
- Random Forest (F1=0.652) significantly outperforms Logistic 
  Regression (F1=0.235) on this imbalanced dataset
- Threshold tuning (0.5 → 0.3) improved Recall from 0.57 to 0.75

## Tools Used
- Python, Pandas, NumPy, Scikit-learn
- Matplotlib, Seaborn

## Dataset
[AI4I 2020 Predictive Maintenance Dataset](https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset)

## Next Steps
- Try XGBoost and Gradient Boosting
- Apply SMOTE for class imbalance
- Feature engineering — Torque × Rotational Speed interaction
