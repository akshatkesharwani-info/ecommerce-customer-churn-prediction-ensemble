# 🔄 E-commerce Customer Churn Prediction — Ensemble

![Python](https://img.shields.io/badge/Python-3.x-blue) ![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

## Overview
An e-commerce company is losing customers rapidly. This project builds and compares three classifiers — Logistic Regression, Decision Tree and Random Forest — then combines them into a Voting Ensemble to predict churn and identify the top retention levers.

## Dataset
- Telco Customer Churn Dataset — [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

## Tech Stack
Python · Pandas · NumPy · Seaborn · Scikit-learn (Logistic Regression, Decision Tree, Random Forest, Voting Ensemble)

## Approach
1. Analyzed churn rate by contract type, tenure and payment method
2. Cleaned TotalCharges (string → numeric) and encoded all categorical features
3. Trained Logistic Regression, Decision Tree and Random Forest individually
4. Compared all three using 5-fold cross-validation AUC for a reliable comparison
5. Combined all three into a soft-voting `VotingClassifier` ensemble
6. Extracted the top 10 churn drivers via Random Forest feature importance
7. Translated the drivers into concrete retention campaign recommendations

## Key Results & Insights
- **Ensemble model outperforms every individual model by 2–3% AUC**
- Month-to-month contract customers churn at 3x the rate of two-year contract customers
- Customers with under 12 months' tenure are the highest churn-risk group — early experience matters most
- Fiber optic internet customers show surprisingly high churn — likely a service-quality signal worth investigating
- Electronic check payment correlates strongly with churn — customers on auto-pay stay significantly longer

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook ecommerce_churn_ensemble.ipynb
```

## Project Structure
```
ecommerce-customer-churn-prediction-ensemble/
├── notebooks/ecommerce_churn_ensemble.ipynb
├── images/  (model_comparison.png, churn_drivers.png)
├── requirements.txt
└── README.md
```

## Author
Akshat Kesharwani — [LinkedIn](https://linkedin.com/in/akshat-kesharwani-b0452b346) · [Portfolio](https://akshatkesharwani-info.github.io)
