# Retail_Sales_Performance

### Dashboard Link : https://app.powerbi.com/reportEmbed?reportId=40d15544-68f3-4751-9ec5-9f6213b9ef4c&autoAuth=true&ctid=3eb3d01e-9f8f-4b54-9885-92d3333f0d5c&actionBarEnabled=true&reportCopilotInEmbed=true
## Problem Statement

 Project Description
 Developed an end-to-end Power BI Business Performance Dashboard using an Excel
 dataset. Cleaned and transformed raw data in Power Query, built a star-schema data
 model, and created advanced DAX measures for sales, profit, customer insights, and
 time intelligence. Delivered interactive dashboards that support decision-making for
 product, customer, and regional performance
 
  1. Business Requirements
 Goal
 Build an interactive dashboard that helps management understand key trends such as
 sales, profit, product performance, customer behavior, and operational KPIs.
 Key Business Questions
 1. What is the total revenue, cost, and profit for the selected period?
 2. What are the top-performing products/categories?
 3. Which regions/customers contribute the most?
 4. What are month-over-month and year-over-year trends?
 5. Are there abnormal values or underperforming areas?
 ### Steps followed 
Data Preparation Steps

 Step 1 – Import Data
 Loaded Excel file into Power BI using Get Data → Excel.
 Inspected columns and detected data types automatically.
 
 Step 2 – Data Cleaning (Power Query)
 Removed empty rows and duplicates.
 Changed column types (Date → Date, Amount → Decimal).
 Split complex columns (e.g., "Full Name" → First/Last).
 Trimmed spaces and standardized category names.

  Step 3 – Create a Date Table
 You will write this DAX:
 DAX
 DateTable = 
ADDCOLUMNS (
    CALENDAR (DATE(2018,1,1), TODAY()),
    "Year", YEAR([Date]),
    "Month", FORMAT([Date], "MMM"),
    "Month Number", MONTH([Date]),
    "Quarter", "Q" & QUARTER([Date])
 )
 Mark the table as Date Table.
 
 Step 4 – Data Modeling
 Created relationships:
 Date Table → Fact Table using Date
 Products Table → Fact Table using ProductID
 Customers Table → Fact Table using CustomerID
 Set one-to-many and single-direction filters.

 Step 5 - DAX Measures 
 Basic KPIs-

 Total Sales ,
 Total Cost ,
 Total Profit
 Time Intelligence
 Sales LY  
 Top N, 
 Customer KPIs,
Customer Count ,
Avg Sales per Customer 
 
4. Dashboard Pages 
 Page 1 — Executive Overview
 Visuals:
 KPI Cards: Sales, Profit, Cost, Customer Count
 Line Chart: Sales by Month
 
 
 Bar Chart: Sales by Category
 Donut Chart: Sales % by Region
 Map: Sales by State/City
 
 Page 2 — Product Performance
 Matrix: Category → Subcategory → Product
 Top 10 Products by Sales
 Profitability Heatmap (High Profit vs Low Profit Items)
 
 Page 3 — Customer Insights
 Customer segmentation by:
 Geography
 Order Frequency
 Average Spend
 RFM-style table (Recency, Frequency, Monetary)
 
 Page 4 — Region/Store Analysis (If applicable)
 Map or filled map
 Region-level KPIs
 Store ranking
 
 Page 5 — Time Intelligence
 Month-over-Month change
 Year-over-Year growth
 Seasonality patterns (Monthly/Quarterly trends
 ![Executive Summary Report](https://github.com/user-attachments/assets/83fa0d21-d71a-4a70-a56c-1709a1f02cd8)
 ![Product Performance Report](https://github.com/user-attachments/assets/03affbff-7670-4d16-b056-2f85afd46882)
 ![Customer Insights Report](https://github.com/user-attachments/assets/4ed34138-0a08-4b97-b579-95eaef040499)
 ![Regional Analysis Report](https://github.com/user-attachments/assets/e25ca6d1-2246-413d-9166-3aab66da9e91)
 ![Time Intelligence   Forecast Report](https://github.com/user-attachments/assets/ed0da041-8f7f-4fea-b1f1-6233e373f407)
 
 












           
       
