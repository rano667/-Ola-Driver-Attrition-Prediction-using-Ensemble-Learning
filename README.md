# 🚖 Ola Driver Attrition Prediction using Ensemble Learning

## 📌 Problem Statement

Recruiting and retaining drivers is a critical challenge for Ola. High attrition increases operational costs and lowers service quality. This project aims to **predict driver attrition** using historical performance and demographic data, helping Ola retain valuable drivers through timely intervention.

---

## 📂 Dataset Overview

The dataset contains monthly snapshots of Ola drivers' details across 2019–2020.

**Key Attributes:**

- `Driver_ID`, `MMM-YY`, `Date of Joining`, `Last Working Date`
- `Age`, `Gender`, `City`, `Education_Level`
- `Income`, `Total Business Value`, `Quarterly Rating`, `Grade`, `Joining Designation`

---

## 🎯 Objective

1. Predict whether a driver will **leave Ola** or not (binary classification)
2. Engineer new features to better capture **driver performance trends**
3. Handle **missing data**, **class imbalance**, and **standardization**
4. Build models using **Random Forest** and **XGBoost**
5. Derive **insights & recommendations** for retention strategies

---

## 🔍 Workflow Summary

### 📊 Exploratory Data Analysis (EDA)
- Date parsing & conversion
- Missing value analysis (KNN Imputation used for `Age`)
- Feature engineering:
  - `Attrition` (target)
  - `Quarterly Rating Change`
  - `Income Change`
- Correlation analysis

### ⚙️ Preprocessing
- KNN Imputation for missing values
- One-Hot Encoding of categorical features
- Feature scaling (StandardScaler)
- Class imbalance treatment (RandomOverSampler)

### 🤖 Model Building
- **Random Forest Classifier**
- **XGBoost Classifier**
- Hyperparameter tuning (GridSearchCV)
- Evaluation via:
  - Confusion Matrix
  - Classification Report
  - ROC AUC Score & Curve

---

## 📈 Results

| Model            | Accuracy | Recall (Attrition) | ROC-AUC |
|------------------|----------|---------------------|---------|
| Random Forest    | 80%      | 90%                | 0.81    |
| XGBoost          | 79%      | 89%                | 0.80    |

✅ Random Forest outperformed slightly and is recommended for deployment.

---

## 🧠 Key Takeaways

- Features like **Income Change**, **Rating Change**, and **Grade** are strong predictors of attrition.
- The models are effective in predicting likely driver exits, helping reduce churn.
- Targeted interventions based on model predictions can **save costs** and **retain top performers**.
