Based on the content of the provided notebook, here is a comprehensive **README.md** file for your project.

---

# Capstone Project: Mobile Financial Transaction Fraud Detection

This project aims to enhance the accuracy of detecting fraud in mobile financial transactions. By leveraging machine learning, the project seeks to develop a robust model to predict fraudulent transactions with high precision and recall, enabling real-time security improvements and reduction of financial losses.

## Table of Contents

1. [Problem Statement](https://www.google.com/search?q=%23problem-statement)
2. [Dataset Overview](https://www.google.com/search?q=%23dataset-overview)
3. [Project Workflow](https://www.google.com/search?q=%23project-workflow)
4. [Methodology](https://www.google.com/search?q=%23methodology)
5. [Models Evaluated](https://www.google.com/search?q=%23models-evaluated)
6. [Results & Conclusion](https://www.google.com/search?q=%23results--conclusion)

## Problem Statement

The goal is to accurately identify fraudulent transactions in real-time. Key objectives include:

* Analyzing initial patterns and addressing severe class imbalance (approx. 10:1 ratio).
* Identifying key separators between legitimate and fraudulent transactions through extensive EDA.
* Prioritizing **High Recall** for the fraudulent class (Class 1) to minimize financial risks.

## Dataset Overview

The dataset contains **11,142 entries** with the following key features:

* **step:** Unit of time in the system.
* **type:** Transaction type (CASH_IN, CASH_OUT, DEBIT, PAYMENT, TRANSFER).
* **amount:** Transaction amount in local currency.
* **oldbalanceOrg / newbalanceOrig:** Originator's balance before and after the transaction.
* **oldbalanceDest / newbalanceDest:** Recipient's balance before and after the transaction.
* **isFraud:** Target variable (1 = Fraud, 0 = Legitimate).

## Project Workflow

The notebook follows a structured 10-step approach:

1. **Import Libraries:** Setup of environment (Pandas, Scikit-Learn, XGBoost, etc.).
2. **Read Dataset:** Loading the `Fraud_Analysis_Dataset.csv`.
3. **Dataset Overview:** Initial data inspection.
4. **Data Preprocessing:** Cleaning data, treating outliers, and feature engineering.
5. **EDA:** Deep dive into transaction patterns.
6. **Scale Features:** Establishing pipelines for feature scaling.
7. **Random Forest:** Model implementation and tuning.
8. **Logistic Regression:** Baseline classification model.
9. **XGBOOST:** Advanced gradient boosting implementation.
10. **Conclusion:** Final performance comparison.

## Methodology

* **Preprocessing:** Includes handling outliers and encoding categorical variables like `type`.
* **Class Imbalance:** Strategies implemented to manage the high ratio of legitimate to fraudulent transactions.
* **Evaluation Metrics:** Models are evaluated using Accuracy, Precision, Recall, F1-score, and AUC.

## Models Evaluated

The project compares three main classification models:

* **Logistic Regression**
* **Random Forest**
* **XGBoost**

## Results & Conclusion

Final results are summarized in a comparison table sorted by **Recall**, as capturing all fraudulent instances is the highest priority for this security-focused application.

| Model | Accuracy | Precision | Recall | F1-Score |
| --- | --- | --- | --- | --- |
| **Logistic Regression** | 0.919 | 0.56 | 0.99 | 0.72 |
| **Random Forest** | 0.993 | 0.99 | 0.95 | 0.97 |
| **XGBoost** | 0.996 | 0.98 | 0.98 | 0.98 |

*XGBoost and Random Forest show superior performance, particularly in maintaining a high balance between Precision and Recall.*
