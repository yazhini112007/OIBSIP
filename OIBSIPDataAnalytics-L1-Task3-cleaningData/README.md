# Level 1 Task 3: Data Cleaning and Quality Audit

## Project Overview
This task focuses on performing a data quality audit and cleaning pipeline on retail transactional data using Python and Pandas. The goal is to audit missing values, handle categorical string formatting, preserve structural data formats (such as ZIP codes), and evaluate continuous numeric distributions for potential outliers.

---

## Dataset Summary
* **Source File:** `Superstore Dataset Source (1).xlsx` (Sheet: `Orders`)
* **Total Records:** 9,994 rows
* **Total Features:** 21 columns

---

## Data Quality Audit (Pre-Cleaning)

```text
=== DATA QUALITY AUDIT (BEFORE CLEANING) ===
Duplicate Rows Count: 0

Column Summary:
                    Data Type  Null Count  Null Percentage (%)  Unique Values
Row ID                  int64           0                  0.0           9994
Order ID                  str           0                  0.0           5009
Order Date     datetime64[us]           0                  0.0           1237
Ship Date      datetime64[us]           0                  0.0           1334
Ship Mode                 str           0                  0.0              4
Customer ID               str           0                  0.0            793
Customer Name             str           0                  0.0            793
Segment                   str           0                  0.0              3
Country                   str           0                  0.0              1
City                      str           0                  0.0            531
State                     str           0                  0.0             49
Postal Code             int64           0                  0.0            631
Region                    str           0                  0.0              4
Product ID                str           0                  0.0           1862
Category                  str           0                  0.0              3
Sub-Category              str           0                  0.0             17
Product Name              str           0                  0.0           1850
Sales                 float64           0                  0.0           6144
Quantity                int64           0                  0.0             14
Discount              float64           0                  0.0             12
Profit                float64           0                  0.0           7545

Data Cleaning Workflow1. Handling Missing & Duplicate DataMissing Values: No null values were detected across the primary features.Duplicates: Exact duplicate records were checked and 0 duplicate rows were found.2. Data Type Casting & StandardizationPostal Code: Cast from numeric int64 to a 5-digit zero-padded string (zfill(5)) to preserve valid U.S. ZIP code formatting with leading zeros (e.g., 01841).IDs: Explicitly cast Customer ID and Order ID to string objects.3. Categorical Text NormalizationApplied .strip() and .title() transformation across all categorical attributes (Ship Mode, Segment, Country, City, State, Region, Category, Sub-Category) to remove trailing whitespace and standardize letter casing.4. Outlier Analysis (IQR Method)Using the Interquartile Range ($1.5 \times \text{IQR}$) rule:Sales: 1,167 potential outliersProfit: 1,881 potential outliersDiscount: 856 potential outliersQuantity: 170 potential outliers[cite: 2]