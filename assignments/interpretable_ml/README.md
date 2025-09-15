# Interpretable ML Assignment

This assignment is part of AIPI 590: Emerging Trends in Explainable AI (Fall 2025).  
The goal was to analyze the Telco Customer Churn dataset and compare three different models:

- **Linear Regression** (used only as a baseline; not appropriate for churn since it is binary, R² ≈ 0.272)  
- **Logistic Regression** (best performing, with accuracy ≈ 0.807 and ROC AUC ≈ 0.840)  
- **Generalized Additive Model (GAM)** (slightly lower accuracy with accuracy ≈ 0.790 and ROC AUC ≈ 0.826, but provided valuable non-linear insights)

The main deliverable is the `interpretable_ml.ipynb` notebook, which includes EDA, model assumptions, results, and a discussion of strengths and weaknesses.

Overall, Logistic Regression proved to be the most practical model for deployment because it combines strong predictive accuracy with interpretability through odds ratios. The GAM model complemented this by uncovering important non-linear churn patterns, such as higher risk during the first year of tenure and among customers with higher monthly charges. Linear Regression was included to demonstrate why classification-appropriate models are necessary.

Dataset: [Telco Customer Churn (Kaggle)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
GitHub Repo: [Assignment Folder](https://github.com/ericiortega/aipi590-xai-fall2025/tree/main/assignments/interpretable_ml)
