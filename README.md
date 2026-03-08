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

### 🧮 Formulas and Functions

#### 💰 Median Salary by Job Titles
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
* 🔍 Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.
* 📊 Array Formula: Utilizes MEDIAN() function with nested IF() statement to analyze an array.
* 🎯 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.
* 🔢 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified.

##### 🍽️ Background Table
<img width="265" height="220" alt="1_Salary_Dashboard_Screenshot1" src="https://github.com/user-attachments/assets/7d5d4920-21ed-4759-a3ac-70331ce0287b" />

##### 📉 Dashboard Implementation
<img width="1148" height="1214" alt="1_Salary_Dashboard_Job_Title" src="https://github.com/user-attachments/assets/fc2b9f88-4dab-4cda-a7a2-098b5b63762d" />

##### ⏰ Count of Job Schedule Type
```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```
* 🔍 Unique List Generation: This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.
* 🔢 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.
##### 🍽️ Background Table
<img width="195" height="119" alt="1_Salary_Dashboard_Screenshot2" src="https://github.com/user-attachments/assets/eaeb77a2-78e7-4f7d-afa7-dd34103a876d" />
