## Atlas Labs | HR People Analytics Dashboard
### 📌 Project Overview
Atlas Labs is a comprehensive Power BI business intelligence solution designed to help HR departments monitor employee performance, understand demographic distributions, and identify the root causes of employee attrition.

This project transforms raw HR data into a 4-page interactive report that tracks 1,470 employees and provides deep dives into hiring trends, ethnic diversity, and performance metrics.

## 🏗️ Data Architecture
The project follows a Star Schema (with a minor Snowflake extension for education levels) to ensure high performance and scalability.

- Fact Table: fact_PerformanceRating (Contains all performance-based events and scores).

Dimension Tables:

Dim_Employee: Core employee attributes (Hiring, Attrition, Gender, Salary).

DimDate: Calendar table for Time Intelligence.

Dim_Educationlevel: (Sub-dimension to Employee).

Dim_Ratinglevel & Dim_Satisfiedlevel: Lookup tables for categorical scoring.

![Schema](images/Schema.png)

## 📊 Dashboard Pages
### 1. Overview: Executive Summary
- Focuses on high-level KPIs and hiring velocity.

KPIs: Total Employees (1,470), Active (1,233), Inactive (237), and 16.1% Attrition Rate.

Hiring Trends: Stacked Column Chart tracking growth vs. attrition over time.

Departmental Split: Technology leads the company in headcount.

Key Insight: 2020 was a volatile year with the highest raw attrition count (28 people).

![Alt text](images/Overview.png)

### 2. Demographics: Diversity & Inclusion
- Analyzes the makeup of the workforce.

Age Profile: Employees range from 18 to 51, with the 20–29 age bracket being the largest.

Marital Status: 42.45% of the workforce is married.

Equity Analysis: A dual-axis chart comparing Ethnicity to Average Salary shows that White employees represent the largest group and the highest salary bracket.

![Alt text](images/demographics.png)

### 3. Performance Tracker: Individual Deep Dive
- A specialized page for managers to review specific employee histories using a Slicer by Employee Name.

Timeline: Tracks Start Date, Last Review, and Next Review dates.

Satisfaction Metrics: 6 Line charts tracking Job, Relationship, Environment, and Work-Life Balance scores.

Technical Implementation: Utilized USERELATIONSHIP and Inactive Relationships to toggle between different satisfaction categories within a single dimension.

![Alt text](images/Performance.png)

### 4. Attrition: Risk Factor Analysis
- Identifying why people leave.

Highest Risk Role: Sales Representatives have a staggering 39.76% attrition rate.

Time Factor: Attrition peaked in 2020 at 22.05%.

Key Drivers:

Travel: Frequent travelers are more likely to leave (24.91%).

Overtime: Employees working overtime show a 30.53% attrition rate.

Tenure: New hires (1 year at company) are the most vulnerable, with a 34.46% attrition rate.

![Alt text](images/attrition.png)


### 🚀 Key Learning Points
Relationship Management: Handled multiple connections between a single satisfaction dimension and multiple fact columns using active/inactive paths.

Age Binning: Created custom age groups (20-29, etc.) to turn a continuous variable into a categorical one for better visualization.

UX Design: Implemented a Page Navigator for a seamless "App-like" user experience.

HR Insights: Identified that "Overtime" and "Travel Frequency" are the top two controllable predictors of employee turnover.

#### How to view this project
- Download the .pbix file from this repository.

- Open with Power BI Desktop.

- Explore the pages using the sidebar navigation.

