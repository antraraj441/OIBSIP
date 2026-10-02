# OIBSIP Task 3 – Data Cleaning and Preprocessing

## 📌 Project Overview

This project focuses on cleaning and preprocessing a deliberately messy customer dataset and transforming it into a clean, consistent, and analysis-ready dataset.

The main goal is to identify data quality issues, apply appropriate cleaning techniques, document each decision, and produce a final cleaned CSV file.

## 🎯 Objective

To demonstrate professional-level data cleaning skills by systematically identifying and fixing:

* Missing values
* Duplicate records
* Inconsistent formatting
* Incorrect data types
* Invalid values
* Numerical outliers

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Jupyter Notebook

## 📂 Dataset

The project uses a deliberately messy customer dataset containing the following columns:

| Column        | Description                |
| ------------- | -------------------------- |
| `Customer_ID` | Unique customer identifier |
| `Name`        | Customer name              |
| `Age`         | Customer age               |
| `Gender`      | Customer gender            |
| `Join_Date`   | Customer joining date      |
| `Salary`      | Customer salary            |
| `City`        | Customer city              |
| `Rating`      | Customer rating            |

The dataset intentionally contains missing values, duplicate records, inconsistent formats, invalid values, and outliers to demonstrate different data-cleaning techniques.

## 🔍 Data Quality Issues Identified

The following issues were identified during the initial data-quality analysis:

* Missing values in several columns
* Duplicate rows
* Inconsistent gender values such as `M`, `male`, `F`, and `female`
* Different date formats
* Salary values stored as text
* Invalid salary values
* Unrealistic age values
* Rating values outside the expected range
* Salary outliers

## 🧹 Data Cleaning Process

### 1. Data Quality Report

The dataset was initially inspected to identify:

* Number of rows and columns
* Missing values
* Duplicate records
* Data types
* Unique values
* Numerical ranges

### 2. Missing Value Handling

Different strategies were selected according to the type of data:

* **Age:** Median imputation
* **Salary:** Median imputation after converting invalid values to missing
* **City:** Mode imputation
* **Rating:** Median imputation

Median was selected for numerical columns because it is less affected by extreme values.

### 3. Duplicate Removal

Duplicate rows were identified using:

```python
df.duplicated()
```

The duplicate records were removed using:

```python
df.drop_duplicates()
```

### 4. Standardisation

Inconsistent values were converted into a common format.

For example:

```text
M → Male
male → Male
F → Female
female → Female
```

City names were also standardised, and different date formats were converted into a common datetime format.

### 5. Data Type Correction

The following corrections were applied:

* `Customer_ID` → String
* `Age` → Numeric
* `Salary` → Float
* `Rating` → Float
* `Join_Date` → Datetime
* `Gender` → Categorical
* `City` → Categorical

### 6. Invalid Value Handling

Unrealistic ages such as negative values or values above 100 were identified and replaced with missing values before median imputation.

Ratings outside the expected 1–5 range were also identified and corrected.

### 7. Outlier Detection

The Interquartile Range (IQR) method was used to detect salary outliers.

The formula used was:

```text
IQR = Q3 - Q1
Lower Limit = Q1 - 1.5 × IQR
Upper Limit = Q3 + 1.5 × IQR
```

Salary outliers were handled using IQR capping rather than deleting the customer records.

## 📊 Before vs After

A before-and-after comparison was created to evaluate the cleaning process.

The comparison includes:

* Row count
* Column count
* Total missing values
* Duplicate count
* Data types

The final dataset was checked to ensure that the major data-quality issues had been addressed.

## 📁 Project Files

```text
OIBSIP/
│
├── Task3/
│   ├── data_cleaning.ipynb
│   ├── messy_customer_data.csv
│   ├── cleaned_customer_data.csv
│   └── README.md
```

## 💾 Output

The cleaned dataset is saved as:

```text
cleaned_customer_data.csv
```

The cleaned file is ready for further analysis and machine-learning workflows.

## ✅ Key Learning Outcomes

Through this task, I learned how to:

* Perform systematic data-quality checks
* Handle missing values
* Remove duplicate records
* Standardise inconsistent categorical data
* Convert incorrect data types
* Detect invalid values
* Detect and handle numerical outliers
* Compare data quality before and after cleaning
* Export a cleaned dataset to CSV

## 🏁 Conclusion

This project demonstrates a complete data-cleaning workflow using Python, Pandas, and NumPy. The messy dataset was systematically transformed into a cleaner and more consistent dataset suitable for further analysis.

The project also emphasizes documenting cleaning decisions so that the process is transparent and reproducible.

## 👩‍💻 Internship

**Oasis Infobyte – OIBSIP**

**Task 3: Data Cleaning and Preprocessing**
