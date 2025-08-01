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

### **v1: Data Loading and Preview**  
> - Loaded CSV data and verified basic structure  
> - Inspected data types, column info, and initial nulls  
> - Summarized column-wise purpose and relevance  

### **v2: Data Cleaning and Formatting**  
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
### **v3: Exploratory Data Analysis (EDA)**  
> - Explored key categorical columns: `contractType`, `experienceLevel`, `companyName`, `city`, `month`, and `year`  
> - Analyzed top hiring companies, contract types, and demand distribution across experience levels  
> - Grouped columns to uncover patterns like experience level vs contract type  
> - Investigated which job types receive fewer applications despite frequent postings  
>
> ### 🔍 **Observations**
> - Full-time jobs dominate hiring volume  
> - Mid and senior experience levels are in highest demand  
> - Some contract types attract very few applications despite high posting counts  
>
> ### ⚠️ **Challenges**
> - Many companies share the lowest application count, making it hard to isolate one  
> - Several city values were generic (e.g., "United States") and needed manual fixing  
>
> ### 📚 **Learnings**
> - Even without visuals, grouped EDA can reveal powerful hiring signals  
> - Categoricals can offer strong patterns when combined thoughtfully (e.g., exp + contract type)
### **v4: Visual Exploration & Job Trend Charts**
> - Turned cleaned data into visual insights using Seaborn and Matplotlib  
> - Created 9 charts to highlight job trends that matter to both job seekers and recruiters  
> - Covered key topics: hiring companies, contract and experience trends, sector-wise demand, state-level hiring, and application volume  
> - Added geographic combo chart (company × state) to show where hiring is actually happening  
>
> ### 🔍 **Observations**
> - Hiring is concentrated among a few major companies  
> - Full-time and contract roles dominate the listings  
> - Certain states are significantly more active in job postings  
>
> ### ⚠️ **Challenges**
> - `sector` column contains long, compound values — not ideal for cross-analysis yet  
> - `applicationCount` values are mostly constant making averages unhelpful  
> - `title` data still too noisy to use effectively
>
> ### 📚 **Learnings**
> - Visuals make trends far more intuitive, especially for stakeholders  
> - Even without complex modeling, basic plots reveal what’s in demand and where  

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

