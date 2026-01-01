# US-Adidas-Sales-Report

# Project Overview

This Power BI dashboard provides a comprehensive analysis of Adidas USA sales performance across multiple dimensions such as time, region, product category, and sales method.
The report is designed to help stakeholders quickly monitor key performance indicators (KPIs), identify sales trends, and compare performance across channels and regions.

# Objectives
Track overall sales performance using key KPIs
Analyze sales trends over time (daily, monthly, yearly)
Compare sales by region, product, and sales method
Support data-driven decision-making with clear visual insights

# Data Model Overview

The dashboard is built using a star schema with the following tables:
Fact_sale – Transaction-level sales data
Dim_Date – Date attributes (Year, Month, Day)
Dim_Product – Product categories and types
Dim_retailer – Retailer and sales method details
Measure_data – DAX measures used for KPIs and visuals

# Measures Used (DAX Summary)

Key measures created in the report include:
Total_Sales
SUM(Fact_sale[Total_Sales])
AveragePrice
AVERAGE(Fact_sale[Price_per_Unit])
Sales YTD


TOTALYTD([Total_Sales], Dim_Date[Date])
Sales MTD
TOTALMTD([Total_Sales], Dim_Date[Date])
Total Units Sold
SUM(Fact_sale[Units_Sold])
Avg Operating Margin
AVERAGE(Fact_sale[Operating_Margin])

# Visuals Summary
1️ Sales Trend by Date (Line Chart)

Displays daily total sales
Helps identify peaks, drops, and seasonal patterns

2️ Sales by Sales Method (Donut Chart)
Breakdown of sales across:
In-store
Outlet
Online
Highlights dominant sales channels

3️ Sales by Region (Horizontal Bar Chart)
Compares performance between regions such as:
South
Northeast
Supports regional strategy planning

4️ Sales by Product (Column Chart)

Shows total sales for:
Men’s & Women’s Apparel
Athletic & Street Footwear
Identifies top-performing product categories
