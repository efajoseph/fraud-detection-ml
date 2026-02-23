# Credit Card Fraud Detection using Machine Learning

## Project Overview

Financial fraud results in significant financial losses and operational risk.  
This project develops and evaluates machine learning models to detect fraudulent credit card transactions in a highly imbalanced dataset.

The goal is to maximise fraud detection (recall) while minimising false positives to reduce customer friction.

## 📊 Dataset

- European credit card transactions dataset
- Highly imbalanced (fraud ≈ 0.17%)
- Features are anonymised PCA components
- Target variable:
  - 0 → Legitimate
  - 1 → Fraud

## Key Challenge

The dataset is severely imbalanced.  
Accuracy is not a reliable metric in this scenario.

A model predicting all transactions as legitimate would still achieve ~99.8% accuracy.

Therefore, evaluation focused on:
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix

## Models Implemented

1. Logistic Regression (Baseline)
2. Logistic Regression with Class Weights
3. Logistic Regression with SMOTE
4. Random Forest Classifier

## Model Comparison (Fraud Class)

| Model | Precision | Recall |
|--------|-----------|--------|
| Logistic Regression | 0.83 | 0.63 |
| Logistic Regression (Class Weight) | 0.06 | 0.92 |
| Logistic Regression (SMOTE) | 0.06 | 0.92 |
| Random Forest | 0.94 | 0.82 |

## Final Model: Random Forest

The Random Forest model provided the best balance:

- 94% Precision
- 82% Recall
- Only 5 false positives
- 18 missed fraud cases

This demonstrates the effectiveness of ensemble tree-based methods in fraud detection systems.

## Additional Techniques Explored

- Class imbalance handling
- SMOTE oversampling
- Probability threshold tuning
- Feature importance analysis

## Business Interpretation

Fraud detection systems must balance:

- Financial loss (false negatives)
- Customer experience disruption (false positives)

This project demonstrates how different modelling strategies impact that trade-off.

## Future Improvements

- Hyperparameter tuning
- Gradient boosting (XGBoost, LightGBM)
- Cost-sensitive learning
- Model deployment via Streamlit

## Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Imbalanced-learn
- Matplotlib / Seaborn

## Author

MSc Artificial Intelligence & Data Science  
Open to Data Analyst / Data Scientist opportunities in the UK
