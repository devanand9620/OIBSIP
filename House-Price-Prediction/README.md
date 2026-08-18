# House Price Prediction

## 📌 Project Overview

This project focuses on predicting house prices using **Linear Regression**. The model uses features such as house size, number of bedrooms, number of bathrooms, house age, and location to estimate the price of a house.

This project was completed as part of the **OASIS INFOBYTE Data Analytics Internship**.

## 🎯 Objectives

- Create and inspect a house price dataset.
- Prepare the data for machine learning.
- Convert categorical location values into numerical features.
- Split the data into training and testing sets.
- Train a Linear Regression model.
- Predict house prices using the trained model.
- Evaluate the model using MSE, RMSE, and R² Score.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Visual Studio Code

## 📂 Files

- `House_Price_Prediction.ipynb` – Jupyter Notebook containing the complete machine learning workflow.
- `house_prices.csv` – Dataset used for house price prediction.

## 📊 Features Used

The model uses the following features:

- `SquareFeet` – Size of the house
- `Bedrooms` – Number of bedrooms
- `Bathrooms` – Number of bathrooms
- `Age` – Age of the house
- `Location` – Location category
- `Price` – Target variable

## 🔄 Methodology

### 1. Dataset Creation

A dataset containing 200 house records was created with different house characteristics and prices. :contentReference[oaicite:1]{index=1}

### 2. Data Preprocessing

The `Location` column was converted into numerical features using one-hot encoding.

The data was then divided into training and testing sets using an 80:20 split. :contentReference[oaicite:2]{index=2}

### 3. Model Training

A **Linear Regression** model was trained using the training dataset.

### 4. Model Evaluation

The model was evaluated using:

- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

These metrics help measure the prediction error and model performance. :contentReference[oaicite:3]{index=3}

## 📈 Result

The trained Linear Regression model predicts house prices based on the selected house features. Model performance is evaluated using the test dataset and the calculated evaluation metrics.

## 💡 Skills Demonstrated

- Machine Learning
- Linear Regression
- Data Preprocessing
- One-Hot Encoding
- Train-Test Split
- Model Evaluation
- Python Programming
- Pandas
- Scikit-learn

## 👨‍💻 Internship

**OASIS INFOBYTE – Data Analytics Internship**
