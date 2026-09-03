# Data Cleaning and Transformation (FIFA 21 Dataset)

## 📌 Project Overview

This project demonstrates professional-level **Data Cleaning and Preprocessing** on a raw, deliberately messy FIFA 21 football dataset (`fifa21_raw_data.csv`). The primary goal is to systematically transform inconsistent, noisy, and unstructured raw records into a clean, standardized, and analysis-ready format (`fifa21_cleaned_data.csv`).

This project was completed as part of the **Data Analytics Internship** at **OASIS INFOBYTE** (Task 3: Cleaning Data).

---

## 🎯 Objectives

* Load and generate a comprehensive **Data Quality Report** (shape, duplicates, nulls, and format anomalies).
* Detect and permanently drop duplicate records.
* Address missing values with structured domain-appropriate imputation strategies.
* Normalize and clean inconsistent string formatting, special symbols, and hidden newline characters.
* Standardize metric measurements (Height to centimeters, Weight to kilograms).
* Parse complex monetary and string notations (EUR values with 'M'/'K' suffixes, Hits counts).
* Correct and cast data types across all columns (Dates to `datetime64`, Identifiers to `string`, Values to numeric `float64`).
* Perform statistical **Outlier Detection** using the Interquartile Range (IQR) method and justify retention decisions.
* Produce a complete **Before vs. After** comparison summary table.
* Export the cleaned dataset to a new CSV file.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Jupyter Notebook
* Visual Studio Code

---

## 📂 Project Structure
Data-Cleaning/
│
├── data_cleaning.ipynb
├── fifa21_raw_data.csv
├── fifa21_cleaned_data.csv
├── requirements.txt
└── README.md
---

## 📊 Data Cleaning Pipeline & Feature Checklist

### 1. Data Quality Report
* Inspected dataset structure (18,979 rows, 77 columns).
* Checked for missing values across all features (found 17,966 missing entries in `Loan Date End`).
* Identified 1 exact duplicate record.
* Identified mixed formats and string data types in `Height`, `Weight`, `Value`, `Wage`, and `Hits`.

### 2. Duplicate Removal
* Detected and removed 1 exact duplicate row using `drop_duplicates()`, retaining 18,978 unique records.

### 3. Missing Data Handling
* **`Loan Date End`**: 17,966 missing entries represent permanent squad contracts (players not currently on loan). Imputed with the categorical label `'Not on Loan'`.
* **`Hits`**: Missing entries imputed with `'0'` representing zero recorded profile visits.

### 4. Text Normalisation & Metric Standardisation
* **Whitespace & Newlines**: Stripped leading/trailing whitespaces and removed hidden `\n` characters across `Team & Contract` and `Hits`.
* **`Hits` Column**: Converted string `'K'` notations (e.g., `'1.5K'`) into numeric float values (`1500.0`).
* **`Height` Column**: Converted mixed feet-and-inches strings (e.g., `5'7"`) and centimeters into a standard metric float format (`Height_cm`).
* **`Weight` Column**: Converted imperial pounds (e.g., `159lbs`) and kilograms into a standard metric float format (`Weight_kg`).

### 5. Data Type Corrections & Currency Parsing
* **Dates**: Converted `Joined` from string object into standard `datetime64` format.
* **Identifiers**: Converted `ID` to string type to prevent erroneous mathematical operations.
* **Monetary Values**: Stripped currency symbols (`€`) and converted multiplier suffixes (`M` for millions, `K` for thousands) into exact `float64` numerical values (`Value_EUR`, `Wage_EUR`, `Release_Clause_EUR`).

### 6. Outlier Detection (IQR Method)
* Applied Interquartile Range (IQR) method on `Wage_EUR`:
  * $Q1 = 1,000 \text{ EUR}$, $Q3 = 8,000 \text{ EUR}$, $\text{IQR} = 7,000 \text{ EUR}$.
  * Upper outlier threshold: $18,500 \text{ EUR}$.
* **Decision**: **Retained all outliers**, as elite football superstars legitimately earn exponential salaries that naturally skew real-world market distributions.

---

## 📋 Before vs. After Summary Table

| Metric | Before Cleaning | After Cleaning |
| :--- | :--- | :--- |
| **Total Rows** | 18,979 | 18,978 |
| **Duplicate Rows** | 1 | 0 |
| **Loan Date End Nulls** | 17,966 | 0 (Imputed `'Not on Loan'`) |
| **Height Data Type** | `object` (e.g., `5'7"`) | `float64` (`Height_cm`) |
| **Weight Data Type** | `object` (e.g., `159lbs`) | `float64` (`Weight_kg`) |
| **Joined Column Type** | `object` (string) | `datetime64[ns]` |
| **ID Column Type** | `int64` | `string` |
| **Value / Wage Type** | `object` (e.g., `€67.5M`) | `float64` (`Value_EUR`) |

---

## ▶️ How to Run

1. Clone this repository or download the project files.
2. Open the project folder in Visual Studio Code.
3. Install the required dependencies:

```bash
pip install pandas numpy jupyter
Ensure fifa21_raw_data.csv is present in the workspace root.

Open data_cleaning.ipynb and select Run All to execute the pipeline and generate fifa21_cleaned_data.csv.

📚 Skills Demonstrated
Data Quality Assessment

Missing Value Imputation

Unit Conversion & Standardisation

Regular Expressions & String Parsing

Data Type Casting

Statistical Outlier Analysis (IQR Method)

Python Programming & Pandas Manipulation

👨‍💻 Author
Devanand K

Data Analytics Intern

OASIS INFOBYTE Internship