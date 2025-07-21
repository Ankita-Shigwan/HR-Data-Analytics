# 🧠 Employee Attrition Prediction using Machine Learning

This project analyzes employee attrition using machine learning models to help HR departments identify employees who are likely to leave and understand the key factors driving attrition.

---

## 📌 Project Overview

- **Dataset**: `Human_Resources.csv`  
- **Goal**: Predict whether an employee will leave the company  
- **Target Variable**: `Attrition` (Yes/No → 1/0)

---

## 🛠️ Models Used & Accuracy

| Model                   | Accuracy (%)     |
|------------------------|------------------|
| Logistic Regression     | 84.78            |
| Random Forest           | 84.78            |
| XGBoost Classifier      | 84.51            |
| K-Nearest Neighbors     | 83.97            |
| **Support Vector Machine** | **85.87 ✅**  |

> ✅ **SVM** achieved the highest accuracy and was used as the final classifier.  
> 🧩 **XGBoost** was used to extract feature importance and interpret business drivers of attrition.

---

## 🔍 Top 15 Features (XGBoost)

Key factors contributing to employee attrition:

- OverTime
- JobRole (Sales Executive, Healthcare Rep, etc.)
- MaritalStatus (Divorced, Single)
- StockOptionLevel
- MonthlyIncome
- JobInvolvement
- EnvironmentSatisfaction
- WorkLifeBalance
- DistanceFromHome
- Age
- PerformanceRating
- YearsAtCompany
- NumCompaniesWorked
- TotalWorkingYears
- JobSatisfaction

---

## ⚙️ Techniques Used

- Exploratory Data Analysis (EDA)
- Data Cleaning & Preprocessing
- One-Hot Encoding (for categorical variables)
- Feature Scaling using `MinMaxScaler`
- Train-Test Split (80-20)
- ML Model Training & Evaluation
- Feature Importance with XGBoost
- Model Comparison
- Final Model Saving using `joblib`

---

## 📁 Output Files

- `svm_attrition_model.pkl` — Final classification model
- `xgboost_attrition_model.pkl` — Used for extracting feature importance
- Visualizations for:
  - Attrition by various features (OverTime, JobRole, etc.)
  - Feature importance (bar charts)

---

## 🧾 Requirements

Install the following Python libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost joblib
