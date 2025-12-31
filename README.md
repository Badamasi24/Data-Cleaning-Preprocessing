# Data-Cleaning-Preprocessing
Using python and pandas to prepare data cleaning and preprocessing, handling missing value, removing duplicate and changing data types 
# Task 1: Data Cleaning and Preprocessing (S&P 500 Dataset)

## 📌 Project Overview
In the world of stock market analysis, "Garbage In, Garbage Out" is a fundamental rule. The goal of this task was to take a raw, uncurated dataset of stock prices data set and transform it into a high-integrity, analysis-ready format using **Python** and **Pandas**.

## 🧹 Data Cleaning Workflow

### 1. Handling Missing Values
Financial datasets often have gaps due to trading halts or reporting delays. 
- **Strategy:** I used **Median Imputation** for price-related columns (`open`, `high`, `low`, `close`).
- **Why Median?** Stock data is highly susceptible to outliers (like Amazon or Google trading at \$2000+). The median is a more "robust" statistic than the mean and prevents imputation from biasing the distribution.

### 2. Deduplication
- **Strategy:** Identified and removed duplicate rows based on the unique combination of `date` and `symbol`.
- **Impact:** This ensures that market volume and daily returns are not artificially inflated by redundant entries.

### 3. Data Standardization
- **Datetime Conversion:** Transformed the `date` column from generic strings to **datetime64[ns]** objects. This enables high-performance time-series indexing.
- **Categorical Integrity:** Standardized stock `symbols` to uppercase and stripped leading/trailing whitespace to ensure error-free filtering and grouping.

## 🚀 Final Objectives Met
- **Completeness:** 0% null values in critical price columns.
- **Uniqueness:** Guaranteed unique records for every stock on every trading day.
- **Efficiency:** Optimized data types for faster computation in subsequent EDA tasks.

## 🛠️ Tools Used
- **Language:** Python
- **Libraries:** Pandas (Data manipulation), NumPy (Numerical operations)
