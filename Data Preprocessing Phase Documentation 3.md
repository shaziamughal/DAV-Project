# Phase 3: Data Preprocessing Report
**Dataset**: NLP Knowledge Graph Dataset

---

## Handle Missing Values
- The dataset was thoroughly inspected for missing values across all columns (`sentence`, `source`, `target`, `relation`, `tokens`, and `tags`).
- **Result**: No missing values were found.
- **Impact**: All records are complete and can be utilized for subsequent analysis without data loss.

---

## Remove Duplicates
- Duplicate records were identified, such as the sentence:
  > "a fairy is a mythical creature of folklore and mystery dressed the colors of summer."
- Duplicates were removed by comparing all columns and retaining only unique entries.
- **Impact**: Prevents overrepresentation of certain records, ensuring unbiased frequency-based analyses and improving the accuracy of visualization and modeling.

---

## Outliers Detection and Handling
- **Challenge**: The dataset is entirely textual and non-numeric.
- Traditional numeric outlier detection methods (e.g., z-scores, IQR) are not applicable.
- **Approach**: Outliers were considered as unusual or inconsistent annotations.
- Manual inspection revealed no significant outliers that could impact analysis.
- **Action**: No specific handling was needed; the dataset was deemed suitable for further processing.

---

## Data Transformation (Categorical Variables)
- **Relation Column**:
  - Multi-word phrases (e.g., `['grow', 'on']`) were transformed into single strings (e.g., `"grow on"`) for consistency.
- **Tags Column**:
  - Already structured with labels like `SRC`, `TGT`, and `REL`.
  - No further transformation required.

- **Impact**: 
  - Standardizes categorical data.
  - Facilitates subsequent tasks like knowledge graph construction and relation prediction.

---

## Document Process
- Preprocessing focused on:
  - Ensuring data quality.
  - Addressing redundancy through deduplication.
  - Adapting outlier handling for textual data.
  - Standardizing categorical variables.
- **Outcome**:
  - Dataset is clean, consistent, and ready for exploratory analysis, visualization, and modeling in subsequent project phases.

---
