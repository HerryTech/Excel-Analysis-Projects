# Sales Performance and Profitability Analysis for a Brazilian E commerce Marketplace

## Project Overview

This project is an interactive Excel-based Business Intelligence dashboard analyzing sales performance and profitability for a Brazilian e-commerce marketplace.

The dashboard provides a comprehensive view of:

- Revenue performance over time
- Order volume trends
- Customer activity
- Product category contribution
- Regional (state-level) revenue distribution
- Payment behavior patterns

Built entirely in Microsoft Excel using Pivot Tables, Power Pivot, and DAX measures, this project demonstrates advanced analytical modeling and executive-level dashboard reporting.

## Dashboard Preview

![Sales Performance Dashboard](./Image/Brazilian_Ecommerce.png)

### KPI Summary

- **Total Revenue:** R$ 14,221,705  
- **Total Orders:** 99,441  
- **Total Customers:** 96,096  
- **Average Order Value (AOV):** R$ 143  

All KPIs dynamically update based on slicer selections.

## Dataset

**Source:** Brazilian E-Commerce Marketplace Dataset (Kaggle) 
**Period Covered:** 2016 – 2018  

### Key Tables:
- Customers
- Orders
- Order Items
- Products
- Payments

### Key Columns:
- Order ID
- Customer ID
- Order Date
- Product Category
- Payment Type
- Order Status
- Revenue
- State

## Data Cleaning & Preparation

The dataset was transformed and structured before loading into the Data Model.

### Cleaning Steps:
- Removed duplicate order IDs
- Validated revenue calculations
- Standardized product categories
- Created Year and Month hierarchy
- Grouped order statuses
- Structured relational model (Orders ↔ Customers ↔ Products)
- Loaded tables into Power Pivot Data Model

## Technical Implementation

### Tools & Features Used

- Excel Pivot Tables
- Power Pivot (Data Model)
- DAX Measures
- Time Intelligence Calculations
- Slicers (Year, Month, Product Category)
- KPI Cards
- Donut Charts
- Bar & Column Charts

## Key DAX Measures

### Total Revenue
```DAX
Total Revenue :=
SUM(Order_Items[Revenue])
```

### Total Orders
```DAX
Total Orders :=
DISTINCTCOUNT(Orders[OrderID])
```

### Average Order Value
```DAX
AOV :=
DIVIDE([Total Revenue], [Total Orders])
```

### Total Customers
```DAX
Total Customers :=
DISTINCTCOUNT(Customers[CustomerID])
```

## Dashboard Components

### 1. Sales Trend Over Time
- Monthly revenue tracking
- Identifies growth and seasonal trends
- Highlights peak sales periods

### 2️.  Revenue by Product Category
- Home & Furniture leads
- Health & Beauty and Sports follow
- Identifies high-performing product lines

### 3️.  Order Status Distribution
- Majority Delivered (~97%)
- Minimal cancellations
- Operational performance insight

### 4️. Payment Type Analysis
- Credit Card dominates (~78%)
- Boleto and Debit Card secondary
- Customer payment preference insights

### 5️. Revenue vs Number of Orders
- Category-level performance comparison
- Identifies high-volume vs high-value categories

### 6️. Top 10 Revenue by State
- São Paulo dominates revenue
- Rio de Janeiro and Minas Gerais follow
- Regional revenue concentration analysis

##  Key Insights

- Revenue growth accelerated significantly between 2016 and 2018
- Credit card is the dominant payment method
- São Paulo generates the highest marketplace revenue
- Home & Furniture is the top-performing product category
- High delivery success rate indicates strong logistics performance

## Business Value

This dashboard supports:

- Revenue performance monitoring
- Regional expansion strategy
- Product category optimization
- Payment behavior analysis
- Operational efficiency evaluation
- Executive-level reporting

## Skills Demonstrated

- Advanced Excel Dashboard Design
- Relational Data Modeling
- DAX Calculations
- Time Intelligence Analysis
- KPI Development
- Business Performance Analysis
- Data Visualization Best Practices
- Analytical Storytelling

## How to Use

1. Download the Excel file
2. Open using Excel 2019 or later
3. Enable content if prompted
4. Use slicers to filter by:
   - Year
   - Month
   - Product Category

All visuals and KPIs update dynamically.

## Project Purpose

This project demonstrates the ability to:

- Analyze multi-table transactional data
- Build a structured relational data model
- Apply DAX for KPI engineering
- Translate sales data into actionable business insights
- Design executive-ready dashboards in Excel
