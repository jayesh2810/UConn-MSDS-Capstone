# Enhanced Apply Start Forecasting for Sponsored Job Posts

This repository contains the documentation for the capstone project titled **"Enhanced Apply Start Forecasting for Sponsored Job Posts."** Below are the key aspects of the project, outlined point-wise for clarity:

## Objective
- Develop a predictive solution to estimate the number of job application starts for sponsored job posts before they go live.
- Help advertisers make data-driven investment decisions.

## Context
- Indeed required a solution to price their services fairly for clients posting jobs on their platform.
- The project aimed to optimize ROI and funnel performance for advertisers.

## Dataset
- **Size**: 3.5 million job postings.
- **Columns**:
  - `id`, `total_impressions`, `total_clicks`, `total_apply_starts`, `actual_title`, `job_state`, `job_city`, `job_salary`, `advertiser_name`, `employee_count`.

## Data Challenges
- **Missing Values**:
  - Significant missing data in `job_city` and `job_state`.
  - Resolved using the Google Maps API and NER system to extract location details from the `actual_title` column.
- **Data Cleaning**:
  - Removed unnecessary punctuation marks.
  - Dropped rows with missing values in more than four variables.

## Feature Engineering
- Generated embeddings for the cleaned `actual_title` column using the Hugging Face API.
- Clustered embeddings to create a new categorical variable, `Job_sector`, with six sectors (e.g., Healthcare, Tech, Restaurant).
- Introduced the `Clicks-to-Impressions Ratio` variable to measure job ad relevance and engagement.
- Used word clouds to identify job sectors within clusters, providing actionable insights.

## Modeling
- Experimented with multiple algorithms, with XGBoost emerging as the best-performing model.
- **Evaluation Metrics**: R², MSE, and RMSE.
- Ensured robust performance using cross-validation.

## Key Insights
- **Influential Variables**: `Advertiser_name`, `Salary`, and `Job_sector` were the top three drivers of `total_apply_starts`.
- **Sector Analysis**: Tech sector jobs offered the highest salaries.
- **Remote Work Trend**: Remote jobs attracted the highest number of applications, highlighting the growing preference for flexible work arrangements.

## Tools and Technologies
- Jupyter and Hugging Face API for data preprocessing, feature engineering, and modeling.

## Limitations
- **NDA Restriction**: Due to the NDA, source code cannot be shared publicly.
- Deployment was not part of the project; results were shared via PowerPoint presentations.

## Repository Structure
- **reports/**: Presentation slides shared with stakeholders.
- **README.md**: Project overview and documentation.
