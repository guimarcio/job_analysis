# Project 2 - Analysis

## Introduction

I’ve always struggled with a lack of trusted information about jobs in the technology market. So, I investigated some key information about tech jobs to help people decide their paths in the tech job market. 

### Questions to Analyze

To understand the tech job market, I asked the following:

1. **Which tech job pays the most?**
2. **What is the salary difference among the job schedule types in each year?**
3. **Does the salary change depending on the company size?**
4. **Does experience level impact on salary?**
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

- Finally, I loaded the first transformed query into the workbook, setting the foundation for my subsequent analysis. The other were loaded as a Data Model, so I could create the future DAX. The Data Model: 

![4.9_data_model.png](/Images/4.9_data_model.png)

### 📊 Analysis

#### 💡 Insights

- 📈 Some jobs, specially those related to `Software Engineer` pay more.
- 💼 Some opportunities have low salaries.

    ![1_sal_job.png](/Images/1_sal_job.png)

#### 🤔 So What

- This emphasizes how distinct salaries can be across different roles in the tech market.


## 2️⃣ What is the salary difference among the job schedule types in each year??

### 🧮 Skills: PivotTables and Pivot Charts

#### 📈Pivot Table and Chart

- 🔢 I created a PivotTable with different fields: in the column I used the `job_type`; in the row I used the `year`; and the `salary` in the values configured to be the mean value.
- 📊 Then I created a chart to show, based on the year, the mean salary for the hybrid, on-site and remote jobs.
- 
### 📊 Analysis

#### 💡 Insights

- 💼 Remote and On-Site jobs have approximate salaries, while hybrid has lower salary than both other categories.
- ⭐The year after the pandemics, remote jobs tended to pay more than the others.

    ![2_sal_year_type.png](/Images/2_sal_year_type.png)

#### **🤔 So What**

- These salary insights are important for planning and salary negotiations, helping professionals and companies align their offers with market standards while considering job schedule types.

## 3️⃣ Does the salary change depending on the company size?

### 🔧 Skills: Pivot Table and Conditional Cell Formating

#### 💪 Pivot Table

I created a Pivot Table, where the column is the company size, the row is the job title, and the values are the mean salary. 

### 📊Analysis

#### 💡Insights

- 💻 The salary difference between large and medium-sized companies does not depend on job title and is very similar across roles.
- ☁️ Small companies pay much less than the other categories.
- ⭐ The job title doesn't affect the salary when compared to the size of the company. 

    ![3_sal_compsize.png](/Images/3_sal_compsize.png)

#### 🤔So What

- Understanding the company size and job offer helps job seekers estimate their approximate salary.

## 4️⃣ Does experience level impact on salary?

### 📊 Skill: Pivot Table and Chart

#### 📈 PivotChart

- I created a table with experience level as rows and mean salary as values. Then, I created a chart similar to a scatter plot to see the trend of the mean salary for each experience level.

### 📊 Analysis

#### 💡Insights

- 💰 Higher mean salaries are associated with higher experience level.

    ![4_sal_level.png](/Images/4_sal_level.png)

### 🤔So What

- This chart highlights the importance of investing time in learning and specializing so that job seekers can find the best opportunities.

## 5️⃣ Does experience level impact on salary?

### 📊 Skill: Power Pivot and DAX

#### 📈 Data Model and DAX

- In the Data Model Editor, I created a DAX for the percentage of job schedule types across the years. First I used a metric to count and then I divide it depending on the year:

  ```
  total_count:=COUNT(data_mod[Índice])
  ```
  ```
  percentage:=DIVIDE([total_count]; CALCULATE([total_count];ALLEXCEPT(data_mod;data_mod[work_year])))
  ``` 

### 📊 Analysis

#### 💡Insights

- 💰 The percentage of remote and hybrid jobs have been reducing, since the pandemics ended.

    ![5_dax.png](/Images/5_dax.png)

### 🤔So What

- Probably, most job offers are for on-site positions. This can help job seekers find the best option for their careers.

## Conclusion

Using a dataset from real-world job postings, I investigated essential features related to tech jobs. By leveraging Excel tools such as Power Query, PivotTables, DAX, and charts, I identified key correlations between higher salaries and the features analyzed. I hope this project serves as a practical guide for tech professionals and provides an overview of the skills needed for higher-paying roles.
