OLIST E-Commerce 360° Sales, Profit & Business Intelligence Dashboard

📊 Project Overview

An end-to-end Power BI business intelligence project built on the Brazilian Olist E-Commerce dataset (2016–2018) containing 99K+ orders.

The objective was to transform raw e-commerce data into an interactive, CEO-friendly dashboard that answers key business questions around revenue, profitability, customers, products, logistics, and time-based sales performance.

🛠️ Tools & Technologies

Power BI Desktop

Power Query

DAX

Data Modeling

CSV datasets

Interactive dashboards and visual analytics

📁 Final Power BI File

Olist E-commerce.pbix

🎯 Business Objectives

The dashboard was designed to answer questions such as:

How much revenue and profit is the business generating?

Which states and customer regions contribute the most revenue?

Which product categories are most profitable?

When do customers purchase the most?

What are the peak months, days, and hours?

How does delivery performance relate to customer reviews?

Where are potential business and logistics problems?

🗂️ Dataset

The project uses the Olist Brazilian E-Commerce public dataset (2016–2018).

Data Model

The model contains:

9 original Olist CSV tables

1 DimDate table

Orders as the central transactional table

Relationships created in Power BI Model View

The DimDate table covers:

2016-01-01 → 2018-12-31

Total date rows:

1,095

🔄 Data Preparation & Modeling

Step 1 — Data Loading

All 9 CSV files were imported into Power BI using Get Data.

Step 2 — Power Query Transformation

Data preparation included:

Correcting date and data types

Handling null values where appropriate

Removing duplicates where required

Preparing fields for analysis

Creating consistent columns for modeling

Step 3 — Data Modeling

Relationships were created in Model View, with the orders table acting as the central transactional table.

Step 4 — Date Dimension

A dedicated DimDate table was created with:

Date

Year

MonthNo

MonthName

Quarter

Day Number

Day Name

This enabled reliable time-based analysis.

🧮 DAX Measures

Key measures created for the dashboard include:

Total Revenue

Total Revenue =
SUM(order_items[price])

Total Orders

Total Orders =
COUNTROWS(orders)

Average Order Value

Avg Order Value =
DIVIDE([Total Revenue], [Total Orders])

Additional measures were created for profitability and dashboard-specific analysis.

Note: Measure definitions should be kept consistent with the final .pbix model when this README is maintained.

📑 Dashboard Pages

The final report contains 7 interactive pages:

1. Executive Overview

High-level business KPIs and overall performance.

2. Profitability

Analysis of revenue, profit, and category-level profitability.

3. Revenue By Customer

Customer geography and revenue contribution analysis.

4. Sales Performance

Sales trends and business performance across key dimensions.

5. Product Category Analysis

Category and product-level revenue/profitability analysis.

6. Logistics

Delivery performance and customer-review relationships.

7. Time Analysis

Revenue and order patterns across years, months, days, and hours.

⏱️ Time Analysis

The Time Analysis page was built to identify purchasing patterns.

Revenue by Year

Axis: DimDate[Year]

Value: Total Revenue

Revenue by Month

Axis: DimDate[MonthName]

Value: Total Revenue

Sorting: MonthName sorted by MonthNo

This prevents months from appearing alphabetically.

Revenue by Day

Axis: DimDate[Day Name]

Value: Total Revenue

Sorted using the appropriate day-order column.

Orders by Hour

An Hour column was derived from:

order_purchase_timestamp

using the hour component of the timestamp.

The resulting visual analyzes order activity across 0–23 hours.

Year-Month Trend Table

The trend table uses:

Year

MonthName

Revenue

Orders

The data is sorted chronologically using Year and MonthNo.

🧩 Challenges & Solutions

Challenge 1 — Months Appearing Alphabetically

Problem:
January, February, March, etc. can appear in alphabetical order when MonthName is treated as normal text.

Solution:
Created a numeric MonthNo column and used:

Sort by Column → MonthNo

Challenge 2 — Incorrect Day Ordering

Problem:
Day names can also appear alphabetically.

Solution:
Used a numeric day-order column and sorted the day-name field accordingly.

Challenge 3 — MonthName Data Type Warning

Problem:
Power BI can show a warning if a text month-name field is incorrectly converted to a numeric type.

Solution:
MonthName remains Text.

Only MonthNo is stored as Whole Number and is used for sorting.

Challenge 4 — Hour-Level Analysis

Problem:
Power BI requires a usable hour value for hourly analysis.

Solution:
The hour was extracted from:

order_purchase_timestamp

This created an hour value from 0 to 23 for the Orders by Hour analysis.

💡 Key Business Insights

The dashboard revealed several notable patterns:

São Paulo (SP) contributes approximately 42% of revenue, making it the dominant state in the analyzed sales data.

Health & Beauty and Watches & Gifts are among the strongest categories from a profitability perspective.

Order activity is strongest during the 2 PM–10 PM period.

Delivery delays exceeding 7 days are associated with lower customer review scores, highlighting a potential logistics/customer-satisfaction relationship.

Insights are based on the final dashboard analysis and should be interpreted within the scope of the Olist dataset.

📈 Dashboard Capabilities

The report includes:

KPI cards

Time-series analysis

Category analysis

Geographic analysis

Profitability analysis

Customer analysis

Logistics analysis

Interactive slicers

Tables and charts

Drill/filter-based exploration

Business-focused visual storytelling

🧠 Skills Demonstrated

This project demonstrates practical experience with:

Power BI Desktop

Power Query

DAX

Data Cleaning

Data Transformation

Data Modeling

Relationships

Date Tables

Time Intelligence

KPI Development

Business Analytics

E-Commerce Analytics

Data Visualization

Dashboard Design

Business Insight Generation

🚀 Project Workflow

Raw Olist CSV Files
        ↓
Power Query
        ↓
Data Cleaning & Transformation
        ↓
Data Model & Relationships
        ↓
DimDate Creation
        ↓
DAX Measures
        ↓
Interactive Visualizations
        ↓
7-Page Power BI Dashboard
        ↓
Business Insights

📌 Project Outcome

The final result is an interactive Olist E-Commerce Business Intelligence Dashboard that converts raw transactional data into actionable insights across:

Revenue → Profitability → Customers → Products → Logistics → Time

The project demonstrates an end-to-end BI workflow rather than only dashboard creation: data preparation, modeling, DAX, visualization, analysis, and business storytelling.

👤 Author

Divyam Khajuria

B.Tech CSE Graduate | Aspiring AI/ML & Data Professional

🔗 LinkedIn: linkedin.com/in/divyam-khajuria-76a930296
🔗 GitHub: github.com/divyamkhajuria4-glitch

⭐ If you find this project useful

Feel free to explore the dashboard, review the data model and DAX measures, and share feedback.
