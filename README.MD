# Customer Churn Prediction - MLOps Project

An end-to-end Customer Churn Prediction project that combines Machine Learning
with MLOps practices for data versioning, experiment tracking, model management,
and reproducibility.

---

## 📌 Project Overview

Customer churn prediction helps businesses identify customers who are likely
to discontinue their services.

In this project, the Telco Customer Churn dataset is used to build a machine
learning classification model that predicts whether a customer will churn.

The project follows an MLOps workflow using:

- Python
- Scikit-learn
- Git & GitHub
- DVC
- MLflow

The initial baseline model is Logistic Regression, which currently achieves
approximately **80.62% accuracy**.

---

## 🎯 Objectives

- Perform Exploratory Data Analysis (EDA)
- Clean and preprocess customer data
- Perform feature engineering
- Encode categorical variables
- Standardize numerical features
- Train machine learning classification models
- Evaluate model performance
- Track experiments using MLflow
- Track datasets and model artifacts using DVC
- Version control source code using Git/GitHub
- Register and version machine learning models using MLflow
- Compare different machine learning models

---

## 📊 Dataset

### Telco Customer Churn Dataset

The dataset contains customer information related to:

- Customer demographics
- Tenure
- Contract type
- Internet service
- Online services
- Payment method
- Monthly charges
- Total charges
- Churn status

### Dataset Size

- **Rows:** 7,043
- **Target Variable:** `Churn`

### Target Variable

| Value | Meaning |
|---|---|
| `Yes` | Customer churned |
| `No` | Customer did not churn |

---

## 🧹 Data Preprocessing

The following preprocessing steps were performed:

- Checked for missing values
- Identified whitespace values in `TotalCharges`
- Converted numerical columns to appropriate data types
- Removed unnecessary columns such as `customerID`
- Applied binary encoding to binary categorical variables
- Applied One-Hot Encoding to multi-category variables
- Standardized numerical features

### Numerical Features Standardized

- `tenure`
- `MonthlyCharges`
- `TotalCharges`

### Categorical Features

Binary categorical variables were encoded into numerical values.

Multi-category variables were transformed using One-Hot Encoding.

Examples:

- `Contract`
- `InternetService`
- `MultipleLines`
- `PaymentMethod`
- `OnlineSecurity`
- `OnlineBackup`
- `DeviceProtection`
- `TechSupport`
- `StreamingTV`
- `StreamingMovies`

---

## 📈 Exploratory Data Analysis

Important observations from the analysis include:

- Month-to-month contract customers have a significantly higher churn rate.
- Customers with shorter tenure are more likely to churn.
- Fiber optic customers show relatively high churn.
- Senior citizens have a higher churn rate compared to non-senior citizens.
- Customers with higher monthly charges tend to have higher churn.
- Long-term contract customers have considerably lower churn rates.

---

## 🤖 Machine Learning

### Baseline Model

The initial baseline model used in the project is:

**Logistic Regression**

Configuration:

```text
max_iter = 1000