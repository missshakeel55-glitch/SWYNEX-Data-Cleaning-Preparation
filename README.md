# SWYNEX-Data-Cleaning-Preparation
# Amazon Data Cleaning Project

## 📌 Project Overview

This project focuses on cleaning and preparing an Amazon product dataset using Microsoft Excel.

The objective was to identify common data quality issues such as missing values, duplicate records, incorrect data types, and inconsistent or invalid values, and then prepare a cleaner dataset for further analysis.

## 📊 Dataset

The dataset contains Amazon product and customer review information, including:

* Product ID
* Product Name
* Category
* Discounted Price
* Actual Price
* Discount Percentage
* Rating
* Rating Count
* Product Description
* User Information
* Review Information
* Product and Image Links

The original dataset contains 1,465 records and 16 columns.

## 🛠️ Tool Used

**Microsoft Excel**

## 🔍 Data Cleaning Performed

### 1. Missing Values

* Identified 2 missing values in the `rating_count` column.
* The missing values were retained rather than assigning an assumed number.
* One invalid rating value was also identified and treated as missing.

### 2. Duplicate Records

* Checked the dataset for completely duplicated rows.
* No exact duplicate rows were found.
* Repeated `product_id` values were reviewed and retained because the dataset contains multiple review records for some products.

### 3. Incorrect Data Types

The following columns required data type cleaning:

* `discounted_price` — removed the ₹ symbol and commas and converted the values to numbers.
* `actual_price` — removed the ₹ symbol and commas and converted the values to numbers.
* `discount_percentage` — removed the % symbol and converted the values to numbers.
* `rating` — converted rating values to numeric format.
* `rating_count` — removed commas and converted the values to numbers.

### 4. Inconsistent / Invalid Values

* The `rating` column contained an invalid `|` value.
* The invalid value was replaced with a blank because the correct rating could not be determined.
* Unnecessary spaces in text data were checked and cleaned where required.
* Category values containing `|` were retained because the symbol is used to represent the category hierarchy in the original dataset.

## 📁 Files

### `amazon_raw.csv`

The original, unmodified dataset.

### `amazon_cleaned.csv`

The cleaned dataset after data quality checks and corrections.

## 📋 Cleaning Summary

| Issue                         | Action                             |                     |
| ----------------------------- | ---------------------------------- | ------------------- |
| Missing `rating_count` values | Retained as missing                |                     |
| Invalid `rating` value (`     | `)                                 | Replaced with blank |
| Exact duplicate rows          | None found                         |                     |
| Repeated product IDs          | Reviewed and retained              |                     |
| Currency symbols and commas   | Removed from price columns         |                     |
| Percentage symbols            | Removed from discount percentage   |                     |
| Commas in rating counts       | Removed                            |                     |
| Text spacing                  | Checked and cleaned where required |                     |

## 🎯 Learning Outcomes

This project helped me gain practical experience in:

* Data Cleaning
* Data Quality Checking
* Microsoft Excel
* Handling Missing Values
* Duplicate Detection
* Data Type Conversion
* Data Standardization
* Data Validation
* Preparing Data for Analysis

## 🚀 Project Purpose

This project was completed as a beginner-level Data Analytics project to develop practical skills in cleaning and preparing real-world data for analysis.
