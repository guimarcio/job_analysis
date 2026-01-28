# Excel Salary Dashboard

https://github.com/user-attachments/assets/09df0cad-76c9-4988-b946-d89f00a709cf

## Introduction

This tech jobs salary dashboard was created to help job seekers investigate tech job salaries and job schedule trends since 2020, so they can make more informed career decisions.

The data is real and was provided on a Kaggle page. It contains detailed information on job titles, salaries, locations, schedules, years, and more.

### Dashboard File
My final dashboard is in [project1.xlsx](project1.xlsx).

### Excel Skills

The following Excel skills were utilized for analysis:

- **📉 Charts**
- **🧮 Formulas and Functions**
- **❎ Data Validation**

## Dashboard Build

### Transformations

Before creating the dashboard, new columns were created to provide informative data. Job categories were also created, and some minor text changes and corrections were made.

<img src="/Images/dash_data.png" width="850" height="550" alt="Dataset">

### 📉 Charts

#### 📊 Tech Job Salaries - Bar Chart

As shown in the video above, the chart shows the median for each job category.

- 🛠️ **Excel Features:** Utilized bar chart feature (with formatted salary values) and optimized layout, selected by the data validation list, for clarity.
- 🎨 **Design Choice:** Horizontal bar chart for visual comparison of median salaries.
- 📉 **Data Organization:** Sorted job titles by descending salary for better readability.
- 💡 **Insights Gained:** This enables quick identification of salary trends.

#### 🗺️ Count of Jobs per Country - Map Chart

- 🛠️ **Excel Features:** Utilized Excel's map chart feature to plot job count globally.
- 🎨 **Design Choice:** Color-coded map to visually differentiate salary levels across regions.
- 📊 **Data Representation:** Plotted job count for each country with available data.
- 👁️ **Visual Enhancement:** Improved readability and immediate understanding of geographic opportunities.
- 💡 **Insights Gained:** Enables quick grasp of global job opportunities disparities.

#### ⏰ Count of Job per year and percentage of Job schedule type per year


- 🔍 **Unique List Generation:** Some filtering were done to calculate the Job Count and the percentage of job type.
- 📑 **Trend:** It was possible to visualize how the number of each job schedule type changed over the years.


### ❎ Data Validation

#### 🔍 Filtered List

- 🔒 **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the `Job Title` and `Year` option in the Data tab ensures:
    - 🎯 User input is restricted to predefined, validated job and year.
    - 🚫 Incorrect or inconsistent entries are prevented
    - 👥 Overall usability of the dashboard is enhanced

## Conclusion

I created this dashboard to highlight insights into salary trends across various tech-related job titles. It allows users to make informed career decisions.
