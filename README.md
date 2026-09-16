# customer_behaviour_analysis
Data analystics project showcasing customer behaviour analysis using python sql and power Bi.

📌 Project Overview

This project demonstrates an end-to-end data analytics workflow, starting from raw dataset ingestion and data exploration to SQL-based analysis, interactive dashboard development, and business reporting.

The project uses Python, MySQL, and Power BI to transform raw data into meaningful insights and actionable business information.

🔄 Project Workflow
Raw Dataset
     │
     ▼
Load Data using Python
     │
     ▼
Exploratory Data Analysis (EDA)
     │
     ▼
Data Cleaning & Preprocessing
     │
     ▼
Load Cleaned Data into MySQL
     │
     ▼
SQL Queries & Data Analysis
     │
     ▼
Power BI Dashboard
     │
     ▼
Analytical Report
     │
     ▼
Business Insights & Recommendations
🎯 Project Objectives

The main objectives of this project are to:

Load and understand a raw dataset using Python.
Perform Exploratory Data Analysis (EDA) to identify patterns, trends, and anomalies.
Clean and preprocess the data for further analysis.
Store and analyze the cleaned dataset using MySQL.
Write SQL queries to extract meaningful business insights.
Build an interactive Power BI dashboard.
Create a comprehensive analytical report summarizing findings and insights.
Demonstrate an end-to-end data analytics workflow using industry-relevant tools.
🛠️ Tools & Technologies
Tool / Technology	Purpose
Python	Data loading, analysis, and preprocessing
Pandas	Data manipulation and transformation
NumPy	Numerical operations
Matplotlib	Data visualization
Seaborn	Statistical visualization
Jupyter Notebook	Data analysis and EDA
MySQL	Data storage and SQL analysis
SQL	Data querying and business analysis
Power BI	Interactive dashboard and visualization
Microsoft Excel	Supporting data inspection/analysis, if applicable
📂 Project Structure
data-analytics-project/
│
├── data/
│   ├── raw/
│   │   └── dataset.csv
│   │
│   └── cleaned/
│       └── cleaned_dataset.csv
│
├── python/
│   └── data_analysis.ipynb
│
├── sql/
│   └── analysis_queries.sql
│
├── powerbi/
│   └── analytics_dashboard.pbix
│
├── report/
│   └── analytical_report.pdf
│
├── images/
│   ├── dashboard.png
│   └── analysis.png
│
└── README.md
🔍 Project Methodology
1. 📥 Data Loading

The raw dataset is loaded into Python using Pandas.

The initial stage includes:

Importing the dataset.
Inspecting the number of rows and columns.
Understanding column names and data types.
Checking the first and last few records.
Identifying categorical and numerical variables.

Example:

import pandas as pd

df = pd.read_csv("data/raw/dataset.csv")

print(df.head())
print(df.shape)
print(df.info())
2. 📊 Exploratory Data Analysis (EDA)

Exploratory Data Analysis is performed to understand the structure and characteristics of the dataset.

The analysis includes:

Descriptive statistics.
Distribution analysis.
Missing-value analysis.
Duplicate-value analysis.
Outlier detection.
Correlation analysis.
Univariate analysis.
Bivariate analysis.
Multivariate analysis.
Identification of important trends and patterns.

Example:

# Statistical summary
df.describe()

# Missing values
df.isnull().sum()

# Duplicate records
df.duplicated().sum()
📈 Data Visualization

Visualizations are created using Matplotlib and Seaborn to better understand the data.

Common visualizations include:

Bar charts
Histograms
Box plots
Scatter plots
Line charts
Heatmaps
Count plots
3. 🧹 Data Cleaning & Preprocessing

The raw dataset is cleaned and prepared for analysis.

The data-cleaning process includes:

Handling missing values.
Removing duplicate records.
Correcting inconsistent values.
Converting data types.
Standardizing categorical values.
Handling outliers where appropriate.
Renaming columns for consistency.
Creating derived/calculated columns.
Validating the final dataset.

Example:

# Remove duplicates
df = df.drop_duplicates()

# Convert date column
df["Date"] = pd.to_datetime(df["Date"])

# Handle missing values
df["Sales"] = df["Sales"].fillna(0)

The cleaned dataset is then exported for further analysis.

df.to_csv("data/cleaned/cleaned_dataset.csv", index=False)
🗄️ 4. MySQL Data Analysis

The cleaned dataset is imported into MySQL for structured querying and analysis.

SQL is used to answer business-related questions and extract meaningful insights from the data.

SQL Analysis Includes
Filtering and sorting data.
Aggregations using SUM(), AVG(), COUNT(), MIN(), and MAX().
GROUP BY analysis.
HAVING conditions.
Joins between tables.
Subqueries.
Common Table Expressions (CTEs).
Window functions.
Date-based analysis.
Ranking and segmentation.

Example:

SELECT
    Category,
    SUM(Sales) AS Total_Sales
FROM sales_data
GROUP BY Category
ORDER BY Total_Sales DESC;

SQL queries used for the analysis are available in:

sql/analysis_queries.sql
📊 5. Power BI Dashboard

The analyzed data is used to create an interactive Power BI dashboard.

The dashboard provides a visual overview of important business metrics, trends, and performance indicators.

Dashboard Components

Depending on the dataset, the dashboard may include:

Key Performance Indicators (KPIs)
Total Sales / Revenue
Total Profit
Total Customers
Total Orders
Average Order Value
Category performance
Regional performance
Monthly/Yearly trends
Top-performing products
Customer segmentation
Interactive filters and slicers
Dashboard Features
Interactive charts and graphs.
KPI cards.
Slicers and filters.
Drill-down analysis.
Trend analysis.
Category and regional comparisons.
Dynamic reporting.

The Power BI dashboard file is available in:

powerbi/analytics_dashboard.pbix
🖼️ Dashboard Preview

Add a screenshot of your dashboard here:

images/dashboard.png

Example Markdown:

![Power BI Dashboard](images/dashboard.png)
📑 6. Analytical Report

A detailed report is created to document the complete analysis and findings.

The report includes:

Executive Summary

A high-level overview of the project and its key findings.

Data Overview

Description of the dataset, variables, and data sources.

Data Cleaning

Explanation of the preprocessing and cleaning steps performed.

Exploratory Data Analysis

Key patterns, distributions, relationships, and trends discovered during EDA.

SQL Analysis

Important business questions answered using MySQL queries.

Power BI Dashboard

Explanation of the dashboard, KPIs, visualizations, and filters.

Key Insights

Summary of the most important findings from the analysis.

Recommendations

Data-driven recommendations based on the identified patterns and findings.

The final report is available in:

report/analytical_report.pdf
💡 Key Insights

The analysis is designed to identify insights such as:

Overall business performance and trends.
Top and bottom-performing categories or products.
Customer behavior and purchasing patterns.
Regional performance differences.
Changes in performance over time.
Factors associated with higher or lower performance.
Opportunities for improvement.

Note: Replace this section with the actual insights discovered from your dataset.

📌 Key Deliverables
Deliverable	Description
🐍 Python Notebook	Data loading, EDA, and data cleaning
🗄️ SQL Scripts	MySQL queries and analysis
📊 Power BI Dashboard	Interactive business dashboard
📑 Analytical Report	Detailed findings and recommendations
📁 Cleaned Dataset	Analysis-ready dataset
🚀 How to Run the Project
Step 1 — Clone the Repository
git clone <your-repository-url>
cd data-analytics-project
Step 2 — Install Python Dependencies
pip install pandas numpy matplotlib seaborn jupyter
Step 3 — Run the Python Notebook

Start Jupyter Notebook:

jupyter notebook

Open:

python/data_analysis.ipynb

Run the notebook sequentially to perform the data loading, EDA, and cleaning processes.

Step 4 — Set Up MySQL

Create a database in MySQL:

CREATE DATABASE analytics_project;

Import the cleaned dataset into the appropriate table.

Then execute the queries available in:

sql/analysis_queries.sql
Step 5 — Open the Power BI Dashboard

Open:

powerbi/analytics_dashboard.pbix

Update the data source/credentials if required and refresh the dataset.

🧰 Skills Demonstrated

This project demonstrates practical experience in:

Data Analysis
Data Cleaning
Exploratory Data Analysis
Data Visualization
Python
Pandas
NumPy
SQL
MySQL
Power BI
Dashboard Development
KPI Development
Business Intelligence
Data Storytelling
Business Reporting
📈 End-to-End Outcome

This project demonstrates how raw data can be transformed into meaningful business insights through a structured analytics process:

Raw Data → Python → EDA → Data Cleaning → MySQL → SQL Analysis → Power BI → Report → Business Insights

The project showcases the ability to work across multiple stages of the data analytics lifecycle and communicate analytical findings through both technical analysis and business-focused visualizations.


