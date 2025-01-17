# Enhanced Apply Start Forecasting for Sponsored Job Posts

This repository contains information about the UConn MSDS final semester capstone project focused on forecasting apply starts for sponsored job posts.

## Project Overview
- The objective was to predict the number of job application starts for sponsored job postings before they go live, helping advertisers make data-driven decisions.
- By analyzing 3.5 million job postings, the project aimed to optimize ROI and improve funnel performance for advertisers.

## Key Features
- **Data Challenges**: Addressed missing location data using Google Maps API and NER systems.
- **Feature Engineering**: Generated embeddings with Hugging Face API, introduced Clicks-to-Impressions Ratio, and categorized job postings into six sectors.
- **Modeling**: Used XGBoost as the final model, validated with cross-validation, and evaluated using R², MSE, and RMSE.
- **Insights**:
  - Top influential variables: `Advertiser_name`, `Salary`, and `Job_sector`.
  - Tech sector jobs offered the highest salaries.
  - Remote jobs attracted the highest number of applications.

## Repository Content
- **data/**: Sample datasets for demonstration purposes.
- **notebooks/**: Jupyter notebooks detailing data preprocessing, feature engineering, and model training.
- **reports/**: Presentation slides shared with stakeholders.
- **README.md**: Project overview and documentation.

> **Note:** Due to an NDA, source code cannot be shared publicly in this repository.
