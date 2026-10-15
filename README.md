# Superstore Sales & Profit Analysis | Power BI

An interactive Power BI dashboard designed to analyze retail sales performance, profitability, product categories, customer segments, shipping modes, and monthly sales trends.

## Project Overview

The objective of this project is to transform retail sales data into meaningful business insights using Microsoft Power BI. The dashboard helps users explore sales performance, compare product categories, identify top-selling sub-categories, and investigate profit contributions.

This project demonstrates practical skills in data preparation, data visualization, DAX calculations, and business reporting.
## Dashboard Preview

![Superstore Sales & Profit Dashboard](dashboard/superstore-sales-profit-dashboard.png)

## Business Objectives

- Analyze overall sales and profitability.
- Track monthly sales trends.
- Identify the highest-performing product categories and sub-categories.
- Compare sales across shipping modes and customer segments.
- Explore the relationship between discounts and profit.
- Investigate positive and negative profit contributions.
- Present key business metrics through an interactive dashboard.

## Tools & Technologies

- **Microsoft Power BI Desktop** — Dashboard development
- **Power Query** — Data cleaning and transformation
- **DAX** — Measures and KPI calculations
- **Data Visualization** — Business performance reporting

## Dataset Description

The dataset contains retail sales information used to analyze product performance, customer segments, shipping preferences, and profitability.

The fields used in the analysis include:

- Order Date
- Order ID
- Sales
- Profit
- Quantity
- Discount
- Category
- Sub-Category
- Region
- Market
- Segment
- Ship Mode

The dataset's original source and usage permissions should be documented before redistributing the raw data.

## Dashboard KPIs

The dashboard includes the following key performance indicators:

| KPI | Purpose |
|---|---|
| Total Sales | Measures overall sales value |
| Profit Margin (%) | Shows profit as a percentage of sales |
| Total Orders | Tracks order volume |
| Total Quantity Sold | Measures the quantity sold |

The KPI values depend on the data and filter context in the Power BI report.

## Dashboard Features

### 1. Sales Distribution by Ship Mode
A donut chart compares sales distribution across shipping modes.

### 2. Monthly Sales Trend
A line chart displays monthly sales performance and helps identify changes over time.

### 3. Top 5 Sub-Categories by Sales
A bar chart ranks the five highest-selling sub-categories.

### 4. Monthly Sales by Category
A matrix compares monthly sales across Furniture, Office Supplies, and Technology.

### 5. Sales Decomposition Tree
A decomposition tree allows sales to be explored by category, sub-category, and region.

### 6. Discount vs Profit — Furniture
A scatter chart helps examine the relationship between discounts and profit for Furniture products.

### 7. Orders by Customer Segment
A funnel chart compares order volume across Consumer, Corporate, and Home Office segments.

### 8. Profit Contribution by Category and Sub-Category
A waterfall chart displays positive and negative profit contributions.

### 9. Sales by Category
A bar chart compares sales across the main product categories.

## Key Findings

The following observations are based on the dashboard screenshot.

### 1. Technology Has the Highest Category Sales
Technology records approximately 4.7M in sales, followed by Furniture at approximately 4.1M and Office Supplies at approximately 3.8M.

### 2. Phones Leads the Displayed Top 5
Phones is the highest-selling sub-category in the displayed chart, with approximately 1.71M in sales. Copiers and Chairs follow.

### 3. Standard Class Has the Largest Sales Share
Standard Class represents approximately 59.95% of sales in the displayed shipping-mode chart.

### 4. Sales Change Across Months
The monthly trend shows fluctuations throughout the year, with sales increasing toward the end of the displayed period.

### 5. Profitability Requires Further Investigation
The dashboard reports a profit margin of 11.61%. The scatter and waterfall charts can help identify sub-categories that warrant further investigation into discounting and profitability.

*Note: These observations describe the displayed report state. Validate the relevant measures and filter context before comparing them with other reports or using them for business decisions.*

## Business Recommendations

- Review Technology's sales performance to understand which products contribute most to revenue.
- Evaluate profit alongside sales when comparing product categories.
- Investigate sub-categories with negative profit contributions.
- Examine discount levels and profitability together before changing pricing policies.
- Monitor monthly sales trends to support inventory and sales planning.
- Evaluate shipping-mode performance alongside cost and customer requirements.

These are recommendations for further analysis; the dashboard alone does not establish the causes of profit or sales changes.

## Data Preparation & Cleaning

Data preparation is an important step before building a reliable dashboard.

For this project, the data preparation workflow should document the transformations actually performed, such as:

- Reviewing column names and data types.
- Checking date and numeric fields.
- Reviewing missing or null values.
- Checking duplicate records where appropriate.
- Assessing the relevance of identifier fields such as Row ID.
- Confirming that Sales, Profit, Discount, and Quantity are suitable for analysis.
- Verifying that totals and measures behave correctly in Power BI.

The exact cleaning steps and data quality issues should be recorded based on the actual Power Query process, rather than assumed.

## DAX Measure

### Profit Margin %

```dax
Profit Margin % =
DIVIDE(
    SUM('RetailVista_Sales'[Profit]),
    SUM('RetailVista_Sales'[Sales]),
    0
)
```

Replace `'RetailVista_Sales'` with the actual table name in your Power BI model if necessary.

This measure calculates total profit divided by total sales and returns zero when the denominator is zero.

## How to Use This Project

1. Download or clone this repository.
2. Open the `.pbix` file using Power BI Desktop.
3. Review the dashboard visuals and KPI cards.
4. Explore the charts and available filters.
5. Review the README to understand the business objectives and findings.

If the report requires an external data source, update the data source path and refresh the report.

## Want to Build a Similar Project?

You can use this project as a learning reference to build your own Power BI sales dashboard.

**Recommended workflow:**

1. Obtain a dataset that you are permitted to use.
2. Inspect the raw data and understand the meaning of each column.
3. Import the dataset into Power BI.
4. Use Power Query to clean and prepare the data before building visuals.
5. Review missing values, duplicates, data types, and inconsistent records where relevant.
6. Create the required DAX measures and validate the results.
7. Build suitable KPIs and visualizations based on business questions.
8. Verify the dashboard totals against the prepared dataset.
9. Document your cleaning steps, analysis, findings, and limitations.
10. Publish your own report and document your work.

**Important:** Do not automatically delete every null value or duplicate. First determine whether it represents an actual data quality issue. Keep the original dataset unchanged and perform transformations in a separate working copy or through Power Query.

If you build on this project, use your own analysis and document the changes you make. Check the original dataset's licence and sharing conditions before uploading data publicly.

## Project Files

Recommended repository structure:

```text
superstore-sales-profit-analysis/
├── README.md
├── Superstore_Sales_Profit_Analysis.pbix
└── screenshots/
    └── dashboard.png
```

Include the dataset only when its licence permits redistribution.

## Skills Demonstrated

- Power BI dashboard development
- Power Query data preparation
- DAX measures
- KPI design
- Sales and profitability analysis
- Trend analysis
- Category and sub-category comparisons
- Interactive reporting
- Business insight communication

## Conclusion

This project demonstrates how retail sales data can be analyzed using Power BI to understand sales trends, compare product performance, monitor profitability, and explore areas for further business investigation.

It provides a foundation for developing interactive reports that support data-driven decision-making.

