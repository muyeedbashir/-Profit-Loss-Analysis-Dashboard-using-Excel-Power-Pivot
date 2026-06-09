# 📊 Profit & Loss Analysis Dashboard using Excel Power Pivot

## 📌 Project Overview

This project analyzes company Profit & Loss (P&L) performance using Excel Power Pivot and Power Query.

The objective was to transform raw business data from multiple CSV files into an interactive reporting dashboard capable of tracking:

- Net Sales
- Cost of Goods Sold (COGS)
- Gross Margin
- Gross Margin Percentage (GM%)
- Market-wise performance
- Quarterly Sub-Zone analysis

The project follows a complete Business Intelligence workflow including data extraction, transformation, data modeling, DAX calculations, and dashboard creation.

---

## Business Problem

Business stakeholders need a consolidated view of financial performance across multiple markets and regions.

The dashboard helps answer:

- Which markets generate the highest sales?
- Which regions have the strongest margins?
- How does Gross Margin change across quarters?
- Which sub-zones perform best financially?

---

## 🛠 Tools Used

- Microsoft Excel
- Power Query
- Power Pivot
- DAX (Data Analysis Expressions)

---

## 📂 Dataset

The project uses 5 CSV files:

1. dim_customer.csv(https://github.com/muyeedbashir/-Profit-Loss-Analysis-Dashboard-using-Excel-Power-Pivot/blob/main/dim_customer.csv)
2. dim_product.csv(https://github.com/muyeedbashir/-Profit-Loss-Analysis-Dashboard-using-Excel-Power-Pivot/blob/main/dim_product.csv)
3. dim_market.csv(https://github.com/muyeedbashir/-Profit-Loss-Analysis-Dashboard-using-Excel-Power-Pivot/blob/main/dim_market.csv)
4. fact_sales_monthly_with_cost.csv(https://github.com/muyeedbashir/-Profit-Loss-Analysis-Dashboard-using-Excel-Power-Pivot/blob/main/fact_sales_monthly_with_cost.zip)
6. ns_targets_2021.csv(https://github.com/muyeedbashir/-Profit-Loss-Analysis-Dashboard-using-Excel-Power-Pivot/blob/main/ns_targets_2021.csv)

---

## 🔄 Data Transformation Process

### Power Query Tasks

- Imported multiple CSV files
- Cleaned inconsistent values
- Checked data types
- Removed data quality issues
- Standardized columns
- Prepared tables for modeling

---

## 🏗 Data Modeling

A Star Schema model was created using Power Pivot.

### Relationships Created

- dim_customer → fact_sales_monthly_with_cost
- dim_product → fact_sales_monthly_with_cost
- dim_date → fact_sales_monthly_with_cost
- dim_market → dim_customer
- dim_market → ns_targets_2021
- dim_date → ns_targets_2021

---

## 📐 DAX Measures Created

### Net Sales

```DAX
Net Sales := SUM(fact_sales_monthly_with_cost[net_sales_amount])
```

### COGS

```DAX
COGS := SUM(fact_sales_monthly_with_cost[total_cogs])
```

### Gross Margin

```DAX
Gross Margin := [Net Sales] - [COGS]
```

### Gross Margin %

```DAX
GM % := DIVIDE([Gross Margin],[Net Sales])
```

---

## 📊 Dashboard Features

### P&L Dashboard

Displays:

- Market-wise Net Sales
- COGS
- Gross Margin
- Gross Margin %

Interactive filters:

- Region
- Sub-Zone
- Fiscal Year

---

### GM% Analysis Dashboard

Displays:

- Quarterly GM%
- Sub-Zone performance
- Year-wise comparison

Interactive Fiscal Year filtering.

---

## 📈 Key Insights

- India generated the highest Net Sales.
- ROA and SE maintained the highest Gross Margin percentages.
- Margin performance varied across fiscal years and regions.
- Dashboard allows quick identification of profitable markets.

---

## 📷 Dashboard Screenshots

### P&L Dashboard

P & L Markets(https://github.com/muyeedbashir/-Profit-Loss-Analysis-Dashboard-using-Excel-Power-Pivot/blob/main/p%26l%20year.png)

### GM% Dashboard

GM% (subzone) (https://github.com/muyeedbashir/-Profit-Loss-Analysis-Dashboard-using-Excel-Power-Pivot/blob/main/Gm%25%20.png)

### Data Model

Data Model (https://github.com/muyeedbashir/-Profit-Loss-Analysis-Dashboard-using-Excel-Power-Pivot/blob/main/diagram%20view.png)


---

## 🚀 Skills Demonstrated

- Data Cleaning
- Data Transformation
- Power Query
- Data Modeling
- Power Pivot
- DAX Measures
- Financial Analysis
- Dashboard Design
- Business Intelligence Reporting

---

## 👤 Author

Muyeed Bashir

Economics Student | Aspiring Data Analyst

LinkedIn:
www.linkedin.com/in/muyeedbashir
