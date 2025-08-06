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
- **Description:** Contains AI/ML job postings scraped from LinkedIn across various US locations from 2022 to 2024.

---

## Project Structure

| Version | Description                                                        |
|---------|--------------------------------------------------------------------|
| v1      | Load and preview data (columns, types, initial checks)             |
| v2      | Data cleaning and formatting                                       |
| v3      | Exploratory data analysis (EDA)                                    |
| v4      | Visual analysis (plots, charts)                                    |
| v5      | Title and sector exploration                                       |
| v6      | Role-wise competition, experience-level hiring focus, and demand-supply mismatch insights |

---

## Version Details

### v1: Data Loading and Preview
- Loaded CSV data and verified basic structure.
- Inspected data types, column info, and initial nulls.
- Summarized column-wise purpose and relevance.

---

### v2: Data Cleaning and Formatting
- Selected 7 most relevant columns for analysis.
- Cleaned `title` and `companyName` using title case.
- Split `location` into new `city` and `state` columns.
- Extracted year and month from `publishedAt`.
- Dropped redundant columns post-transformation.
- Filled missing state values with "Unknown".

#### 🔍 Observations:
- Inconsistent job title formatting (casing, spacing).
- Some locations lacked state data.
- Posting activity clustered in recent years.

#### ⚠️ Challenges:
- Missing or malformed location values.
- Nulls introduced during location splitting.
- Sequence of cleanup steps affected accuracy.

#### 📚 Learnings:
- Preprocessing brings clarity to trends.
- Temporal and geographic splitting is powerful for grouping.
- Consistent formatting improves downstream analysis.

---

### v3: Exploratory Data Analysis (EDA)
- Explored key categorical columns: `contractType`, `experienceLevel`, `companyName`, `city`, `month`, `year`.
- Analyzed top hiring companies, contract types, and experience-level demand.
- Grouped columns to uncover patterns like experience level vs contract type.
- Investigated which job types receive fewer applications despite frequent postings.

#### 🔍 Observations:
- Full-time jobs dominate hiring volume.
- Mid and senior experience levels are in highest demand.
- Some contract types attract very few applications despite high posting counts.

#### ⚠️ Challenges:
- Many companies share the lowest application count, making it hard to isolate one.
- Several city values were generic (e.g., "United States") and needed manual fixing.

#### 📚 Learnings:
- Even without visuals, grouped EDA can reveal powerful signals.
- Categorical grouping (e.g., exp + contract type) yields strong patterns.

---

### v4: Visual Exploration & Job Trend Charts
- Turned cleaned data into visual insights using Seaborn and Matplotlib.
- Created 9 charts to highlight key job trends.
- Topics: hiring companies, contract & experience trends, sector-wise demand, state-level hiring, and application volume.
- Added company × state combo chart to show hiring geography.

#### 🔍 Observations:
- Hiring is concentrated among a few large companies.
- Full-time and contract roles dominate.
- Certain states have much higher posting activity.

#### ⚠️ Challenges:
- `sector` column values are long/compound — tricky for analysis.
- `applicationCount` values mostly constant; averages unhelpful.
- `title` data still too noisy to use effectively.

#### 📚 Learnings:
- Visuals make trends intuitive, especially for stakeholders.
- Even simple plots reveal high-impact demand locations and roles.

---

### v5: Role & Sector Cleanup + Focused Visualizations
- Cleaned and standardized `title` and `sector`.
- Added new column `cleanedSector` (14 categories) and categorized titles into broad job roles.
- Plotted top job titles, sector-wise hiring, and sector vs title heatmap.

#### 🔍 Observations:
- Machine Learning Engineer, Data Scientist, and AI/ML Engineer are most in demand.
- Tech and Consulting sectors dominate.
- Roles are sector-specific: tech dominates, especially for AI/ML jobs.

#### ⚠️ Challenges:
- Raw titles were inconsistent, mixing roles/levels/buzzwords.
- Sector names duplicated, required manual grouping.
- Visuals cluttered with too many categories — filtering key.

#### 📚 Learnings:
- Cleaning categorical text fields unlocks insights.
- Focused visualizations (top 5×5 heatmaps) outperform data overload.
- Investment in data prep pays off in analysis clarity.

---

### v6: Experience Level, Role Demand, and Competition Analysis
- Explored hiring pressure: job counts, application counts, experience per role.
- Compared job openings vs applications to spot supply-demand mismatch.
- Built three Seaborn visualizations:
  - Experience level split for top roles.
  - Avg applications per role.
  - Comparison: job count vs avg application per role.

#### 🔍 Observations:
- Hiring focused on Mid-senior and Entry-level.
- Roles like Intern and Software Engineer (AI/ML) attract many applications (less openings).
- MLOps and Deep Learning Engineer: under-applied-to, but high demand — hidden gems.
- Clear mismatch between company needs and applicant focus.

#### ⚠️ Challenges:
- Crowded data made visuals tough — filtering/mapping essential.

#### 📚 Learnings:
- Competition insights (application pressure) matter as much as demand.
- Layered plots (job count + avg applications) deepen understanding.

---

## 📦 Project Wrap-Up

This project is structured over six versions — each clarifying and deepening the analysis of real-world data. From messy text fields to role-level conclusions, the process honed my skills in asking better questions and "listening" to data.

**Notebook is version-controlled, fully commented, and includes insights at each stage. Hosted on Kaggle and synced to GitHub for transparency.**

---

## Tech Stack

- Python  
- Pandas  
- NumPy  
- Seaborn & Matplotlib (for visualizations)  
- Kaggle Notebooks  

---

## Author

Hurshita Gupta  
Data Analytics Learner  
[LinkedIn](https://www.linkedin.com/in/hurshita-gupta-998871292/)

---

> _Note: This repository is version-controlled. All progress is documented across v1–v6._
