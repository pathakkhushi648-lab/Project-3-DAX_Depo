Sales Performance Dashboard (Power BI)

Overview

This project presents a professional Sales Performance Dashboard developed using Power BI. It focuses on analyzing key business metrics such as sales, profit, cost, and quantity to support data-driven decision-making.

The dashboard is designed to provide clear, interactive, and insightful visualizations for understanding business performance across different dimensions.

Objectives

The main objectives of this project are:

* Analyze overall sales, profit, and cost performance
* Track monthly, quarterly, and yearly trends
* Identify top-performing products
* Compare regional and customer segment performance
* Monitor Year-To-Date (YTD) sales trends


Dashboard Highlights

Key Performance Indicators

* Total Sales: 848K
* Total Profit: 162K
* Average Sale: 848.40
* Total Quantity: 2995

These KPIs provide a quick summary of business performance.

Visual Analysis

Sales and Profit Trend
A combined line and column chart that shows sales and profit trends across months, quarters, and years.

Product Performance Table
A matrix visual displaying product-level insights including sales, profit, cost, and running totals.

Category Analysis
A donut chart representing distribution of sales across categories such as Electronics, Home Appliances, Books, Clothing, and Toys.

Regional and Segment Analysis
A bar chart comparing sales across regions (Central, North, West, South, East) and customer segments (Corporate, Retail, SMB).

YTD Sales Trend
A line chart that highlights year-to-date sales performance and monthly progression.


Filters and Interactivity

* Region-based slicer for dynamic filtering
* Interactive visuals with hover-based insights
* Easy navigation across different business dimensions


DAX Calculations

Basic Measures

Total Sales = SUM(Sales_Fact[SalesAmount])

Total Profit = SUM(Sales_Fact[SalesAmount]) - SUM(Sales_Fact[Cost])

Average Sale = AVERAGE(Sales_Fact[SalesAmount])

Total Quantity = SUM(Sales_Fact[Quantity])


Time Intelligence Measures

YTD Sales = TOTALYTD([Total Sales], Date_Dim[Date])

Running Total =
CALCULATE(
[Total Sales],
FILTER(
ALL(Date_Dim),
Date_Dim[Date] <= MAX(Date_Dim[Date])
)
)


Data Model

The dashboard is built using a star schema model:

* Sales_Fact: Contains transactional data
* Product_Dim: Product-related information
* Customer_Dim: Customer details
* Region_Dim: Regional classification
* Date_Dim: Date and time attributes

Relationships are established between the fact and dimension tables to enable efficient filtering and analysis.


Design Approach

* Dark theme with contrasting highlights for better readability
* Structured layout for intuitive navigation
* Focus on clarity and minimalism
* Emphasis on key metrics and trends


Insights

The dashboard enables users to:

* Identify top-performing products and categories
* Compare sales performance across regions
* Analyze customer segment behavior
* Monitor trends over time
* Detect patterns in sales growth and returns


Tools and Technologies

* Power BI Desktop
* DAX (Data Analysis Expressions)
* Data Modeling techniques


Usage Instructions

1. Open the Power BI (.pbix) file
2. Refresh the dataset if required
3. Use slicers to filter data dynamically
4. Interact with visuals to explore insights

Author

Swarna Ajay Pathak
Power Bi..
