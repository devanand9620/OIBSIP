## 📂 Project Structure

```text
Retail-Sales-EDA/
│
├── Retail_Sales_EDA.ipynb        # Main analysis pipeline and visualizations
├── retail_sales_dataset.csv       # Raw transactional dataset
├── requirements.txt               # Required Python dependencies
└── README.md                      # Project documentation and summary
```

---

## 📊 Exploratory Data Analysis Pipeline & Findings

### 1. Data Quality & Initial Inspection
* **Dataset Dimensions:** 1,000 transaction records across 9 distinct columns.
* **Data Integrity:** Zero missing values (0 nulls) and zero duplicate records (0 duplicates).
* **Feature Engineering:** Extracted `YearMonth`, `Quarter`, `Month`, and `DayOfWeek` from transaction dates; segmented customer ages into standard cohorts (18–25 Youth, 26–35 Young Adult, 36–50 Middle-Aged, 51+ Senior).

### 2. Descriptive Statistics
* **Age:** Mean = 41.39 years | Median = 42.00 years | Std Dev = 13.68 | Range = 18 to 64 years
* **Total Amount (Spend):** Mean = $456.00 | Median = $135.00 | Std Dev = $559.99 | Max = $2,000.00
* **Price per Unit:** Mean = $179.89 | Median = $50.00 | Std Dev = $189.68 | Max = $500.00
* **Quantity:** Mean = 2.51 units | Median = 3.00 units | Std Dev = 1.13 | Range = 1 to 4 units

### 3. Time Series & Seasonality Analysis
* **Monthly Trajectory:** Examined annual revenue trends across 2023, showcasing steady baseline demand with cyclical purchase spikes in spring (May) and year-end holiday seasons (October and December).
* **Quarterly Performance:** Q2 and Q4 recorded higher aggregate demand driven by seasonal transitions and holiday gift purchasing.
* **Day-of-Week Distribution:** Customer shopping volume remains well-balanced across weekdays and weekends, indicating sustained omnichannel retail engagement.

### 4. Customer Demographics & Segmentation
* **Gender Distribution:** Near-equal retail participation: Females represent 51.0% (510 transactions, $232,840) and Males represent 49.0% (490 transactions, $223,160).
* **Age Cohort Contribution:** Shoppers in the 26–35 (Young Adult) and 36–50 (Middle-Aged) brackets account for over 60% of total transactions and store revenue.

### 5. Product Category Performance
* **Electronics:** Generated the highest gross revenue at $156,905 across 849 units sold.
* **Clothing:** Followed closely with $155,580 in revenue, driving the highest overall sales volume (894 units).
* **Beauty:** Contributed $143,515 in revenue across 771 units sold.

### 6. Correlation Analysis
* **Strong Linear Relationships:** Total Amount strongly correlates with Price per Unit ($r = 0.85$) and moderately with Quantity ($r = 0.37$).
* **Demographic Neutrality:** Customer Age exhibits negligible correlation with total purchase amount ($r = -0.06$), confirming that high-value basket sizes occur across all adult age tiers.

### 7. Non-Obvious Insight: Gender-Specific Category Spending
* In the **Beauty** category, Male shoppers registered a higher average ticket value ($487.13) than Female shoppers ($450.78), challenging the conventional retail assumption that male personal care spending is strictly low-ticket.
* In the **Clothing** segment, Female shoppers led average transaction spending ($467.10 vs. $419.80 for males).

---

## 💡 Actionable Business Recommendations
1. **Targeted Men's Premium Grooming Bundles:** Capitalize on the higher average order value of male shoppers in the Beauty category by marketing curated premium skincare and grooming kits directly to male professionals.
2. **Loyalty Incentives for Core Demographics (Ages 26–50):** Concentrate promotional spend, personalized email marketing, and tiered reward structures on 26–50-year-olds, who form the store's primary revenue engine.
3. **High-Margin Cross-Category Merchandising:** Introduce cross-category bundles pairing complementary apparel and tech accessories to elevate the store's median transaction basket beyond $135.

---

## ▶️ How to Run
1. Clone this repository or open the project folder in your editor.
2. Install the required dependencies:
```bash
pip install -r requirements.txt
```
3. Ensure `retail_sales_dataset.csv` is present in the workspace root directory.
4. Open `Retail_Sales_EDA.ipynb` in Jupyter Notebook / VS Code and select **Run All** to execute the pipeline and generate all visualizations.

---

## 📚 Skills Demonstrated
* Data Quality Assessment & Schema Validation
* Exploratory Data Analysis (EDA)
* Time Series & Seasonality Analysis
* Customer Demographic Segmentation
* Statistical Correlation Analysis
* Data Visualization (Matplotlib & Seaborn)
* Business Intelligence & Strategy Formulation

---

## 👤 Author
Devanand K
Data Analytics Intern
OASIS INFOBYTE Internship