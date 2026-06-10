# CodeAlpha_Educational_Performance_Dashboard

## Project Title

**Educational Performance and Resource Allocation Dashboard using Power BI**

## Internship Domain

**Power BI Internship — CodeAlpha**

## Task

**Task 4: Educational Performance and Resource Allocation**

---

## Project Overview

This project is an interactive **Power BI dashboard** designed to analyze student academic performance and identify factors that affect educational outcomes.

The dashboard focuses on student scores, attendance, study habits, internet access, school type, parental education, and other support factors. It helps education managers understand performance gaps, identify at-risk students, and make data-driven decisions for improving student outcomes.

---

## Objective

The main objective of this project is to evaluate student performance and support better resource allocation in educational institutions.

The dashboard aims to:

* Analyze overall academic performance
* Track student scores across different subjects
* Identify at-risk students
* Analyze attendance and study behavior
* Compare performance across school types
* Study the impact of internet access and study methods
* Support data-driven decisions in education management

---

## Dataset Used

The dataset used in this project is:

```text
Student_Performance.csv
```

The dataset contains student-level academic and support-related information.

### Dataset Columns

| Column                | Description                             |
| --------------------- | --------------------------------------- |
| student_id            | Unique student identifier               |
| age                   | Student age                             |
| gender                | Student gender                          |
| school_type           | Type of school                          |
| parent_education      | Parent education level                  |
| study_hours           | Number of study hours                   |
| attendance_percentage | Student attendance percentage           |
| internet_access       | Whether the student has internet access |
| travel_time           | Student travel time category            |
| extra_activities      | Participation in extra activities       |
| study_method          | Student study method                    |
| math_score            | Student math score                      |
| science_score         | Student science score                   |
| english_score         | Student English score                   |
| overall_score         | Overall academic score                  |
| final_grade           | Final academic grade                    |

---

## Tools and Technologies

* Microsoft Power BI Desktop
* Power Query
* DAX
* CSV Dataset
* Data Visualization
* Educational Analytics

---

## Dashboard Pages

The Power BI report contains two main pages:

---

# Page 1: Academic Performance Overview

This page provides a high-level overview of student academic performance.

## KPI Cards

The page includes the following KPI cards:

| KPI                   | Description                                         |
| --------------------- | --------------------------------------------------- |
| Total Students        | Total number of students in the dataset             |
| Average Overall Score | Average overall academic score                      |
| Average Attendance    | Average student attendance percentage               |
| Average Study Hours   | Average study hours                                 |
| At Risk Rate          | Percentage of students with low overall performance |

## Visualizations

### 1. Students by Final Grade

Shows the distribution of students across final grade categories.

### 2. Average Overall Score by Gender

Compares academic performance between male and female students.

### 3. Average Overall Score by School Type

Shows performance differences between school types.

### 4. Average Overall Score by Parent Education

Analyzes the relationship between parental education and student performance.

### 5. Average Overall Score by Age

Shows how average performance differs by student age.

### 6. Students by Gender

Shows the gender distribution of students.

## Interactive Filters

This page includes slicers for:

* Gender
* School Type
* Parent Education
* Final Grade

---

# Page 2: Resource & Student Support Analysis

This page focuses on resources and support factors that may affect student performance.

## KPI Cards

The page includes the following KPI cards:

| KPI                  | Description                                    |
| -------------------- | ---------------------------------------------- |
| Internet Access Rate | Percentage of students with internet access    |
| Average Study Hours  | Average study hours                            |
| Average Attendance   | Average attendance percentage                  |
| At Risk Students     | Number of students with overall score below 60 |
| At Risk Rate         | Percentage of at-risk students                 |

## Visualizations

### 1. Average Overall Score by Internet Access

Shows whether students with internet access perform better than students without internet access.

### 2. Average Overall Score by Study Method

Compares student performance across different study methods.

### 3. Average Overall Score by Extra Activities

Analyzes the effect of extra activities on academic performance.

### 4. Average Overall Score by Travel Time

Shows whether travel time affects student performance.

### 5. Resource and Risk Summary Table

A table showing:

* School Type
* Total Students
* Average Overall Score
* At Risk Students
* At Risk Rate

This table helps identify groups that may need more academic support or better resource allocation.

## Interactive Filters

This page includes slicers for:

* Internet Access
* Study Method
* Extra Activities
* Travel Time

---

## DAX Measures Used

### Total Students

```DAX
Total Students = COUNTROWS('Student_Performance')
```

### Average Overall Score

```DAX
Average Overall Score = AVERAGE('Student_Performance'[overall_score])
```

### Average Attendance

```DAX
Average Attendance = AVERAGE('Student_Performance'[attendance_percentage])
```

### Average Study Hours

```DAX
Average Study Hours = AVERAGE('Student_Performance'[study_hours])
```

### Average Math Score

```DAX
Average Math Score = AVERAGE('Student_Performance'[math_score])
```

### Average Science Score

```DAX
Average Science Score = AVERAGE('Student_Performance'[science_score])
```

### Average English Score

```DAX
Average English Score = AVERAGE('Student_Performance'[english_score])
```

### At Risk Students

Students with an overall score below 60 are considered at risk.

```DAX
At Risk Students =
CALCULATE(
    COUNTROWS('Student_Performance'),
    'Student_Performance'[overall_score] < 60
)
```

### At Risk Rate

```DAX
At Risk Rate =
DIVIDE(
    [At Risk Students],
    [Total Students]
)
```

### Students With Internet Access

```DAX
Students With Internet Access =
CALCULATE(
    COUNTROWS('Student_Performance'),
    'Student_Performance'[internet_access] = "yes"
)
```

### Internet Access Rate

```DAX
Internet Access Rate =
DIVIDE(
    [Students With Internet Access],
    [Total Students]
)
```

---

## Key Insights

The dashboard helps identify important educational insights such as:

* The average overall academic performance of students.
* The percentage of students considered at risk.
* The relationship between attendance and student performance.
* The impact of study hours on academic outcomes.
* The difference in performance between school types.
* The effect of internet access on student scores.
* The relationship between study method and academic results.
* Student groups that may require additional academic support.

---

## Business / Educational Value

This dashboard can help schools and education managers to:

* Monitor student performance more effectively.
* Identify students who need extra support.
* Understand the impact of attendance and study habits.
* Analyze how learning resources affect student outcomes.
* Improve resource allocation decisions.
* Support academic planning using data-driven insights.

---

## Project Files

The repository contains:

```text
CodeAlpha_Educational_Performance_Dashboard.pbix
README.md
Student_Performance.csv
screenshots/
```

Recommended folder structure:

```text
CodeAlpha_Educational_Performance_Dashboard/
│
├── CodeAlpha_Educational_Performance_Dashboard.pbix
├── README.md
├── dataset/
│   └── Student_Performance.csv
│
└── screenshots/
    ├── academic_performance_overview.png
    └── resource_student_support_analysis.png
```

---

## Screenshots

### Page 1: Academic Performance Overview
<img width="1495" height="1167" alt="image" src="https://github.com/user-attachments/assets/b2053888-35e4-446f-8a54-c34cc2f33de6" />


```markdown
![Academic Performance Overview](screenshots/academic_performance_overview.png)
```

### Page 2: Resource & Student Support Analysis
<img width="1532" height="1309" alt="image" src="https://github.com/user-attachments/assets/1f6928c0-107d-482f-9f19-c86481c98d5a" />

```markdown
![Resource & Student Support Analysis](screenshots/resource_student_support_analysis.png)
```

---

## How to Open the Project

1. Download the `.pbix` file from this repository.
2. Open it using **Microsoft Power BI Desktop**.
3. Use the slicers to filter the dashboard.
4. Navigate between the two pages:

   * Academic Performance Overview
   * Resource & Student Support Analysis

---

## Final Deliverable

The final deliverable is an interactive Power BI dashboard that supports education management decisions through:

* Academic performance analysis
* Attendance and study behavior tracking
* At-risk student identification
* Resource and support factor analysis
* Interactive visual reporting

---

## Internship Submission

This project was completed as part of the **CodeAlpha Power BI Internship**.

Repository name:

```text
CodeAlpha_Educational_Performance_Dashboard
```

---

## Author

**Marwan Tamer**

---

## Tags

`Power BI` `Education Analytics` `Student Performance` `DAX` `Power Query` `Dashboard` `Business Intelligence` `CodeAlpha`
