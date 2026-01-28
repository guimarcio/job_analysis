# Project 2 - Analysis

## Introduction

I’ve always struggled with a lack of trusted information about jobs in the technology market. So, I investigated some key information about tech jobs to help people decide their paths in the tech job market. 

### Questions to Analyze

To understand the tech job market, I asked the following:

1. **Which tech job pays the most?**
2. **What is the salary difference among the job schedule types in each year?**
3. **Does the salary change depending on the company size?**
4. **Does level of experience impact salary?**
5. **How does the distribution of job schedule types change by year?**

### Excel Skills Used

Excel skills utilized for the analysis:

- **📊 Pivot Tables**
- **📈 Pivot Charts**
- **🧮 DAX (Data Analysis Expressions)**
- **🔍 Power Query**
- **💪 Power Pivot**

### Tech Jobs Dataset

The dataset used for this project contains real-world techjob information from 2020 to 2024. The dataset were changed in other project and I used the [transformed dataset](/0_Resources/data.csv) to analyze. The [original dataset](/0_Resources/global_tech_salary.txt) was obtained on a Kaggle page.

## 1️⃣ Which tech job pays the most?

### 🔍 Skill: Power Query (ETL) and Power Pivot (Data Model)

#### 📥 Extract

-First, I used Power Query to extract the data (`data.csv`) and created one query with all the tech job information.

#### 🔄 Transform

- Then, I transformed the query by adding id column and removing unnecessary columns.
- After that, I created a copy of the previous query to be loaded as a Data Model.

The final result in the Power Query Editor:![0_power_query.png](/Images/0_power_query.png)

#### 🔗 Load

- Finally, I loaded the first transformed query into the workbook, setting the foundation for my subsequent analysis. The other were loaded as a Data Model, so I could create the DAX. 

The Data Model: ![4.9_data_model.png](/Images/4.9_data_model.png)

### 📊 Analysis

#### 💡 Insights

- 📈 Some jobs, specially those related to `Software Engineer` pay more.
- 💼 Some opportunities have low salaries.

    ![1_sal_job.png](/Images/1_sal_job.png)

#### 🤔 So What

- This emphasizes how distinct salaries can be across different roles in the tech market.
----------------------------------------------------------------------------------------------------------------
