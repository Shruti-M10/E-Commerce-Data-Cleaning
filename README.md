# Project Title (Task 1):  E-Commerce Dataset Cleaning

# Week number 1 and objective.
The objective of this task is to inspect and clean an e-commerce dataset by identifying missing values, duplicate records, data type issues, and invalid values.

# Dataset description.
- The raw dataset contains 2,000 rows and 23 columns.
- The dataset includes order, customer, location, product, pricing, payment, shipping, return, and review information.
- The columns contain text and numeric data types.
- The `OrderDate` column is currently stored as text and requires date validation.
- No missing values were indicated in the displayed dataset information.
- The original dataset has not been modified during this inspection.


# Tools and libraries used.

Tools :- VS Code 

Libraries :- 

 Imports the Python libraries required for data manipulation, numerical calculations, and visualization.

- Pandas will be used to load, clean, group, and analyze the sales data.


# Key steps performed

## Missing Value Analysis 

The missing value analysis was performed on all 23 columns of the dataset.

- Total records examined: 2,000
- Total columns examined: 23
- Total missing-value cells: 0
- Missing-value percentage: 0% across all columns



## Duplicate Analysis 

The duplicate analysis identified 20 fully duplicated rows. A separate check of the `OrderID` column found 39 rows associated with 19 distinct repeated order IDs.

These results indicate that exact duplicate rows and repeated order identifiers must be investigated separately. Repeated order IDs will not automatically be treated as errors because they may represent valid transactions or repeated entries.

**Cleaning decision:** Further inspection is required before deciding how to handle the repeated order IDs. No records have been removed at this stage.

## Date and Category Consistency 

The recorded weekdays and seasons were compared with the values calculated from `OrderDate`.

- Weekday mismatches: 0
- Season mismatches: 0

All recorded weekdays match the actual weekdays calculated from the order dates. All recorded seasons match the defined meteorological seasons.



# Major Findings

1. **Missing values:** No imputation or row removal was needed because no missing values were detected.
2. **Duplicate records:** Removed 20 exact duplicate rows while preserving one copy of each record.
3. **Repeated order IDs:** Investigated separately; the repeated IDs had identical full records, so the extra copies were treated as duplicates.
4. **Date validation:** All dates were valid and fell between January 1, 2022, and February 28, 2025.
5. **Date conversion:** Converted `OrderDate` from text to datetime.
6. **Transaction amounts:** All tested total, discount, and final amounts matched their calculated values.
7. **Numeric validation:** All records passed the quantity, unit-price, discount percentage, shipping duration, and review-score checks.
8. **Categorical consistency:** No weekday or season mismatches were found.
9. **Text formatting:** No leading/trailing spaces or capitalization inconsistencies were detected in the inspected columns.
10. **Column names:** No leading/trailing spaces or duplicate column names were found.


# Folder structure

data-science-week1-assignment/
├── data/
   ├──raw/
    └─ecommerce_cleaned.csv
   └──cleaned/
    └─Ecommerce_2000.csv
├── notebooks/
    └──week1_analysis.ipynb
├── reports/
    └──final_report.pdf
├──
 README.md

 



