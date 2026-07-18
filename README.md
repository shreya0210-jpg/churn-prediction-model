# 📊 Customer Churn Prediction Model

A machine learning project built in Python using Jupyter Notebook to analyze customer metrics and predict subscription churn. This project evaluates both linear and tree-based classification models to determine the primary drivers behind customer cancellation.

---

## 📂 Project Overview
Customer churn happens when clients stop doing business with a company. Predicting this behavior allows companies to proactively engage at-risk customers. 

This pipeline explores a synthetic dataset of 100,000 customers, cleans anomalies, handles categorical variable encoding, splits data into training/testing sets, and evaluates model performances.

---

## 📈 Dataset Summary
The data contains **100,000 customer records** with 9 columns tracking behavioral and financial metrics:
*   **Target Variable:** `Churn` (Yes / No)
*   **Numerical Features:** `Age`, `Tenure` (months active), `MonthlyCharges`, `TotalCharges`
*   **Categorical Features:** `Gender`, `Contract` (Month-to-month, One year, Two year), `PaymentMethod`

---

## 🤖 Models & Methodology
The data is preprocessed using **One-Hot Encoding** for categorical labels and evaluated across two primary scikit-learn models:

1. **Logistic Regression:** Used as a baseline linear classifier.
2. **Random Forest Classifier:** Used to evaluate non-linear patterns and extract feature importances.

### Current Base Performance (Logistic Regression)
*   **Overall Accuracy:** 72.3%
*   **Confusion Matrix:**
    *   *True Negatives (Correctly predicted stayed):* 11,364
    *   *True Positives (Correctly predicted churned):* 3,110

---

## 🔍 Key Insights & Feature Importance
According to the Random Forest model, the top 3 critical drivers that influence whether a customer leaves or stays are:

1. **Monthly Charges (~23.6%)** – High individual monthly bills correlate heavily with customer exits.
2. **Tenure (~17.6%)** – The length of time a user has been a customer strongly dictates loyalty.
3. **Total Charges (~17.3%)** – The cumulative spend over the lifetime of the account.

---

## 🛠️ Tech Stack Used
*   **Language:** Python
*   **Environment:** Jupyter Notebook
*   **Libraries:** Pandas, NumPy, Seaborn, Matplotlib, Scikit-Learn
