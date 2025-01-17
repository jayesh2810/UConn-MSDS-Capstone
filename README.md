## Enhanced Apply Start Forecasting for Sponsored Job Posts

This repository contains the documentation for the capstone project titled "Enhanced Apply Start Forecasting for Sponsored Job Posts." Below are the key aspects of the project, outlined point-wise for clarity:

The objective was to develop a predictive solution to estimate the number of job application starts for sponsored job posts before they were live, helping advertisers make data-driven investment decisions.

Indeed required a solution to price their services fairly for clients posting jobs on their platform, aiming to optimize ROI and funnel performance for advertisers.

The dataset analyzed consisted of 3.5 million job postings with 9 columns: id, total_impressions, total_clicks, total_apply_starts, actual_title, job_state, job_city, job_salary, advertiser_name, and employee_count.

### Data challenges included:

Significant missing values in job_city and job_state.

Missing values were resolved using the Google Maps API and an NER system to extract location details from the actual_title column.

Data cleaning steps included removing unnecessary punctuation marks and dropping rows with missing values in more than four variables.

### Feature engineering highlights:

Generated embeddings for the cleaned actual_title column using the Hugging Face API.

Clustering of embeddings led to the creation of a new categorical variable, Job_sector, with six sectors such as Healthcare, Tech, and Restaurant.

Introduced the Clicks-to-Impressions Ratio variable as a measure of job ad relevance and engagement.

Word clouds were used to identify job sectors within each cluster, providing actionable insights.

### Modeling process:

Experimented with multiple algorithms, with XGBoost emerging as the final and best-performing model.

Evaluation metrics included R², MSE, and RMSE, ensuring robust performance through cross-validation.

### Key insights:

Advertiser_name, Salary, and Job_sector were the top three variables driving total_apply_starts.

Tech sector jobs offered the highest salaries among all sectors.

Remote jobs received the most applications, underscoring the growing preference for flexible work arrangements.

Due to the NDA signed for this project, code cannot be shared publicly, and therefore, the repository does not include any source code.

Tools used included Jupyter and the Hugging Face API for data preprocessing, feature engineering, and modeling.

The project outcomes were presented to stakeholders through PowerPoint presentations, as deployment was not part of the scope for this capstone project.

