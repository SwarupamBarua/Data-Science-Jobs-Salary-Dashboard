# Data Science Jobs Salary Dashboard
![1_Salary_Dashboard_Final_Dashboard](https://github.com/user-attachments/assets/c7781c98-e567-40dc-9d8a-c78c7fd1c218)
## Introduction
This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.

The data is from my Excel course, which provides a foundation in analyzing data using this powerful tool. The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.

### Dashboard File

My final dashboard is in [Data_Science_Salary_Dashboard_2026](https://github.com/SwarupamBarua/Data-Science-Jobs-Salary-Dashboard/blob/main/Data_Science_Salary_Dashboard_2026.xlsx)

### Excel Skills Used

The following Excel skills were utilized for analysis:

* 📉 Charts
* 🧮 Formulas and Functions
* ❎ Data Validation

### Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023. The dataset is available via my Excel course, which provides a foundation for analyzing data using Excel. It includes detailed information on:

* 👨‍💼 Job titles
* 💰 Salaries
* 📍 Locations
* 🛠️ Skills

## Dashboard Build

### 📉 Charts

#### 📊 Data Science Job Salaries - Bar Chart
<img width="1336" height="867" alt="1_Salary_Dashboard_Chart1" src="https://github.com/user-attachments/assets/3528efde-657e-4418-8a24-60da636f3a4e" />
* 🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
* 🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.
* 📉 Data Organization: Sorted job titles by descending salary for improved readability.
* 💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

#### 🗺️ Country Median Salaries - Map Chart
![1_Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/82fc41b8-0206-4dee-807e-737d3348dc95)
* 🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
* 🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.
* 📊 Data Representation: Plotted median salary for each country with available data.
* 👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
* 💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.

## 🧮 Formulas and Functions

### 💰 Median Salary by Job Titles
```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

