# Interpretable ML Assignment

This assignment is part of AIPI 590: Emerging Trends in Explainable AI (Fall 2025). The goal was to analyze the Telco Customer Churn dataset and compare three different models:

- **Linear Regression** (used as a baseline, not really appropriate for churn since it’s binary)  
- **Logistic Regression** (best performing, with accuracy ≈ 0.804 and ROC AUC ≈ 0.841)  
- **Generalized Additive Model (GAM)** (slightly lower accuracy but provided useful non-linear insights)  

The main deliverable is the `interpretable_ml.ipynb` notebook, which includes EDA, model assumptions, results, and a discussion of strengths/weaknesses.  

Overall, Logistic Regression ended up being the most practical choice for predicting churn, while GAM helped show patterns like higher risk in the first year of tenure and with high monthly charges.  

Dataset: [Telco Customer Churn (Kaggle)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
