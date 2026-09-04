# Hospital-patient-data-analysis
Data analytics project showcasing Hospital patient data analysis using Python, SQL, Power BI

📌 Overview

This project focuses on analyzing hospital patient data to identify patterns in patient demographics, medical conditions, hospital admissions, treatment, length of stay, and billing.

The project demonstrates an end-to-end data analytics workflow, starting from data loading and exploratory analysis in Python, followed by data cleaning, SQL-based analysis, and interactive visualization using Power BI.

🎯 Project Objectives
Understand patient demographics and healthcare patterns
Clean and prepare raw healthcare data for analysis
Perform Exploratory Data Analysis (EDA) using Python
Analyze healthcare data using SQL
Identify trends in medical conditions, admissions, billing, and hospital performance
Build an interactive Power BI dashboard
Generate a business-focused analytical report
Present actionable insights in a recruiter-friendly portfolio project
📂 Dataset

The dataset contains hospital patient-level information, including:

Column	Description
Name	Patient name
Age	Patient age
Gender	Patient gender
Blood Type	Patient blood group
Medical Condition	Primary medical condition
Date of Admission	Hospital admission date
Doctor	Assigned doctor
Hospital	Hospital name
Insurance Provider	Patient's insurance provider
Billing Amount	Patient billing amount
Room Number	Assigned room
Admission Type	Emergency, Urgent, or Elective
Discharge Date	Patient discharge date
Medication	Medication provided
Test Results	Patient test result

Note: The dataset is used for educational and portfolio purposes.

🛠️ Tools & Technologies
Python
Pandas
NumPy
Matplotlib
Seaborn
SQL
PostgreSQL / MySQL / SQL Server
Power BI
Power Query
DAX
Interactive dashboards
Excel/CSV – Data source
Git & GitHub – Project version control and documentation
🔄 Project Workflow
Raw Dataset
     ↓
Python Data Loading
     ↓
Data Cleaning & Preprocessing
     ↓
Exploratory Data Analysis
     ↓
SQL Database
     ↓
SQL Analysis & Business Queries
     ↓
Power BI Data Modeling
     ↓
Power BI Dashboard
     ↓
Insights & Analytical Report
🐍 1. Data Loading & EDA

The dataset was initially loaded into Python using Pandas.

Key EDA activities
Dataset structure and dimensions
Data types
Missing-value analysis
Duplicate-value analysis
Descriptive statistics
Distribution analysis
Categorical-value analysis
Outlier identification
Correlation analysis
Patient demographic analysis
Medical condition analysis
Billing analysis

Example:

import pandas as pd

df = pd.read_csv("healthcare_dataset.csv")

df.head()
df.info()
df.describe()
df.isnull().sum()
df.duplicated().sum()
🧹 2. Data Cleaning

The raw dataset was cleaned and prepared for further analysis.

Cleaning activities
Removed duplicate records
Handled missing values
Standardized categorical values
Corrected data types
Converted admission and discharge dates
Checked numerical columns for invalid values
Identified and handled potential outliers
Created calculated fields such as Length of Stay
Length of Stay
Length of Stay = Discharge Date - Date of Admission

The cleaned dataset was then prepared for SQL analysis and Power BI visualization.

🗄️ 3. SQL Analysis

The cleaned data was loaded into a relational database such as:

PostgreSQL
MySQL
SQL Server

SQL was used to answer important healthcare business questions.

Example Analysis

Total number of patients

SELECT COUNT(*) AS total_patients
FROM healthcare;

Average billing amount by medical condition

SELECT
    medical_condition,
    AVG(billing_amount) AS avg_billing
FROM healthcare
GROUP BY medical_condition
ORDER BY avg_billing DESC;

Patient count by admission type

SELECT
    admission_type,
    COUNT(*) AS patient_count
FROM healthcare
GROUP BY admission_type;

Hospital-wise patient count

SELECT
    hospital,
    COUNT(*) AS patient_count
FROM healthcare
GROUP BY hospital
ORDER BY patient_count DESC;

Average length of stay by medical condition

SELECT
    medical_condition,
    AVG(length_of_stay) AS avg_stay
FROM healthcare
GROUP BY medical_condition
ORDER BY avg_stay DESC;
📊 4. Power BI Dashboard

An interactive Hospital Patient Data Analysis Dashboard was developed using Power BI.

Key KPIs
👥 Total Patients
💰 Average Billing
🛏️ Average Length of Stay
Dashboard Visualizations
Patient count by age group
Patient distribution by gender
Average billing by medical condition
Admission type distribution
Hospital performance
Medical condition analysis
Interactive Filters

Users can filter the dashboard by:

Gender
Medical Condition
Hospital
Admission Type

The dashboard enables users to explore patient and hospital trends interactively.

💡 Key Results & Insights

The analysis provides insights into:

Overall patient volume and demographics
Distribution of patients across different age groups
Most frequently occurring medical conditions
Average billing across medical conditions
Average patient length of stay
Distribution of Emergency, Urgent, and Elective admissions
Hospital-wise patient volume
Differences in healthcare costs across hospitals and conditions
Example Dashboard KPIs
KPI	Result
Total Patients	55.5K
Average Billing	$25.54K
Average Stay	15.51 Days

These values are based on the current dashboard and may change if the dataset is modified or additional cleaning is applied.

📁 Project Structure
Hospital-Patient-Data-Analysis/
│
├── data/
│   └── healthcare_dataset.csv
│
├── python/
│   └── healthcare_eda.ipynb
│
├── sql/
│   └── healthcare_analysis.sql
│
├── powerbi/
│   └── hospital_patient_dashboard.pbix
│
├── report/
│   └── healthcare_analysis_report.pdf
│
├── images/
│   └── dashboard.png
│
└── README.md
