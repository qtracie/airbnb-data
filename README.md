![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)
![Completed](https://img.shields.io/badge/Status-Completed-brightgreen)
# Airbnb Data Cleaning & Preprocessing Project 🧹📊

This project focuses on one of the most critical stages of the data science pipeline: **Data Cleaning and Preprocessing**. Using a large-scale Airbnb dataset, I transformed raw, inconsistent data into a high-quality, model-ready dataset suitable for downstream analytics and machine learning tasks.

## 📌 Project Objective
In real-world analytics, the quality of insights depends entirely on the quality of the data. This project demonstrates a systematic approach to handling missing values, outliers, and complex string manipulations to prepare data for future predictive modeling.

## 🛠️ Tech Stack
* **Language:** Python
* **Primary Library:** `Pandas` (Data Manipulation)
* **Supporting Libraries:** `NumPy`, `Seaborn`, `Matplotlib` (Visualization of Data Quality)

## 🚀 Data Cleaning & Preprocessing Workflow

### 1. Initial Data Audit & Target Refinement
* **Target Cleaning:** Identified and removed records with null values in the `price` column to ensure dataset reliability.
* **Handling Missing Values:** - Performed a row-wise and column-wise null analysis.
    - Dropped columns with a high percentage of missing values (exceeding 50-60%) that couldn't provide meaningful signals.
    - Filtered out rows with critical missing information to reduce noise and improve data density.
* **Redundancy Removal:** Dropped irrelevant high-cardinality columns (URLs, IDs, scrape dates) to optimize memory usage.

### 2. Advanced Imputation Strategies
* **Numerical Features:** Applied median imputation to handle skewed distributions and outliers(e.g., `host_listings_count`).
* **Categorical Features:** Logically filled missing boolean indicators (e.g., `host_is_superhost`).
* **Percentage Fields:** Processed string-based percentages into numerical values and handled "Unknown" categories for missing response data.

### 3. Feature Engineering (Value Extraction)
* **Text Feature Extraction:** Created binary keyword indicators from listing descriptions (e.g., "spacious", "beach", "luxury").
* **Temporal Features:** Engineered host seniority (years active) and recency of reviews from date fields.
* **Categorical Binning:** Grouped continuous variables (like response rates) into discrete bins to simplify the feature space and improve model interpretability.

### 4. Data Distribution & Consistency
* Standardized boolean values 't'/'f' into binary numeric format.
* Used Histograms to verify that the cleaning process did not introduce biases in the review score distributions.

## 📊 Final Result
The output of this project is a **Cleaned Dataset** with:
* Zero missing values in critical feature columns.
* 10+ new engineered features extracted from raw text and dates.
* Optimized data types for efficient modeling and analysis.
This cleaned dataset is ready for applications such as price prediction, demand forecasting, and host performance analysis.

## 🏗️ How to Use
1. Clone the repo:
   ```bash
   git clone [https://github.com/qtracie/airbnb-data.git](https://github.com/qtracie/airbnb-data.git)
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Execute the script:
   ```bash
   python notebooks/airbnb-analysis.py
   ```
