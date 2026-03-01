# Customer Churn Prediction – End-to-End Machine Learning Project

## Overview

Customer churn is a major challenge for subscription-based businesses. 
This project builds a machine learning model to predict whether a customer will churn based on demographic, service, and billing information.

This is a complete end-to-end binary classification project covering:

- Data preprocessing
- ML pipelines
- Model comparison
- Threshold tuning
- ROC-AUC evaluation
- Feature importance analysis
- Business interpretation

---

## Problem Statement

Predict whether a telecom customer will churn.

Target Variable:
- `Churn` (Yes / No)

Business Objective:
Identify high-risk customers early so the company can take preventive action.

---

## Dataset

The dataset includes:

- Customer demographics
- Service subscriptions
- Account information
- Billing details
- Target variable: Churn

---

## Project Workflow

### 1. Data Cleaning
- Checked data types
- Converted `TotalCharges` to numeric
- Handled missing values
- Inspected class distribution

### 2. Train-Test Split
- Stratified split to preserve churn ratio
- Prevented data leakage

### 3. Preprocessing Pipelines

Used `ColumnTransformer` with:

**Numerical Features**
- Median imputation
- Standard scaling

**Categorical Features**
- One-hot encoding

Pipelines ensure:
- Clean workflow
- No data leakage
- Reproducibility

---

## Models Trained

- Logistic Regression
- Random Forest
- Gradient Boosting

All implemented using Scikit-learn Pipelines.

---

## Evaluation Metrics

- Confusion Matrix
- Accuracy
- Precision
- Recall
- F1 Score
- ROC Curve
- AUC Score

---

## ROC Curve & AUC

AUC Score: **0.84**

Interpretation:

If we randomly select one churned and one non-churned customer,
the model correctly ranks the churned customer higher 84% of the time.

This indicates strong class separation ability.

---

## Threshold Tuning

Instead of using the default threshold (0.5), 
we experimented with lowering it to improve recall.

Reason:

In churn prediction, missing a churner is more costly than contacting a safe customer.

Lowering the threshold improved churn detection at the cost of more false positives.

---

## Feature Importance Insights

Key drivers of churn:

- Month-to-month contracts increase churn probability
- Short tenure customers are more likely to churn
- Higher monthly charges correlate with churn
- Long-term contracts reduce churn risk

---

## Results

Best performing model:
- Logistic Regression

Performance:
- Accuracy ≈ 81%
- AUC = 0.84
- Improved recall after threshold tuning

---

## Business Impact

This model can help:

- Identify at-risk customers
- Design retention campaigns
- Offer targeted discounts
- Improve contract strategies

---

## Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## How to Run

Clone the repository:

```bash
git clone https://github.com/shaikhsanan04/customer-churn-prediction.git
