# 📊 Retail Sales Exploratory Data Analysis (EDA)

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange.svg)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-teal.svg)](https://seaborn.pydata.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## 📌 Project Overview

This project demonstrates professional-level **Exploratory Data Analysis (EDA) and Business Intelligence** on a comprehensive retail transaction dataset (`retail_sales_dataset.csv`). The primary goal is to systematically evaluate revenue dynamics, customer demographic behavior (age groups and gender breakdown), product category performance, and correlation metrics to deliver data-driven, actionable recommendations for optimizing sales and marketing strategies.

This project was completed as part of the **Data Analytics Internship** at **OASIS INFOBYTE** (**Task 1: Exploratory Data Analysis**).

---

## 🎯 Objectives

* Load, inspect, and validate dataset dimensions, structure, null counts, and duplicates.
* Perform data cleaning, datetime parsing, and feature engineering (`YearMonth`, `DayOfWeek`, `Age Group`).
* Compute comprehensive **Descriptive Statistics** (Mean, Median, Mode, Standard Deviation, Min, Max).
* Perform **Time Series Analysis** on monthly and daily sales trajectories to uncover demand seasonality.
* Conduct **Customer Demographics & Segmentation Analysis** covering gender ratios and age cohort spending.
* Evaluate **Product & Category Performance** to identify top revenue-generating merchandise and unit sales.
* Generate a full **Correlation Matrix Heatmap** across all numerical metrics.
* Uncover non-obvious business relationships (gender-specific category preferences and spending depth).
* Deliver data-driven, actionable business recommendations.

---

## 🛠️ Technologies Used

* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Environment:** Jupyter Notebook, Visual Studio Code

---

## 📂 Project Structure

```text
Retail-Sales-EDA/
│
├── Retail_Sales_EDA.ipynb        # Main analysis pipeline and visualizations
├── retail_sales_dataset.csv       # Raw transactional dataset
├── requirements.txt               # Required Python dependencies
└── README.md                      # Project documentation and summary
📊 Exploratory Data Analysis Pipeline & Findings
1. Data Quality & Initial Inspection
Dataset Dimensions: 1,000 transaction records across 9 distinct columns.

Data Integrity: Zero missing values (0 nulls) and zero duplicate records (0 duplicates).

Feature Engineering: Extracted YearMonth, Month, and DayOfWeek from transaction dates; binned customer ages into standardized demographic cohorts (18-25 Youth, 26-35 Young Adult, 36-50 Middle-Aged, 51+ Senior).

2. Descriptive Statistics
Age: Mean = 41.39 years | Median = 42.00 years | Std Dev = 13.68 | Range = 18 to 64 years

Total Amount (Spend): Mean = $456.00 | Median = $135.00 | Std Dev = $560.00 | Max = $2,000.00

Price per Unit: Mean = $179.89 | Median = $50.00 | Std Dev = $189.68 | Max = $500.00

Quantity: Mean = 2.51 units | Median = 3.00 units | Std Dev = 1.13 | Range = 1 to 4 units

3. Time Series & Seasonality Analysis
Monthly Trajectory: Examined annual revenue trends across 2023, showcasing steady baseline demand with cyclical purchase spikes in spring (May) and year-end holiday seasons (October and December).

Day-of-Week Distribution: Customer shopping volume remains well-balanced across weekdays and weekends, indicating sustained omnichannel retail engagement.

4. Customer Demographics & Segmentation
Gender Distribution: Near-equal retail participation: Females represent 51.0% (510 transactions, $232,840) and Males represent 49.0% (490 transactions, $223,160).

Age Cohort Contribution: Shoppers in the 26–35 (Young Adult) and 36–50 (Middle-Aged) brackets account for over 60% of total transactions and store revenue.

5. Product Category Performance
Electronics: Generated the highest gross revenue at $156,905 across 849 units sold.

Clothing: Followed closely with $155,580 in revenue, driving the highest overall sales volume (894 units).

Beauty: Contributed $143,515 in revenue across 771 units sold.

Transaction volume and unit demand remain diversified without disproportionate risk on a single product segment.

6. Correlation Analysis
Constructed a Pearson correlation matrix heatmap across all numerical variables (Age, Quantity, Price per Unit, Total Amount).

Strong Linear Relationships: Total Amount strongly correlates with Price per Unit (r = 0.85) and moderately with Quantity (r = 0.37).

Demographic Neutrality: Customer Age exhibits negligible correlation with total purchase amount (r = -0.06), confirming that high-value basket sizes occur across all adult age tiers.

7. Non-Obvious Insight: Gender-Specific Category Spending
In the Beauty category, Male shoppers registered a higher average ticket value ($487.13) than Female shoppers ($450.78), challenging the conventional retail assumption that male personal care spending is strictly low-ticket.

In the Clothing segment, Female shoppers led average transaction spending ($467.10 vs. $419.80 for males).

💡 Actionable Business Recommendations
Targeted Men's Premium Grooming Bundles:

Capitalize on the higher average order value of male shoppers in the Beauty category by marketing curated premium skincare and grooming kits directly to male professionals.

Loyalty Incentives for Core Demographics (Ages 26–50):

Concentrate promotional spend, personalized email marketing, and tiered reward structures on 26–50-year-olds, who form the store's primary revenue engine.

High-Margin Cross-Category Merchandising:

Introduce cross-category bundles pairing complementary apparel and tech accessories to elevate the store's median transaction basket beyond $135.

▶️ How to Run
Clone this repository or open the project folder in Visual Studio Code.

Install the required dependencies:
pip install -r requirements.txt
Ensure retail_sales_dataset.csv is present in the workspace root directory.
t
Open Retail_Sales_EDA.ipynb in Jupyter Notebook / VS Code and select Run All to execute the complete analytical pipeline and generate all visualizations.

📚 Skills Demonstrated
Data Quality Assessment & Schema Validation

Exploratory Data Analysis (EDA)

Time Series & Seasonality Analysis

Customer Demographic Segmentation

Statistical Correlation Analysis

Data Visualization (Matplotlib & Seaborn)

Business Intelligence & Strategy Formulation

👤 Author
Devanand K

Data Analytics Intern

OASIS INFOBYTE Internship