# NLP-KnowledgeGraph Project

## Overview
This project focuses on analyzing the **NLP-KnowledgeGraph** dataset, sourced from Hugging Face, to perform semantic analysis, knowledge graph construction, and relation prediction. 

The dataset contains annotated textual data with the following columns: `sentence`, `source`, `target`, `relation`, `tokens`, and `tags`.  
The preprocessing phase (Phase 3) ensures the dataset is clean and standardized for downstream tasks like exploratory data analysis, visualization, and modeling.

This README provides instructions for running the preprocessing scripts and a summary of the steps taken.

---

## Prerequisites

- **Python 3.x**

### Required Libraries:
- `pandas` (for data manipulation)

### Install dependencies:
```bash
pip install pandas
```
# Preprocessing Summary

## Handle Missing Values
- No missing values were found in the dataset.
- No imputation or row removal was necessary.

## Remove Duplicates
- Duplicate rows (e.g., repeated sentences like "a fairy is a mythical creature...") were identified and removed by comparing all columns.
- Only unique records were retained to ensure unbiased analysis.

## Outliers
- As the dataset is non-numeric, outliers were assessed based on annotation consistency.
- No significant outliers were found.

## Data Transformation (Categorical Variables)
- The `relation` column was transformed from list-like strings (e.g., `['grow', 'on']`) to single strings (e.g., `"grow on"`) for consistency.
- The `tags` column was already properly structured and required no changes.

---

## Contact
For questions or issues, please contact the project team.
- shaziamughal504@gmail.com
- ayeshatahirad@gmail.com

---

