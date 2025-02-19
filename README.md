# Excel Salary Dashboard
![1_Salary_Dashboard_Final_Dashboard](https://github.com/user-attachments/assets/7cc3d5d1-5f6f-431c-a23b-8d0896016a1a)

## Introduction
This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.

The data is from my Excel course, which provides a foundation for analyzing data using this powerful tool. The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.

  ### Dashboard
 My final dashboard is in 1_Salary_Dashboard.xlsx.
  
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
 ### Charts
 
📊 Data Science Job Salaries - Bar Chart
![1_Salary_Dashboard_Chart1](https://github.com/user-attachments/assets/e28db1e6-ea1b-4955-8ff3-f9069c3b0bb5)

* 🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
* 🎨 Design Choice: Horizontal bar chart for visually comparing median salaries.
* 📉 Data Organization: Sorted job titles by descending salary for improved readability.
* 💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.
 
🗺️ Country Median Salaries - Map Chart
![1_Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/c59c5f82-bca4-4aff-8a7f-6963620d712d)

* 🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
* 🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.
* 📊 Data Representation: Plotted median salary for each country with available data.
* 👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
* 💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.

## Formulas & Functions

Median Salary by Job Titles
<code>
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
</code>

* 🔍 Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.
* 📊 Array Formula: Utilizes <code>MEDIAN()</code> function with nested <code>IF()</code> statement to analyze an array.
* 🎯 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.
* 🔢 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified.

Background Table
![1_Salary_Dashboard_Screenshot1](https://github.com/user-attachments/assets/44c60401-36d3-48c6-bfbe-99d6c859d07b)
Dashboard Implementation
![1_Salary_Dashboard_Data_Validation](https://github.com/user-attachments/assets/b9c639f6-f47e-4486-9026-013768006a9e)

### Count of Job Schedule Type
<code>=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))</code>
* 🔍 Unique List Generation: This Excel formula below employs the <code>FILTER()</code> function to exclude entries containing "and" or commas, and omit zero values.

* 🔢 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.

Background Table:
![1_Salary_Dashboard_Screenshot2](https://github.com/user-attachments/assets/0075345b-6032-466d-b483-08d47ec5cb71)

DashBoard Implementation:
![1_Salary_Dashboard_Type](https://github.com/user-attachments/assets/b257dcf1-5df5-4475-9ae5-43ffbe25c840)

## Data Validation

Filtered List 
  * 🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:
    * 🎯 User input is restricted to predefined, validated schedule types
    * 🚫 Incorrect or inconsistent entries are prevented
    * 👥 Overall usability of the dashboard is enhanced

![1_Salary_Dashboard_Data_Validation](https://github.com/user-attachments/assets/d68b78b7-caac-4472-aec9-6098b0399780)

## Conclusion
Developing this dashboard has unveiled distinct insights into salary trends by analyzing job titles, locations, and required skill sets. It offers clarity to users, regardless of their familiarity with the data profession, by exploring how these factors influence compensation.

### Final Thoughts
Upon detailed examination, it's evident that data analysts typically possess four key skills: SQL, Excel, Tableau or Power BI, and Python. Notably, job descriptions often encompass skills from related roles, such as Data Engineers or Data Scientists, which may contribute to the elevated salaries observed for Data Analysts.

For future analysis, isolating data analyst positions that specifically require these four core skills could provide a more accurate assessment of salary ranges, potentially yielding intriguing insights.
