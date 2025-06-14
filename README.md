# Term-Desposit-Subscription

# Predicting Client Subscription to Term Deposits

This project builds a machine learning model to predict whether a client will subscribe to a term deposit, based on historical data from a Portuguese bank’s direct marketing campaigns. It uses a complete data science workflow from exploratory data analysis (EDA) to model deployment readiness.

---

## Dataset Overview

- **Source:** Direct marketing campaigns (phone calls) of a Portuguese banking institution
- **Total records:** ~41,000
- **Features:** 20 input features + 1 binary target (`y`: `yes` or `no`)
- **No missing values**

---

## Project Steps

### 1. Data Preprocessing
- Checked for missing values
- One-hot encoded categorical variables
- Standardized numerical features (where applicable)

### 2. Exploratory Data Analysis (EDA)
- Distribution analysis for key features like age, duration, and previous outcomes
- Target class imbalance identified (12% “yes” vs 88% “no”)

### 3. Handling Imbalanced Classes
- `class_weight='balanced'` in Logistic Regression
- SMOTE (Synthetic Minority Over-sampling) for balancing classes

### 4. Models Compared
- Logistic Regression (best interpretability & good performance)
- Random Forest
- XGBoost

---

## Model Performance

| Model                | Accuracy | Precision | Recall | F1 Score |
|----------------------|----------|-----------|--------|----------|
| Logistic Regression  | 0.78     | 0.88      | 0.85   | 0.83     |
| Random Forest        | 0.89     | 0.88      | 0.89   | 0.88     |
| XGBoost              | 0.88     | 0.88      | 0.90   | 0.89     |

> Logistic Regression was selected due to its interpretability and strong recall, essential for understanding likelihoods in subscription behavior.

---

## Key Findings

- **Longer call durations** and **previous positive responses** were highly predictive
- **Cellular contacts** performed significantly better than telephone
- **May and August** had lower subscription rates
- Clients with **prior campaign success** are much more likely to subscribe again

---


## Deliverables

- `notebook.ipynb`: End-to-end data science workflow
- `model.pkl`: Saved Logistic Regression model (optional)
- `Client_Subscription_Model_Report.pdf`: PDF for management
- `Client_Subscription_Model_Report.docx`: Word report
