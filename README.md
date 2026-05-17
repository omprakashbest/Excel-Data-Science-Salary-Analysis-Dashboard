📊 Data Science Salary Dashboard

This project is an interactive Excel dashboard built to analyze salaries across various Data Science and Analytics job roles. The dashboard provides insights into salary trends based on job title, country, and employment type using real-world data science job postings.

The project demonstrates practical Excel skills used in Data Analytics workflows, including data cleaning, dynamic formulas, data validation, and dashboard visualization.



🛠️ Excel Skills Used

This project was built using several important Excel features commonly used in Data Analytics projects:

📊 Dashboard Design – Created an interactive and visually organized salary analysis dashboard.

📉 Charts & Visualizations – Used charts to compare salaries across different job roles.

🧮 Formulas & Functions – Applied advanced Excel formulas for filtering and salary calculations.

🎯 Data Validation – Added dropdown filters for better user interaction.

📂 Data Organization – Structured and cleaned raw datasets for analysis.

🔍 Dynamic Filtering – Enabled dashboard filtering by job title, country, and employment type.

📚 Dataset Information

The dataset contains real-world data science job information, including:

👨‍💼 Job Titles

💰 Average Salaries

🌍 Countries / Locations

🕒 Employment Type

🛠️ Skills & Technologies

🏢 Platforms / Sources

The dataset is organized into multiple Excel sheets for analysis and dashboard building.

📈 Dashboard Overview

The dashboard helps users analyze salary trends in the Data Science industry through interactive filtering and visualization.

Key Features:

✅ Filter salaries by Job Title

✅ Analyze salaries by Country

✅ Compare different Employment Types

✅ Interactive dropdown-based filtering

✅ Clear visual salary comparisons

📊 Dashboard Components

📉 Salary Analysis Chart

The dashboard includes salary comparison visualizations for different Data Science roles.



Features:

📌 Interactive filtering using dropdown selections

📌 Clean and professional dashboard layout

📌 Salary comparison across multiple job categories

📌 Improved readability using formatted charts and labels

Insights:

Senior-level roles generally offer higher salaries.

Engineering and Machine Learning roles tend to have higher pay compared to Analyst positions.

Salary trends vary significantly by country and employment type.

🧮 Formulas and Functions Used

Median Salary Calculation

The dashboard uses advanced Excel formulas to calculate salary insights dynamically.

=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)

Formula Purpose:

🔍 Filters data using multiple conditions

📊 Calculates median salary dynamically

🎯 Generates customized salary insights

⚡ Supports interactive dashboard filtering

Dynamic Filter Formula

=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))

Formula Purpose:

📋 Creates clean filtered dropdown lists

🚫 Removes invalid or unnecessary entries

⚡ Improves dashboard interactivity

❎ Data Validation

Data Validation was implemented to create interactive dropdown filters for:

Job Titles

Countries

Employment Types

Benefits:

✅ Prevents incorrect input

✅ Improves user experience

✅ Makes the dashboard interactive

✅ Ensures clean and consistent filtering

🚀 Project Goals

This project was created to:

Practice real-world Excel Data Analytics skills

Build an interactive dashboard project for portfolio use

Analyze salary trends in the Data Science industry

Improve data visualization and reporting skills

🎯 Conclusion

This dashboard provides meaningful insights into Data Science salary trends using Excel. It demonstrates how Excel can be used for data cleaning, analysis, visualization, and interactive dashboard creation.
