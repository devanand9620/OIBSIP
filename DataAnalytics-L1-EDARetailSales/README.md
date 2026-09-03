# TASK 1: Exploratory Data Analysis (Retail Sales Dataset)

## 📌 Project Overview

This project demonstrates professional-level **Exploratory Data Analysis (EDA) and Business Intelligence** on a comprehensive global retail transaction dataset (`SuperStoreOrders.csv`). The primary goal is to systematically evaluate revenue dynamics, customer demographic behavior, product category performance, and correlation metrics to deliver data-driven, actionable recommendations for optimizing profit margins.

This project was completed as part of the **Data Analytics Internship** at **OASIS INFOBYTE** (Task 1: Exploratory Data Analysis).

---

## 🎯 Objectives

* Load, inspect, and validate dataset dimensions, structure, null counts, and duplicates.
* Clean financial currency features and cast numerical attributes to appropriate types.
* Compute comprehensive **Descriptive Statistics** (Mean, Median, Mode, Standard Deviation, Min, Max).
* Perform **Time Series Analysis** on monthly and quarterly trajectories to uncover demand seasonality.
* Conduct **Customer Demographics & Segmentation Analysis** using distribution and revenue visualizations.
* Evaluate **Product & Category Performance** to identify top-selling inventory and core profit drivers.
* Generate a full **Correlation Matrix Heatmap** across numerical metrics.
* Uncover non-obvious business relationships (Impact of Discounting on Net Profitability).
* Deliver data-driven, actionable business recommendations.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook
* Visual Studio Code

---

## 📂 Project Structure

```text
Retail-Sales-EDA/
│
├── Retail_Sales_EDA.ipynb
├── SuperStoreOrders.csv
├── requirements.txt

📊 Exploratory Data Analysis Pipeline & Findings
1. Data Quality & Initial Inspection
Inspected dataset structure (51,290 rows, 21 columns).

Verified zero missing values (0 nulls) and zero duplicate transactions (0 duplicates).

Cleaned comma formatting and string symbols in sales to cast it into a standard float64 numeric type.

2. Descriptive Statistics
sales: Mean = $246.49 | Median = $85.05 | Std Dev = $486.22 | Max = $22,638.48

profit: Mean = $28.61 | Median = $9.24 | Std Dev = $174.34 | Max = $8,399.98

discount: Mean = 0.14 | Median = 0.00 | Std Dev = 0.21 | Max = 0.85

quantity: Mean = 3.48 | Median = 3.00 | Std Dev = 2.28 | Max = 14

3. Time Series & Seasonality Analysis
Extracted monthly (YearMonth) and quarterly (Quarter) periods from transaction dates.

Monthly Trajectory: Plotted multi-year revenue growth showcasing consistent annual expansion.

Quarterly Demand: Identified strong, recurring demand surges in Q4 (October–December) across all operating years driven by holiday commercial activity.

4. Customer Demographics & Segmentation
Order Share: Consumer segment leads customer distribution with ~51.5% of total orders, followed by Corporate (~30.3%) and Home Office (~18.2%).

Revenue Contribution: The Consumer segment generates the largest share of overall business revenue.

5. Product & Category Performance
Identified and mapped the Top 10 Best-Selling Products by gross revenue.

Analyzed revenue breakdown across major categories, establishing Technology as the highest revenue and net profit driver.

6. Correlation Analysis
Built a Pearson correlation heatmap across numerical metrics (sales, quantity, discount, profit, shipping_cost).

Verified strong positive correlation between sales volume and gross revenue, while discounts display negative associations with net profitability.

7. Non-Obvious Insight: Discount vs. Profitability
Evaluated average transaction profit against applied discount rates.

Key Finding: Discount rates exceeding 20% cause sharp margin collapse, driving average transactions into net operating losses.
💡 Actionable Business Recommendations
Enforce 20% Discount Ceilings: Establish rigid discount guardrails (max 20%)—especially on lower-margin furniture products—to protect operating margins.

Q3 Inventory & Campaign Ramp-Up: Scale supplier procurement and marketing allocations during late Q3 to maximize Q4 demand capture and prevent stockouts.

Targeted B2B Volume Programs: Implement structured tier-based loyalty and volume incentives for Corporate and Home Office customer groups to expand Average Order Value (AOV).

▶️ How to Run
Clone this repository or download the project files.

Open the project folder in Visual Studio Code.

Install the required dependencies:

Bash
pip install pandas numpy matplotlib seaborn jupyter
Ensure SuperStoreOrders.csv is present in the workspace root.

Open Retail_Sales_EDA.ipynb and select Run All to execute the pipeline and generate all visualizations.

📚 Skills Demonstrated
Data Quality Assessment & Validation

Exploratory Data Analysis (EDA)

Time Series & Seasonality Analysis

Customer Segmentation & Demographic Profiling

Statistical Correlation Analysis

Data Visualization (Matplotlib & Seaborn)

Business Intelligence & Strategic Recommendations

👨‍💻 Author
Devanand K

Data Analytics Intern

OASIS INFOBYTE Internship