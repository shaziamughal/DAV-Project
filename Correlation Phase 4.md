# Phase 4: Correlation Analysis Report
**Dataset**: NLP Knowledge Graph Dataset

---

## Introduction
This phase aims to perform correlation analysis on the **NLP-KnowledgeGraph** dataset as per the project requirements, including calculating and visualizing a correlation matrix and identifying significant correlations.

However, since the dataset is entirely textual (columns: `sentence`, `source`, `target`, `relation`, `tokens`, and `tags`) and lacks numerical data, traditional correlation methods like Pearson correlation cannot be directly applied. 

This report outlines attempts to adapt the dataset for correlation analysis by converting textual features into numerical representations and proposes an alternative approach better suited to the dataset's nature.

---

## Attempted Correlation Analysis

### Converting Textual Data to Numerical Features

The following steps were performed:

- **Feature Extraction**:   
  - Selected the `source`, `target`, and `relation` columns.
  - Converted them into frequency-based numerical features using a bag-of-words approach.

- **Encoding**:
  - Created a pivot table to represent the frequency of source-target pairs and their associated relation frequencies.
  - The resulting matrix had:
    - Rows: Unique source entities
    - Columns: Unique target entities
    - Values: Frequency of their co-occurrence.

- **Correlation Matrix Calculation**:
  - Computed the correlation matrix using **Pearson correlation** based on the numerical frequency matrix.

- **Visualization**:
  - Visualized the correlation matrix using a **heatmap** to highlight potential relationships.

---

## Challenges and Findings

### Challenge
- The textual nature and high dimensionality (many unique `source`, `target`, and `relation` values) resulted in a **sparse matrix**.
- Many entity pairs had little or no co-occurrence.
- The correlation matrix was dominated by zeros or very weak correlations.

### Findings
- The correlation matrix showed **no significant correlations** (most values were close to 0).
- Frequency-based encoding **did not capture semantic relationships**.
- Example: 
  - Entities like "soldiers" and "security" (related via "provide") did not show a strong correlation because their co-occurrence frequency was too low relative to the dataset's diversity.

---

## Conclusion
Traditional correlation analysis is **not suitable** for this dataset because:
- It lacks structured numerical data.
- Frequency-based transformations fail to capture **semantic relationships** essential for knowledge graph construction and relation prediction.

Alternative techniques such as semantic similarity measures or graph-based analysis would be more appropriate for understanding relationships within this dataset.

---
