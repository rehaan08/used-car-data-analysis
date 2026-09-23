# used-car-data-analysis

# Automobile Data Wrangling & Preprocessing

A comprehensive Python data wrangling project demonstrating data cleaning, standardization, normalization, binning, and indicator variable transformation on the UCI Automobile Dataset.

---

## 📌 Project Overview

Raw data collected from real-world sources often contains missing values, improper formatting, or non-standardized metrics that can distort statistical modeling and machine learning algorithms. 

This project transforms raw automobile specifications into a clean, well-structured dataset (`clean_df.csv`) ready for exploratory data analysis (EDA) and predictive modeling.

---

## 🔑 Key Features & Steps

1. **Handling Missing Values:**
   * Replaced missing `"?"` markers with `NaN`.
   * Imputed numerical variables (`normalized-losses`, `bore`, `stroke`, `horsepower`, `peak-rpm`) using mean values.
   * Imputed categorical variables (`num-of-doors`) using frequency/mode substitution.
   * Dropped rows missing target labels (`price`)[cite: 11].

2. **Data Formatting & Type Conversion:**
   * Cast object data types to proper numerical representations (`float`, `int`)[cite: 11].

3. **Data Standardization & Normalization:**
   * Transformed fuel consumption (`city-mpg`, `highway-mpg`) into standardized metric units (`L/100km`)[cite: 11].
   * Scaled feature dimensions (`length`, `width`, `height`) using max-value feature scaling to a range of $[0, 1]$[cite: 11].

4. **Binning:**
   * Segmented continuous `horsepower` values into discrete categories (`Low`, `Medium`, `High`) using equal-width binning for grouped distribution analysis[cite: 11].

5. **Indicator (Dummy) Variables:**
   * Converted categorical variables (`fuel-type`, `aspiration`) into numerical binary indicator vectors ($0$s and $1$s) for future regression analysis[cite: 11].

---

## 🛠️ Tech Stack & Dependencies

* **Language:** Python 3.x
* **Data Processing:** `pandas`, `numpy`[cite: 11]
* **Visualization:** `matplotlib`[cite: 11]

Install dependencies via pip:

```bash
pip install pandas numpy matplotlib
