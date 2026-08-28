📊 E-Commerce Sales & Customer Analytics | Power BI






📌 Project Overview

This project presents an end-to-end Exploratory Data Analysis (EDA) of an e-commerce sales dataset using Microsoft Power BI.

The objective of the project is to transform raw transaction data into meaningful business insights by analyzing sales performance, customer behavior, product categories, discounts, profitability, returns, payment methods, delivery performance, and regional trends.

The project covers the complete analytics workflow:

Data Cleaning → Data Transformation → Data Modeling → DAX → Exploratory Data Analysis → Interactive Dashboard → Business Insights

📊 Dashboard Preview




The final dashboard provides an interactive overview of business performance using key performance indicators, sales trends, customer information, profitability analysis, and return behavior.

Users can interact with the dashboard using filters for dimensions such as year, region, product category, and customer demographics.

🛠️ Tools & Technologies
Microsoft Power BI Desktop
Power Query
DAX (Data Analysis Expressions)
Data Modeling
Exploratory Data Analysis (EDA)
Data Visualization
Business Intelligence
📂 Dataset

The dataset used in this project is the E-commerce Sales Transactions Dataset, obtained from Kaggle.

Dataset: E-commerce Sales Transactions Dataset
Platform: Kaggle
Creator: miadul
Size: Approximately 35,000 e-commerce transactions
Purpose: Educational, exploratory data analysis, and portfolio development
🔗 Dataset Source

https://www.kaggle.com/datasets/miadul/e-commerce-sales-transactions-dataset

All credit for the original dataset belongs to the dataset creator. The dataset was used in this project for educational and portfolio purposes.

Dataset Features

The dataset contains transaction, customer, product, delivery, and profitability information, including:

Order ID
Customer ID
Product ID
Product Category
Product Price
Discount
Quantity
Payment Method
Order Date
Delivery Time
Region
Return Status
Total Amount
Shipping Cost
Profit Margin
Customer Age
Customer Gender
🧹 Data Cleaning & Preparation

Data preparation was performed using Power Query before beginning the exploratory analysis.

The preparation process included:

Checking for missing and null values
Checking for duplicate transactions
Validating column data types
Cleaning and standardizing text columns
Inspecting numerical values for potential outliers
Validating customer age and transaction values
Preparing and formatting the order date
Creating customer age groups
Creating discount groups
Preparing the dataset for analysis and visualization
🗓️ Data Modeling

A dedicated Date Table was created to support time-based analysis.

The Date Table contains:

Date
Year
Month
Month Number
Quarter
Year-Month

A one-to-many relationship was created between:

DateTable[Date]

and

EcommerceDataset[order_date]

This model supports accurate time-based filtering and analysis across the Power BI report.

🧮 DAX Measures

Several DAX measures were created to calculate the main business KPIs.

Total Revenue
Total Revenue =
SUM(EcommerceDataset[total_amount])
Total Orders
Total Orders =
DISTINCTCOUNT(EcommerceDataset[order_id])
Total Customers
Total Customers =
DISTINCTCOUNT(EcommerceDataset[customer_id])
Total Quantity
Total Quantity =
SUM(EcommerceDataset[quantity])
Average Order Value
Average Order Value =
DIVIDE(
    [Total Revenue],
    [Total Orders],
    0
)
Average Delivery Days
Average Delivery Days =
AVERAGE(EcommerceDataset[delivery_time_days])
Returned Orders
Returned Orders =
CALCULATE(
    [Total Orders],
    EcommerceDataset[returned] = "Yes"
)
Return Rate
Return Rate =
DIVIDE(
    [Returned Orders],
    [Total Orders],
    0
)

Additional time-intelligence measures were created for analysis such as Previous Year Revenue and Year-over-Year Growth.

🔎 Exploratory Data Analysis

The analysis was divided into several areas to understand the dataset from different business perspectives.

1. Univariate Analysis

Individual variables were explored to understand their distributions and characteristics.

The analysis included:

Product categories
Customer demographics
Payment methods
Regions
Discounts
Delivery times
Returns
Transaction values
2. Bivariate Analysis

Relationships between variables were investigated to identify patterns and possible business relationships.

The analysis included:

Revenue vs. Product Category
Revenue vs. Region
Customer Age vs. Spending
Discount vs. Profit Margin
Delivery Time vs. Returns
3. Customer Analysis

Customer behavior and demographics were analyzed using:

Customer age
Customer age groups
Customer gender
Customer spending
Regional distribution

This analysis helps identify differences in purchasing behavior across customer segments.

4. Sales Analysis

Sales performance was explored across:

Months
Years
Product categories
Regions
Payment methods

The analysis was used to identify sales patterns and changes in revenue over time.

5. Discount & Profitability Analysis

The relationship between discount levels and average profit margin was investigated.

This analysis helps evaluate whether increasing discount levels are associated with changes in profitability.

6. Returns Analysis

Customer returns were analyzed across different dimensions, including:

Product category
Delivery performance
Region
Order characteristics

The goal was to identify areas associated with higher return rates.

📈 Executive Dashboard

The final Power BI dashboard provides an interactive overview of the most important business metrics and analytical findings.

Key Performance Indicators

The dashboard includes:

💰 Total Revenue
🛒 Total Orders
👥 Total Customers
💳 Average Order Value
↩️ Return Rate
Dashboard Visualizations

The executive dashboard includes:

Monthly Revenue Trend
Revenue by Product Category
Revenue by Region & Customer Gender
Orders by Payment Method
Discount Impact on Profit Margin
Return Rate by Product Category
Interactive Filters

Users can dynamically explore the dashboard using slicers for:

Year
Region
Product Category
Customer demographics

All dashboard KPIs and visualizations update based on the selected filters.

💡 Key Insights

The exploratory analysis revealed several notable patterns within the dataset:

Electronics generated substantially higher revenue than the other product categories.
Revenue performance varied across different geographic regions and customer groups.
The analysis showed a negative relationship between discount level and average profit margin, with higher discounts generally associated with lower average margins.
Customer orders were distributed across several payment methods, demonstrating variation in payment preferences.
Return rates differed across product categories, highlighting categories that may require additional investigation.
Monthly revenue showed fluctuations over time, allowing sales patterns to be explored across different periods.

These findings demonstrate how e-commerce transaction data can be transformed into meaningful business information using Power BI.

🎯 Business Recommendations

Based on the exploratory analysis, the following business recommendations can be considered:

Review discount strategies

Evaluate high-discount products and categories where increasing discounts are associated with declining profit margins.

Investigate high-return categories

Analyze products within categories showing higher return rates to identify possible issues related to product quality, customer expectations, pricing, or fulfillment.

Focus on high-performing categories

Continue monitoring strong-performing categories such as Electronics while identifying opportunities to improve lower-performing categories.

Monitor regional performance

Investigate the factors contributing to differences in revenue across regions and identify opportunities for regional growth.

Track monthly sales patterns

Use monthly revenue trends to support marketing, inventory, and sales planning decisions.

🔄 Project Workflow
Raw E-Commerce Dataset
        ↓
Data Profiling
        ↓
Data Cleaning
        ↓
Power Query Transformation
        ↓
Feature Engineering
        ↓
Data Modeling
        ↓
Date Table Creation
        ↓
DAX Measures
        ↓
Exploratory Data Analysis
        ↓
Interactive Dashboard
        ↓
Business Insights
        ↓
Business Recommendations
📁 Repository Structure

Ecommerce-PowerBI-EDA/
│
├── Ecommerce_Sales_Customer_Analytics.pbix
│
├── README.md
│
└── screenshots/
└── dashboard.png

The original dataset can be accessed through the Kaggle source provided above.

🎯 Skills Demonstrated

This project demonstrates practical experience with:

Power BI
Power Query
DAX
Data Cleaning
Data Transformation
Data Modeling
Exploratory Data Analysis
KPI Development
Data Visualization
Dashboard Design
Business Intelligence
Business Insights & Recommendations
👤 Author

Shatha Mansour

Data Science & Artificial Intelligence Graduate

Interested in opportunities related to Data Analytics, Business Intelligence, Data Science, and Artificial Intelligence.
