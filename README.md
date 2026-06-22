
# FP&A Budget vs Actual Dashboard | Power BI

## Project Overview

This project is an interactive Financial Planning & Analysis (FP&A) dashboard developed in Power BI to analyze Budget vs Actual performance across departments, regions, categories, and payment methods.

The dashboard helps finance teams and business leaders monitor financial performance, identify variances, evaluate departmental contributions, and gain actionable insights through dynamic visualizations and KPI reporting.

---

## Business Objective

Organizations need to compare actual financial performance against planned budgets to:

* Monitor financial health
* Track departmental performance
* Identify budget overruns and savings
* Analyze regional performance
* Support strategic decision-making

This dashboard provides a centralized view of financial performance through interactive and executive-friendly reporting.

---

## Dashboard Features

### Executive KPI Section

* Total Budget
* Total Actual
* Variance
* Variance Percentage
* Previous Year Comparison
* Year-over-Year (YoY) Analysis

### Financial Analysis

* Budget vs Actual Trend Analysis
* Variance by Department
* Variance Percentage by Region
* Category-wise Actual Analysis
* Variance by Payment Method
* Regional Performance Analysis

### Interactive Capabilities

* Year Filter
* Region Filter
* Dynamic Cross Filtering
* Interactive Visuals

---

## Data Modeling

A star schema data model was implemented to improve reporting performance and support scalable analysis.

### Fact Table

* Financial Transactions

### Dimension Tables

* Date
* Department
* Region
* Category
* Payment Method

---

## Key DAX Measures

### Budget

```DAX
Total Budget =
SUM(Finance[Budget])
```

### Actual

```DAX
Total Actual =
SUM(Finance[Actual])
```

### Variance

```DAX
Variance =
[Total Actual] - [Total Budget]
```

### Variance %

```DAX
Variance % =
DIVIDE(
    [Variance],
    [Total Budget],
    0
)
```

### Previous Year Budget

```DAX
Budget PY =
CALCULATE(
    [Total Budget],
    SAMEPERIODLASTYEAR('Date Table'[Date])
)
```

### Previous Year Actual

```DAX
Actual PY =
CALCULATE(
    [Total Actual],
    SAMEPERIODLASTYEAR('Date Table'[Date])
)
```

---

## Tools & Technologies

* Power BI Desktop
* Power Query
* DAX (Data Analysis Expressions)
* Data Modeling
* Microsoft Excel

---

## Skills Demonstrated

* Financial Planning & Analysis (FP&A)
* Budget vs Actual Reporting
* Variance Analysis
* Data Cleaning & Transformation
* Power Query
* DAX Calculations
* Data Modeling
* Star Schema Design
* Dashboard Development
* Business Intelligence Reporting
* Financial Data Visualization

---

## Key Insights Generated

* Measured overall variance between budgeted and actual financial performance.
* Identified departments contributing most significantly to variance.
* Evaluated regional financial performance.
* Analyzed spending patterns across categories.
* Assessed payment method contribution to financial variance.
* Enabled executive-level financial monitoring through KPI-driven reporting.

---

## Dashboard Preview

### Executive Dashboard

<img width="1347" height="759" alt="image" src="https://github.com/user-attachments/assets/85764166-6824-44ce-96ee-888aea36d2bd" />


### Department Variance Analysis

<img width="350" height="270" alt="image" src="https://github.com/user-attachments/assets/c47ee364-ac20-40ff-b6e5-12dd71c1058a" />


### Category Analysis

<img width="470" height="255" alt="image" src="https://github.com/user-attachments/assets/651e129f-b824-4967-b9d4-9cf95e3cfa7b" />


### Waterfall Variance Analysis

<img width="459" height="257" alt="image" src="https://github.com/user-attachments/assets/178c9b3d-05df-4beb-8389-fb8f49422c0f" />

---

## Project Outcome

This project demonstrates practical application of Power BI in Financial Planning & Analysis (FP&A), including KPI reporting, variance analysis, financial performance tracking, and executive dashboard design.

The dashboard is designed to support finance professionals, business analysts, and decision-makers in understanding financial performance and driving data-informed business decisions.
