# celebal_assignment_week1
# Data Cleaning and Feature Engineering Assignment

## Project Overview
This project focuses on executing end-to-end data pre-processing, handling missing records, validating duplicates, and engineering derived columns on a retail product dataset. The goal is to clean a raw collection of 1,000 product rows into a structured, audit-ready format optimized for downstream analysis or machine learning applications.

---

## Dataset Characteristics

### 1. Raw Dataset (`Combined_dataset.csv`)
* **Initial Dimensions:** 1,000 rows × 24 columns
* **Target Schema:** Product identifiers, metadata text (`title`, `product_description`), ratings, prices, category markers, and descriptive attributes.

### 2. Final Processed Dataset (`cleaned_dataset.csv`)
* **Final Dimensions:** 1,000 rows × 26 columns
* **Target Schema:** Contains all original variables along with two newly structured feature columns (`quantity`, `total_amount`).

---

## Pipeline & Applied Data Operations

### Step 1: Structural Audit & Duplication Verification
* The initial structure was parsed utilizing `df.shape` and structural metadata summaries were produced via `df.info()`.
* Row uniqueness validation was completed by executing:
  ```python
  df.duplicated().sum()
