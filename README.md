# San Francisco Employee Compensation Analysis

**Exploratory Data Analysis (EDA) & Insights**

This project analyzes employee compensation data from the City and County of San Francisco. The goal is to understand how **salaries, overtime, and benefits** evolve across departments, organization groups, and job families, and to uncover structural patterns that affect workforce planning and budget allocation.

***

## Project Overview

Employee compensation is one of the city’s largest expenses. This analysis aims to answer key questions such as:
* Which departments and organization groups drive the majority of compensation spending?
* How do salary, benefits, and overtime behave across the workforce?
* Are there departments overly dependent on overtime?
* Which job families receive the highest compensation and benefits?
* Are there structural differences between employment types?

This repository includes the complete EDA, cleaning steps, visualizations, and insights.

***

## Key Findings

From the Exploratory Data Analysis (EDA):

1.  **Public Protection Dominates Total Compensation**
    * Fire, Police, and Sheriff’s departments receive the highest pay and benefits, shaping citywide trends and risk profiles.
2.  **Overtime is Heavily Concentrated**
    * A small number of departments account for most overtime spending—especially Fire, Sheriff, and Public Health—creating **burnout hotspots**.
3.  **Benefits Vary Significantly**
    * High-risk and unionized job families receive large benefit packages; administrative and clerical roles receive far less, indicating inconsistent allocation.
4.  **Salary is Stable, but Overtime is Volatile**
    * This volatility explains major fluctuations in total compensation across years and signals an over-reliance on unstable pay levers.
5.  **The Workforce is Unevenly Distributed**
    * Some organization groups operate far larger teams (e.g., Community Health), directly affecting budget share and resource allocation.

***

## Dataset Description

The dataset contains employee payroll information for San Francisco employees over multiple years.

### Main Columns

| Column | Description |
| :--- | :--- |
| **Year** | Reporting year |
| **Organization Group** | High-level category of departments |
| **Department** | Specific department |
| **Job Family** | Grouping of related jobs |
| **Salaries** | Base salary |
| **Overtime** | Overtime pay |
| **Total Salary** | Base + overtime + other |
| **Total Benefits** | Health, retirement, and other benefits |
| **Total Compensation** | Salary + benefits |
| **Overtime %** | Overtime / Total Salary |
| **Benefits %** | Benefits / Total Compensation |
| **Pay-to-Benefit Ratio** | Salary / Benefits |

A full data dictionary is included in the Technical Report.

***

## Data Cleaning & Preparation

Performed using Python (`pandas`):

* Removed leading/trailing spaces.
* Converted all monetary columns to numeric.
* Filled missing values appropriately (`Overtime → 0`, Benefits only filled when appropriate).
* Removed duplicate employee-year rows.
* Recalculated critical ratios: **Benefits %**, **Overtime %**, **Pay-to-Benefit Ratio**.
* Standardized department and job names.
* Dropped rows with invalid or extreme outliers.


***

## Exploratory Data Analysis

Visualizations created include:
* Average Total Compensation by Organization Group
* Average Total Compensation by Department
* Overtime Percentage by Department
* Benefit Percentage by Job Family
* Job Families with Highest Compensation
* Employee Distribution by Organization Group
* Overtime Trends Over Time
* Benefits Share Over Time

All visuals are included in the presentation and Tableau.

***

## Tools & Technologies

* **Python** (`pandas`, `numpy`, `matplotlib`, `seaborn`)
* **Tableau** (interactive dashboards & visuals)
* **Excel** (initial data checks)
* **Canva** (final presentation)

***

## Recommendations

Based on the analysis, we propose three actionable policy recommendations:

1.  **Address Overtime-Heavy Departments**
    * *Action:* Cap overtime usage and reinvest savings into strategic hiring to reduce burnout and long-term costs.
2.  **Standardize Benefits**
    * *Action:* Ensure benefit structures are consistently aligned with job risk levels and performance requirements to reduce disparities.
3.  **Improve Budget Monitoring for Public Protection**
    * *Action:* Implement specific budget controls for this group, as small changes in their compensation create large city-wide effects.

***

## Limitations

* Missing work-hour data prevents productivity analysis.
* Benefit calculations depend on department reporting accuracy.
* Overtime may spike due to emergencies not visible in the dataset.
* Job titles change over years, making grouping imperfect.
