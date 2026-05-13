# Plant Co. Performance Analytics Dashboard

An end-to-end Power BI analytics project demonstrating business intelligence, data transformation, data modeling, DAX calculations, and dashboard storytelling using CSV datasets.

---

# Project Overview

This project analyzes Plant Co.'s operational and sales performance using Power BI.

The dashboard provides insights into:

- Gross Profit trends
- YTD vs PYTD analysis
- Country performance
- Product profitability
- Product category analysis
- Account segmentation

---

# Dashboard Preview

![alt text](dashboard-overview.png)

---

# Business Objectives

The primary goal of this project is to help stakeholders:

- Monitor profitability
- Identify underperforming regions
- Analyze product contribution
- Track year-over-year growth
- Improve operational decision-making

---

# Tech Stack

| Technology | Purpose |
|---|---|
| Power BI | Dashboard development |
| Power Query | Data transformation |
| DAX | Data modeling & calculations |
| Git & GitHub | Version control |
| CSV Files | Data source |
| VS Code | Documentation |

---

# Dataset Information

The project uses CSV files containing:

- Sales transactions
- Product data
- Customer accounts
- Country hierarchy

---

# Data Model

This project follows a star schema model.

## Fact Table

- Fact_Sales

## Dimension Tables

- Dim_Product
- Dim_Account
- Dim_Date
- Dim_Country

---

# Key DAX Measures

## Gross Profit

```DAX
Gross Profit =
SUM('Fact Sales'[Gross_Profit])
```

## YTD Gross Profit

```DAX
YTD Gross Profit =
TOTALYTD(
    [Gross Profit],
    'Dim_Date'[Date]
)
```

## PYTD Gross Profit

```DAX
PYTD Gross Profit =
CALCULATE(
    [YTD Gross Profit],
    SAMEPERIODLASTYEAR('Dim_Date'[Date])
)
```

## GP%

```DAX
GP% =
DIVIDE(
    [Gross Profit],
    [Sales],
    0
)
```

---

# Dashboard Features

- Treemap
- Waterfall Chart
- Combo Chart
- Scatter Plot
- Slicers
- Filters

---

# Project Structure

```plaintext
Plant-Co-Performance-Dashboard/
│
├── data/
│   └── PlantCo.xls
│
├── reports/
│   └── PlantCoDashboard.pbix
│
├── images/
│   └── dashboard-preview.png
│
├── README.md
├── LICENSE
└── .gitignore│

```

---

# How to Use

1. Clone the repository

```bash
git clone https://github.com/Abiolabello/powerbi-business-performance-dashboard
```

2. Open the `.pbix` file in Power BI Desktop

3. Refresh the dataset if required

4. Explore the interactive dashboard

---

# Future Improvements

- Add forecasting models
- Deploy to Power BI Service
- Implement Row-Level Security (RLS)
- Add automated refresh pipelines
- Integrate SQL database source

---

# Author

Abiola Bello

---

# License

This project is licensed under the MIT License.