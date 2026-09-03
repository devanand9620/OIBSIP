# Level 2 - Task 1: House Price Prediction with Linear Regression

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?logo=scikit-learn)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-purple?logo=pandas)
![Seaborn](https://img.shields.io/badge/Seaborn-Data%20Visualization-green)

---

## 📌 Project Overview
This project focuses on building, evaluating, and interpreting a **Multivariable Linear Regression** model to predict residential house prices using the King County housing dataset. It covers the end-to-end data science pipeline: Exploratory Data Analysis (EDA), feature engineering, categorical encoding, model training, residual diagnostics, coefficient interpretation, and regularization comparison (Ridge and Lasso).

---

## 📂 Project Structure
```text
House-Price-Prediction/
├── House_Price_Prediction.ipynb   # Complete Step-by-Step Jupyter Notebook
├── house_prices.csv               # Dataset file
├── requirements.txt               # Dependencies
└── README.md                      # Project Documentation
---

## 🛠️ Tech Stack & Libraries
* **Language:** Python 3.x
* **Data Manipulation:** pandas, numpy
* **Data Visualization:** matplotlib, seaborn
* **Machine Learning:** scikit-learn
* **Environment:** Jupyter Notebook / VS Code

---

## 🔍 Key Steps & Workflow

1. **Exploratory Data Analysis (EDA):**
   - Verified data integrity with null-value checks and descriptive statistics.
   - Plotted the distribution of the target variable (`price`).

2. **Data Preprocessing & Feature Engineering:**
   - Engineered new features: calculated `house_age` from `yr_built` and binary flag `is_renovated`.
   - Dropped non-predictive identifiers (`id`, `date`).
   - Applied One-Hot Encoding to categorical variables (`waterfront`, `condition`).

3. **Correlation Analysis:**
   - Visualized feature relationships using a correlation heatmap to identify strong price drivers (`sqft_living`, `grade`, `sqft_above`, `bathrooms`, `lat`).

4. **Model Training & Evaluation (80/20 Split):**
   - Trained an Ordinary Least Squares (OLS) **Linear Regression** model.
   - Evaluated accuracy using **Mean Squared Error (MSE)**, **Root Mean Squared Error (RMSE)**, and **R² Score**.

5. **Diagnostic Visualizations:**
   - **Actual vs. Predicted Scatter Plot:** Evaluated prediction fit against the ideal diagonal line.
   - **Residual Plot:** Checked for random error distribution (homoscedasticity).
   - **Coefficient Analysis:** Identified features with the highest positive and negative impact on price.

6. **Bonus - Regularization Benchmark:**
   - Standardized features using `StandardScaler`.
   - Compared performance against **Ridge (L2)** and **Lasso (L1)** regularized linear models.

---

## 📊 Model Performance Summary

- **Linear Regression (OLS):**
  - R² Score: **0.7015**
  - RMSE: **$212,432.90**

- **Ridge Regression (L2):**
  - R² Score: **0.7015**
  - RMSE: **$212,434.50**

- **Lasso Regression (L1):**
  - R² Score: **0.7015**
  - RMSE: **$212,432.70**

---

## 🚀 How to Run the Project

1. **Install required dependencies:**
   ```bash
   pip install -r requirements.txt
   Launch Jupyter Notebook:
   jupyter notebook House_Price_Prediction.ipynb

   
     👤 Author
Devanand K

Oasis Infobyte Data Analytics Internship