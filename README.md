# Data Jobs Salary Dashboard

## Introduction
This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.

The data is sourced from real-world data science job information from 2023, providing a foundation for analyzing job titles, salaries, locations, and essential skills using Excel.

## Dashboard File
The final dashboard is located in: [Data_Science_Analysis_Dashboard.xlsx](./Data_Science_Analysis_Dashboard.xlsx)

## Excel Skills Used
The following Excel skills were utilized for analysis and visualization:
- 📉 **Charts**: Custom bar and map charts for visual data representation.
- 🧮 **Formulas and Functions**: Advanced array formulas for data aggregation.
- ❎ **Data Validation**: Ensuring data integrity and user-friendly filtering.

## Data Jobs Dataset
The dataset includes detailed information on:
- 👨‍💼 **Job titles**
- 💰 **Salaries**
- 📍 **Locations**
- 🛠️ **Skills**

Dataset file: [data_jobs.xlsx](./data_jobs.xlsx)

## Dashboard Build

### 📉 Charts
#### Data Science Job Salaries - Bar Chart
![Salary Dashboard Chart 1](./Data_Science_Analysis.png)
- **🛠️ Excel Features**: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- **🎨 Design Choice**: Horizontal bar chart for visual comparison of median salaries.
- **📉 Data Organization**: Sorted job titles by descending salary for improved readability.
- **💡 Insights Gained**: Enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

### 🧮 Formulas and Functions
#### Median Salary by Job Titles
```excel
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
- **🔍 Multi-Criteria Filtering**: Checks job title, country, schedule type, and excludes blank salaries.
- **📊 Array Formula**: Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- **🎯 Tailored Insights**: Provides specific salary information for job titles, regions, and schedule types.

#### Count of Job Schedule Type
```excel
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```
- **🔍 Unique List Generation**: Employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.
- **🔢 Formula Purpose**: Populates the table for unique job schedule types.

### ❎ Data Validation
#### Filtered List
Implementing the filtered list as a data validation rule under the Job Title, Country, and Type options ensures:
- 🎯 User input is restricted to predefined, validated schedule types.
- 🚫 Incorrect or inconsistent entries are prevented.
- 👥 Overall usability of the dashboard is enhanced.

## Conclusion
This dashboard showcases insights into salary trends across various data-related job titles. By exploring how location and job type influence salaries, users can make more informed decisions about their career paths.
