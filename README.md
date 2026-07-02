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
   models to predict machine failure, with threshold tuning, 
   cross-validation and feature engineering

## Key Findings
- Dataset contains 10,000 records with 3.39% failure rate (highly imbalanced)
- Heat Dissipation Failure (HDF) is the most common failure type
- Torque and Rotational Speed are the strongest predictors of failure,
  confirmed independently by both Random Forest and XGBoost
- Feature engineering (Power = Torque × RPM, Temperature difference, 
  High Wear flag) improved CV F1 by 19% — a larger gain than 
  switching algorithms
- Final model: Random Forest + Feature Engineering at threshold=0.3 
  achieves Recall=0.809, Precision=0.859, F1=0.833

## Model Comparison
| Model | Threshold | Recall | Precision | F1 (CV) |
|-------|-----------|--------|-----------|---------|
| Logistic Regression | 0.5 | 0.824 | 0.139 | 0.235 |
| Random Forest | 0.5 | 0.570 | 0.886 | 0.652 |
| XGBoost | 0.859 (tuned) | 0.750 | 0.761 | 0.623 |
| Random Forest (tuned) | 0.3 | 0.750 | 0.823 | 0.652 |
| **RF + Feature Engineering** | **0.3** | **0.809** | **0.859** | **0.778** |

## Tools Used
- Python, Pandas, NumPy, Scikit-learn, XGBoost
- Matplotlib, Seaborn

## Dataset
[AI4I 2020 Predictive Maintenance Dataset](https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset)

## Next Steps
- Apply SMOTE for class imbalance
- Hyperparameter tuning (GridSearchCV)
- Deploy model as REST API (FastAPI)
