# Employee Hours BI Analytics

## Project Overview

An end-to-end Business Intelligence portfolio project built with Power BI using synthetic employee-hours data. The project explores dimensional modeling, DAX calculations, filter context, and interactive analysis.

**Project Status:** In Progress

## Business Objective

Analyze how employees allocate their working hours across departments, programs, and activities. The goal is to provide visibility into workload distribution and enable users to explore data through interactive reporting.

## Technology Stack

- Power BI
- Power Query
- DAX
- GitHub
  
## Data model

The project uses a star schema with one fact table and four dimensions.

```text
                     Dim Employee     
                         |
                         |
    Dim Dates ------ Fact Hours ------ Dim Programs
                         |
                         |
                      Dim Activities

```

### Fact Table

**Fact Hours**

Contains employee-hours records and foreign keys linking to the dimension tables.

**Grain:** One row represents hours recorded for one employee, one program, one activity, on one date.

### Dimension Tables

- **Dim Employees:** Employee, department, role, and location attributes.
- **Dim Dates:** Calendar attributes such as year, quarter, month, and day.
- **Dim Programs:** Program names and categories.
- **Dim Activities:** Activity names and categories.

  ## Dataset

  All data is synthetic and created specifically for learning and portfolio purposes.

| Dataset | Description
|---|---|
| employees.csv | Employee and department information |
| dates.csv | Calendar and reporting attributes |
| programs.csv | Program details |
| activities.csv | Activity details |
| fact_hours.csv | Employee-hours records |

The dataset contains 50 employees, 8 programs, 12 activities, and 2,899 fact records covering January 2025 through September 2026.

## Analytics Implemented

The current Power BI model includes measures for:

- Total hours
- Hours from long entries
- Long-entry record count
- Distinct employee count
- Average hours per employee
- Department-independent total hours
- Percentage of total hours by department and activity

The project also explores DAX filter context, 'CALCULATE()', 'FILTER()', and 'REMOVEFILTERS()'.

## Planned Enhancements

- Refine data preparation and data-quality checks.
- Build an interactive dashboard with KPI cards and analytics visuals.
- Add and validate row-level security.
- Document DAX measures and modeling decisions.
- Publish screenshots and project learnings.

## Data Disclaimer

This project uses fictional data. It does not contain confidential information from any employer or client.


