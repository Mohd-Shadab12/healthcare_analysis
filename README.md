readme_content = """
# 🏥 Healthcare Consultation Analysis

## 📌 Overview
This project focuses on analyzing hospital consultation logs to gain insights into doctor performance, consultation durations, waiting times, and revenue patterns. The dataset undergoes comprehensive preprocessing, is stored in a MySQL database, and is analyzed using Python with SQL queries and insightful visualizations.

## 🎯 Objectives
- Clean and preprocess raw hospital consultation log data.
- Calculate and analyze time-based metrics like consultation and waiting durations.
- Extract and visualize revenue trends and doctor performance.
- Store and query data in a MySQL database using SQLAlchemy.
- Generate visual insights using Python libraries like Seaborn and Matplotlib.

## 🧠 Key Features
- Column name normalization and type conversion.
- Cleaning and conversion of time and revenue fields.
- Creation of new time-based metrics (e.g., Consultation Duration, Waiting Time).
- Handling missing values for reliable analysis.
- SQL queries to summarize doctor performance metrics.
- Data visualization for trends and distribution analysis.

## 🗃️ Dataset Highlights
- **Entry_Time**, **Post-Consultation_Time**, **Completion_Time**: Used to calculate durations.
- **Consultation_Revenue**, **Medication_Revenue**, **Lab_Cost**: Revenue-related fields cleaned and analyzed.
- **Doctor_Type**: Used for grouping and performance comparison.
- **Date**: Converted to proper datetime format.

## 🧪 Process Workflow

### 1. **Data Cleaning & Transformation**
- Standardized column names (snake_case).
- Converted `Date` to datetime and time columns to timedelta.
- Cleaned revenue columns (removed `$`, `-`, and nulls).
- Derived new features:
  - **Total_Consultation_Time**
  - **Waiting_Time**
  - **Consultation_Duration**
- Converted timedelta features to seconds for MySQL compatibility.
- Removed all rows with missing values.

### 2. **MySQL Integration**
- Used `SQLAlchemy` to upload cleaned data to a MySQL table: `healthcare_records`.
- Executed SQL queries to calculate:
  - **Average Consultation Duration by Doctor Type**
  - **Doctor Consultation Summary**: total consultations, average, min, and max durations.

### 3. **Visualization**
- **Distribution Plot** of Consultation Durations (in minutes).
- **Bar Chart** for number of consultations grouped by Doctor Type.

## 🛠️ Tech Stack
**Languages & Libraries**:
- Python (Pandas, Seaborn, Matplotlib)
- SQL (MySQL)
- SQLAlchemy

**Tools**:
- Jupyter Notebook
- MySQL Server

## 📊 Sample Insights
- Consultation durations show a positively skewed distribution with outliers.
- Significant variation observed in doctor performance based on consultation durations.
- Count of consultations varies across doctor types, indicating possible operational imbalances.

## Thanks

