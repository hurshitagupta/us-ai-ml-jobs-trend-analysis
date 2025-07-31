# US AI/ML Jobs Trend Analysis

A comprehensive analysis of real-world Artificial Intelligence and Machine Learning job postings across the United States (2022–2024) using data scraped from LinkedIn and sourced via Kaggle.

---

## Objective

- Analyze AI/ML hiring trends in the US job market.
- Understand prevalent job roles, locations, experience requirements, and industry distribution.
- Provide actionable insights for job seekers and analysts into the evolving AI/ML market.

---

## Dataset

- **Source:** Kaggle  
- **Dataset:** AI and ML Job Listings USA  
- **File Used:** `ai_ml_jobs_linkedin.csv`  
- **Rows:** 862  
- **Columns:** 10  
- **Description:** The dataset contains AI/ML job postings scraped from LinkedIn across various US locations from 2022 to 2024.

---

## Project Structure

| **Version** | **Description**                                                       |
|-------------|----------------------------------------------------------------------|
| **v1**      | Load and preview data (columns, types, initial checks)               |
| **v2**      | Data cleaning and formatting                                         |
| **v3**      | Exploratory data analysis (EDA)                                      |
| **v4**      | Visual analysis (plots, charts)                                      |
| **v5**      | Insights and interpretations                                         |
| **v6**      | Trend analysis (time/location/sector-based)                         |
| **v7**      | Optional modeling (salary inference, role clustering)                |
| **v8**      | Final summary, key takeaways, and presentation-ready output          |

---

## **Version Details**

> ### **v1: Data Loading and Preview**  
> - Loaded CSV data and verified basic structure  
> - Inspected data types, column info, and initial nulls  
> - Summarized column-wise purpose and relevance  

> ### **v2: Data Cleaning and Formatting**  
> - Selected 7 most relevant columns for analysis  
> - Cleaned `title` and `companyName` using title case  
> - Split `location` into new `city` and `state` columns  
> - Extracted year and month from `publishedAt`  
> - Dropped redundant columns post-transformation  
> - Filled missing `state` values with `"Unknown"`
> ### 🔍 **Observations**
>- **Inconsistent job title formatting**  
  _Examples: inconsistent casing, spacing_  
>- **Some locations lacked state data**  
>- **Posting activity clustered in recent years**
>### ⚠️ **Challenges**
> - Missing or malformed location values  
> - Nulls introduced during location splitting  
> - Sequence of cleanup steps affected accuracy
>### 📚 **Learnings**
>- Preprocessing brings clarity to trends  
>- Temporal and geographic splitting is powerful for grouping  
>- Consistent formatting improves downstream analysis

---

## Tech Stack

- Python  
- Pandas  
- NumPy  
- Matplotlib (for visualizations)  
- Kaggle Notebooks

---

## Author

**Hurshita Gupta**  
Data Analytics Learner  
[LinkedIn](https://www.linkedin.com/in/hurshita-gupta-998871292/)

---

> **Note:** This repository is under active development. All changes are version-controlled for transparency and reproducibility.

