# Predictive Maintenance — EDA & Classification
## AI4I 2020 Manufacturing Dataset

## Overview
This project explores and models the AI4I 2020 Predictive Maintenance 
Dataset from UCI Machine Learning Repository, covering the full 
data science pipeline from exploratory analysis to model deployment.

## Notebooks
1. **EDA** — Exploratory Data Analysis, statistical testing, and 
   visualisation of failure patterns
2. **Classification** — Logistic Regression, Random Forest and XGBoost 
   models to predict machine failure, with threshold tuning and 
   cross-validation

## Key Findings
- Dataset contains 10,000 records with 3.39% failure rate
- Heat Dissipation Failure (HDF) is the most common failure type
- Torque and Rotational Speed are the strongest predictors of failure,
  confirmed independently by both Random Forest and XGBoost
- Random Forest (threshold=0.3) achieves the best overall performance: 
  Recall=0.750, Precision=0.823, F1=0.785
- Threshold tuning is model-specific — optimal threshold differs 
  significantly between models (0.3 for RF vs 0.859 for XGBoost)

## Models Compared
| Model | F1 (CV) | Recall (tuned) | Precision (tuned) |
|-------|---------|----------------|-------------------|
| Logistic Regression | 0.235 | 0.824 | 0.139 |
| Random Forest | 0.652 | 0.750 | 0.823 |
| XGBoost | 0.623 | 0.750 | 0.761 |

## Tools Used
- Python, Pandas, NumPy, Scikit-learn, XGBoost
- Matplotlib, Seaborn

## Dataset
[AI4I 2020 Predictive Maintenance Dataset](https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset)

## Next Steps
- Apply SMOTE for class imbalance
- Feature engineering (Torque × Rotational Speed interaction)
- Hyperparameter tuning (GridSearchCV)
- Deploy model as REST API (FastAPI)
