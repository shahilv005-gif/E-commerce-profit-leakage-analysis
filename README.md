# E-commerce Revenue Leakage Analysis
Overview

I built this project to understand where revenue is being lost in an e-commerce order journey and to turn transaction-level data into actionable business insights.
The analysis focuses on GMV, cancellations, returns, order status, product categories, sizes, sales channels, and geographical performance.

The main goal was not just to build a Power BI dashboard, but to answer a practical business question:
Where is the business losing revenue, how significant is the leakage, and where should we investigate further?

Business Problem
In an e-commerce business, generating sales is only part of the story. Cancellations, returns, rejected orders, and other unsuccessful order outcomes can reduce the revenue that is ultimately retained.

A large transaction dataset can make it difficult to identify:

- How much GMV is being lost
- How much revenue is retained
- Whether cancellation rates are within the expected target
- Which categories contribute most to cancelled GMV
- Whether certain sizes have higher cancellation rates
- Which regions have higher cancellation rates
- Whether particular sales channels or order outcomes require further investigation

This project was created to provide a single analytical view of these areas.
Project Objectives

The analysis was designed to:
1. Measure overall GMV and net revenue.
2. Quantify cancelled and returned GMV.
3. Calculate cancellation rate and compare it with a target.
4. Understand leakage across different order-status groups.
5. Identify product categories contributing to higher cancelled GMV.
6. Analyze cancellation patterns across product sizes.
7. Identify geographical variations in cancellation performance.
8. Provide a management-friendly dashboard for further investigation.

Dataset

The dataset contains e-commerce order and sales information.

-: Some of the important fields used in the analysis include:
- Order ID
- Amount
- Quantity
- Category
- Size
- Style
- SKU
- ASIN
- Order Status
- Status Group
- Sales Channel
- Fulfilment
- Courier Status
- Ship State
- Ship City
- Ship Country
- Date
- Month
- Promotion information

The project uses both the original dataset and a cleaned dataset prepared for analysis.
Data Preparation
Before building the dashboard, the data was reviewed and prepared for analysis.

The preparation process included:
- Cleaning inconsistent values
- Reviewing order-status categories
- Handling duplicate/inconsistent records
- Standardizing fields used for analysis
- Creating analytical status groups
- Preparing date and month fields
- Creating cancellation-related indicators
- Preparing the dataset for Power BI

The purpose of this stage was to make the data consistent enough to support reliable KPI calculations and visual analysis.

Tools Used
- **Microsoft Excel** — Data cleaning and preparation
- **Power BI** — Data modeling, visualization, and dashboard development
- **DAX** — Business metrics and KPI calculations
- **GitHub** — Project versioning and documentation

Key Metrics

The Power BI model contains measures for the main business KPIs, including:

- **Total GMV**
- **Net Revenue**
- **Cancelled GMV**
- **Returned GMV**
- **Cancel Rate**
- **Target Cancel Rate**
- **Leakage GMV**
- **Other Leakage**

These measures were created to move from simple transaction reporting toward business-focused analysis.

Analysis Areas

1. Executive Performance
The dashboard provides a high-level view of overall business performance through:

- Total GMV
- Net Revenue
- Cancelled GMV
- Cancellation Rate
- Target Cancellation Rate
- Revenue/leakage movement
- Order-status performance

This section is designed to give management a quick understanding of the overall situation before drilling into specific problem areas.

2. Leakage Analysis
Order outcomes are grouped into meaningful leakage stages to understand how GMV changes throughout the order journey.
The analysis considers outcomes such as:
- Cancelled orders
- Returned orders
- Other leakage
- Delivered/retained revenue

The purpose is to understand the financial impact of unsuccessful order outcomes rather than looking only at order counts.

3. Merchandise Analysis
Product-level analysis uses fields such as:
- Category
- Size
- Style
- SKU

The analysis focuses on questions such as:

- Which categories contribute the most cancelled GMV?
- Which category/size combinations have higher cancellation rates?
- Where is the financial impact concentrated?

This helps move the analysis from overall performance toward potential product-level causes.

4. Regional Analysis
The dataset contains geographical fields such as state, city, and country.

Regional analysis can be used to identify:

- States with higher cancelled GMV
- States with higher cancellation rates
- Differences in order volume
- Locations that may require further investigation

The objective is to identify geographical patterns rather than assuming that overall performance is consistent across regions.

DAX & Business Logic

DAX measures were created to calculate the main KPIs and support the leakage analysis.

Examples include measures for:

- Total GMV
- Cancelled GMV
- Cancel Rate
- Net Revenue
- Returned GMV
- Leakage GMV
- Target Cancel Rate
- Leakage funnel calculations
- Waterfall status calculations

The detailed DAX formulas will be documented separately so that the business logic behind the dashboard can be reviewed.

Business Insights

The dashboard is designed to identify areas such as:

- Categories with a high financial contribution to cancelled GMV
- Product sizes associated with higher cancellation rates
- States with relatively high cancellation rates
- The contribution of cancellations and returns to overall leakage
- The gap between actual cancellation performance and the defined target

The final insights should be interpreted together with order volume and financial impact rather than relying on cancellation rate alone.

Business Recommendations

Potential areas for further investigation include:

- Investigating categories with disproportionately high cancelled GMV
- Reviewing size-level cancellation patterns for potential product or sizing issues
- Investigating regions with consistently high cancellation rates
- Monitoring cancellation rate against the target
- Prioritizing leakage areas based on financial impact
- Using order-status patterns to identify where in the order journey losses are occurring

These recommendations are intended as investigation areas rather than assumptions about the root cause

Project Structure

E-commerce-profit-leakage-analysis/
│
├── README.md
│
├── PowerBI/
│   └── Ecommerce_Profit_Leakage_Analysis.pbix
│
├── Dataset/
│   ├── Ecommerce_Sales_Data.xlsx
│   └── Ecommerce_Sales_Data.csv
│
├── Dashboard/
│   └── Dashboard_Screenshots/
│
└── Documentation/
    └── DAX_Measures.md
