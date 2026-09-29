# 🏥 Health Patient Flow Dashboard \| Power BI

![Power
BI](https://img.shields.io/badge/Power%20BI-Data%20Visualization-F2C811?logo=powerbi&logoColor=black)
![Dashboard](https://img.shields.io/badge/Project-Health%20Patient%20Flow-0B6EBD)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Project Overview

**Health Patient Flow Dashboard** is a Power BI internship project
designed to analyze and visualize patient flow in a healthcare
environment.

The dashboard provides an interactive view of patient records,
departments, doctors, patient types, treatment/waiting time, admissions,
and discharges. It helps users understand patient movement and identify
important patterns through KPIs, charts, filters, and a detailed table.

The dashboard is designed to be simple, interactive, and easy to
understand for healthcare reporting and data-analysis purposes.

------------------------------------------------------------------------

## 🎯 Project Objective

The main objectives of this project are:

-   Analyze overall patient flow.
-   Monitor total patient records.
-   Compare patient flow across departments.
-   Analyze different patient types.
-   Track admitted and discharged patients.
-   Analyze average waiting time.
-   Analyze average treatment time.
-   Identify doctors handling a higher number of patients.
-   Observe patient flow trends over time.
-   Provide interactive filtering using slicers.
-   Present healthcare data in a clear visual format.

------------------------------------------------------------------------

## 🛠️ Tools & Technologies

  Tool                     Purpose
  ------------------------ -----------------------------------------
  **Microsoft Power BI**   Dashboard development and visualization
  **Power Query**          Data cleaning and transformation
  **DAX**                  Measures and KPI calculations
  **Data Visualization**   Charts, cards, tables and slicers
  **CSV Dataset**          Source data

------------------------------------------------------------------------

## 📊 Dashboard KPIs

The dashboard currently displays the following key metrics:

-   **Total Patient:** 1,000
-   **Average Wait Time:** 62
-   **Average Treatment Time:** 187
-   **Admitted Patient:** 228
-   **Discharge Patient:** 406
-   **Total Records:** 1,000

> KPI values shown above are based on the dataset/filter state
> represented in the dashboard screenshot.

------------------------------------------------------------------------

## 📈 Dashboard Visuals

### 1. Patient Flow Trend

A line chart is used to display patient flow across months.

**Purpose:** - Understand monthly patient volume. - Identify increases
and decreases in patient flow. - Compare patient activity between
months.

------------------------------------------------------------------------

### 2. Patient by Department

A column/bar chart shows the number of patients handled by different
departments.

Example departments visible in the dashboard include:

-   ENT
-   Gynecology
-   Dermatology
-   Orthopedics
-   Cardiology
-   Neurology
-   General Medicine
-   Oncology
-   Pediatrics

**Purpose:** - Compare department-wise patient flow. - Identify
departments with higher patient volume.

------------------------------------------------------------------------

### 3. Patient Type

This visual compares patient categories such as:

-   Inpatient
-   Emergency
-   OPD
-   Follow-up

**Purpose:** - Understand the distribution of different patient types. -
Compare outpatient, inpatient, emergency, and follow-up activity.

------------------------------------------------------------------------

### 4. Count of Patient ID by Doctor

A horizontal bar chart displays patient count by doctor.

**Purpose:** - Compare the number of patients associated with each
doctor. - Identify doctors with relatively higher patient volumes.

------------------------------------------------------------------------

### 5. Department-wise Patient Flow Table

The dashboard contains a detailed table showing
patient-level/department-level information.

The table can be used to inspect fields such as:

-   Department
-   Patient ID count
-   Patient Type
-   Patient Status

**Purpose:** - Provide detailed information behind the summary
visuals. - Support drill-down and data inspection.

------------------------------------------------------------------------

### 6. Count of Patient ID by Day

A column chart displays patient count by day.

**Purpose:** - Understand daily patient flow. - Identify days with
relatively higher or lower patient activity.

------------------------------------------------------------------------

## 🎛️ Interactive Filters / Slicers

The dashboard contains interactive filters for:

### Department

Filter the complete dashboard based on a selected department.

### Doctor

View patient flow for a particular doctor.

### Patient Type

Filter the dashboard by:

-   Inpatient
-   Emergency
-   OPD
-   Follow-up

### Date

Filter the report based on the selected date period.

These slicers make the dashboard interactive and allow users to analyze
specific segments of the data.

------------------------------------------------------------------------

## 🧮 Example DAX Measures

The following are examples of measures that can be used to create the
dashboard KPIs.

### Total Patient

``` dax
Total Patient = DISTINCTCOUNT('Health Patient Flow'[Patient ID])
```

### Total Records

``` dax
Total Records = COUNTROWS('Health Patient Flow')
```

### Average Wait Time

``` dax
Average Wait Time = AVERAGE('Health Patient Flow'[Wait Time])
```

### Average Treatment Time

``` dax
Average Treatment Time = AVERAGE('Health Patient Flow'[Treatment Time])
```

### Admitted Patient

``` dax
Admitted Patient =
CALCULATE(
    DISTINCTCOUNT('Health Patient Flow'[Patient ID]),
    'Health Patient Flow'[Patient Status] = "Admitted"
)
```

### Discharge Patient

``` dax
Discharge Patient =
CALCULATE(
    DISTINCTCOUNT('Health Patient Flow'[Patient ID]),
    'Health Patient Flow'[Patient Status] = "Discharged"
)
```

> Replace table/column names with the exact names used in your Power BI
> model.

------------------------------------------------------------------------

## 🔄 Data Preparation Process

The project follows a basic data-analysis workflow:

``` text
Raw Dataset
     ↓
Power Query
     ↓
Data Cleaning
     ↓
Data Transformation
     ↓
Data Model
     ↓
DAX Measures
     ↓
Power BI Visualizations
     ↓
Interactive Dashboard
```

### Data Cleaning Activities

Typical preparation steps include:

-   Removing duplicate records.
-   Checking missing values.
-   Correcting data types.
-   Formatting date fields.
-   Standardizing categorical values.
-   Creating required calculated columns/measures.
-   Checking data consistency before visualization.

------------------------------------------------------------------------

## 🎨 Dashboard Design

The dashboard uses a healthcare-themed blue interface with:

-   KPI cards
-   Line chart
-   Bar/column charts
-   Detailed data table
-   Slicers
-   Date-period filter
-   Interactive visual filtering

The layout is designed to keep the most important information visible at
the top and detailed analysis below.

------------------------------------------------------------------------

## 💡 Key Analysis Areas

This dashboard can help answer questions such as:

1.  How many patients are recorded?
2.  What is the average waiting time?
3.  What is the average treatment time?
4.  How many patients were admitted?
5.  How many patients were discharged?
6.  Which departments have higher patient flow?
7.  What type of patients are most common?
8.  Which doctors have higher patient counts?
9.  How does patient flow change over time?
10. How does patient flow vary by day?

------------------------------------------------------------------------

## 📁 Suggested GitHub Repository Structure

``` text
Health-Patient-Flow-Dashboard/
│
├── README.md
├── dataset/
│   └── Health_Patient_Flow.csv
│
├── dashboard/
│   └── Health_Patient_Flow_Dashboard.pbix
│
├── images/
│   └── health-patient-flow-dashboard.png
│
└── documentation/
    └── project-details.pdf
```

------------------------------------------------------------------------

## 🚀 How to Use the Project

1.  Download or clone this repository.
2.  Open the `.pbix` file in Microsoft Power BI Desktop.
3.  Make sure the dataset is available at the configured source
    location.
4.  Refresh the data if required.
5.  Use the slicers to filter the dashboard.
6.  Select different departments, doctors, patient types, or dates.
7.  Analyze the KPI cards and charts.

------------------------------------------------------------------------

## 📷 Dashboard Preview

Add your dashboard screenshot to the repository and display it here:

``` markdown
![Health Patient Flow Dashboard](images/health-patient-flow-dashboard.png)
```

------------------------------------------------------------------------

## 📚 Skills Demonstrated

This project demonstrates practical skills in:

-   Power BI
-   Power Query
-   DAX
-   Data Cleaning
-   Data Transformation
-   Data Visualization
-   Dashboard Design
-   KPI Development
-   Interactive Reporting
-   Healthcare Data Analysis
-   Business Intelligence

------------------------------------------------------------------------

## 🎓 Internship Project

**Project Type:** Power BI Internship Project\
**Domain:** Healthcare Analytics\
**Tool:** Microsoft Power BI\
**Dashboard:** Health Patient Flow Dashboard

This project demonstrates the use of business intelligence and data
visualization techniques to convert healthcare patient-flow data into an
interactive analytical dashboard.

------------------------------------------------------------------------

## 🔮 Future Enhancements

Possible future improvements include:

-   Patient admission/discharge trend analysis.
-   Department performance KPIs.
-   Doctor workload analysis.
-   Waiting-time distribution.
-   Treatment-time analysis.
-   Emergency patient monitoring.
-   Monthly and yearly comparison.
-   Drill-through pages.
-   Tooltip pages.
-   Automated data refresh.
-   Additional healthcare performance indicators.

------------------------------------------------------------------------

## 👨‍💻 Author

**Shivam Parmar**

**Skills:** Power BI \| Data Analysis \| Excel \| Python \| SQL

------------------------------------------------------------------------

## ⭐ Conclusion

The **Health Patient Flow Dashboard** provides an interactive and
easy-to-understand view of healthcare patient activity. It combines
KPIs, trends, department analysis, patient-type analysis, doctor-level
analysis, and detailed records into a single Power BI report.

The project demonstrates how raw healthcare data can be transformed into
meaningful visual insights using **Power BI, Power Query, and DAX**.
