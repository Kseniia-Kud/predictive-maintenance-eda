# Predictive Maintenance EDA
## AI4I 2020 Manufacturing Dataset

## Overview
Exploratory Data Analysis of the AI4I 2020 Predictive Maintenance 
Dataset from UCI Machine Learning Repository.

## Key Findings
- Dataset contains 10,000 records with 3.39% failure rate
- Heat Dissipation Failure (HDF) is the most common failure type
- Tool Wear and Torque are the strongest predictors of failure
- Strong negative correlation between Rotational Speed and Torque,
  consistent with the power equation: Power = Torque × RPM

## Tools Used
- Python, Pandas, NumPy
- Matplotlib, Seaborn

## Dataset
[AI4I 2020 Predictive Maintenance Dataset](https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset)

## Next Steps
- Handle class imbalance with SMOTE
- Build classification models: Logistic Regression, Random Forest, XGBoost
- Evaluate with F1-score and Recall
