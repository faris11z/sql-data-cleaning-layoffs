# SQL Data Cleaning Project – Layoffs 2022 Dataset

## Description
This project focuses on cleaning and standardizing the 2022 Layoffs dataset using MySQL. The main goal was to prepare an analysis-ready dataset by removing duplicates, standardizing columns, handling null and blank values, and ensuring proper data types.

This project was inspired by Alex the Analyst’s bootcamp: [YouTube Link](https://youtu.be/4UltKCnnnTA?si=uRxaL7L3iJFBUMyC).

## Dataset
- Source: [Kaggle – Layoffs 2022](https://www.kaggle.com/datasets/swaptr/layoffs-2022)
- Format: CSV

## Tools Used
- MySQL
- SQL functions & concepts:
  - `ROW_NUMBER()` and `PARTITION BY` (for duplicate detection)
  - `TRIM()`, `STR_TO_DATE()`
  - `UPDATE`, `DELETE`, `ALTER TABLE`
  - CTEs for temporary calculations

## Project Steps
1. **Create a staging table** to protect the original dataset.  
2. **Remove duplicate records** using `ROW_NUMBER()` and staging tables.  
3. **Standardize data**:
   - Trim extra spaces from strings  
   - Correct inconsistent industry names  
   - Remove trailing dots in country names  
   - Convert string dates to proper DATE type  
4. **Handle null or blank values**:
   - Convert empty strings to NULL  
   - Fill missing industry values from other rows of the same company  
5. **Final cleanup**:
   - Delete rows with missing layoff counts  
   - Drop helper columns (`row_num`) used for cleaning  
6. **Dataset is ready for analysis or visualization**

## Learning Outcomes
- Learned safe data cleaning techniques in MySQL without altering original data.  
- Practiced using `ROW_NUMBER()` for duplicate detection and handling null/blank values.  
- Gained experience in preparing datasets for analysis and reporting.  
