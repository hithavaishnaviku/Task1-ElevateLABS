# 📊 Netflix Titles Dataset - Data Cleaning and Preprocessing

This repository contains the data cleaning and preprocessing steps performed on the **Netflix Titles dataset** as part of an internship task. The primary objective was to clean and prepare the dataset for further data analysis and visualization by addressing missing values, ensuring consistent formatting, and restructuring key columns.

---

## 📁 Dataset Overview

The original dataset is sourced from [Netflix's public data](https://www.kaggle.com/datasets/shivamb/netflix-shows) and contains metadata about TV shows and movies available on Netflix.

- **Original Dataset Shape:** 8807 rows × 12 columns
- **Cleaned Dataset Shape:** 5332 rows × 14 columns

---

## 🔧 Steps Performed

### 1. Handling Missing Values
- Removed rows with missing values in **critical fields**:
  - `director`
  - `cast`
  - `country`
  - `date_added`
  - `rating`
  - `duration`

### 2. Removing Duplicates
- Checked and removed exact duplicate records from the dataset.

### 3. Standardizing Column Names
- Converted all column names to lowercase.
- Replaced spaces with underscores for consistency and compatibility.

### 4. Date Format Standardization
- Transformed the `date_added` column to proper `datetime` format for time-based analysis.

### 5. Splitting the `duration` Column
- Split the `duration` column into:
  - `duration_int` (numeric part, e.g., `90`)
  - `duration_unit` (unit of time, e.g., `"min"` or `"Seasons"`)

### 6. Data Type Fixes
- Ensured the following data types:
  - `release_year`: `int`
  - `duration_int`: `int`
  - `date_added`: `datetime`

---

## 🧾 Final Dataset Summary

### ✅ Final Columns
| Column Name     | Description |
|-----------------|-------------|
| `show_id`       | Unique identifier for each show |
| `type`          | Movie or TV Show |
| `title`         | Title of the show |
| `director`      | Director of the show |
| `cast`          | Cast involved in the show |
| `country`       | Country of production |
| `date_added`    | Date added to Netflix (datetime format) |
| `release_year`  | Year of release |
| `rating`        | Age rating |
| `duration`      | Original duration column (string) |
| `listed_in`     | Genre(s) |
| `description`   | Short description |
| `duration_int`  | Numeric value extracted from duration |
| `duration_unit` | Unit extracted from duration (e.g., "min", "Seasons") |

---

## 📂 Repository Structure

