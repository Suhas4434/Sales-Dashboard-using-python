📊 Superstore Sales Performance & Insights Dashboard
🚀 Project Overview

This project presents an end-to-end sales data analysis and interactive business intelligence dashboard built using Python (Pandas, Matplotlib, Seaborn) and Power BI.
The objective of this project is to:
Analyze sales trends
Identify top-performing products and regions
Detect sales outliers
Evaluate profitability and discount impact
Build an interactive executive dashboard for business insights
The project demonstrates real-world data cleaning, exploratory data analysis (EDA), feature engineering, time intelligence, and advanced DAX modeling.

📁 Project Structure
📦 Superstore-Sales-Analytics
│
├── sales_analysis.ipynb
├── cleaned_sales_data.csv
├── monthly_sales_trend.png
├── sales_by_region.png
├── PowerBI_Dashboard.pbix
└── README.md

🧾 Dataset Information
Dataset Source: Kaggle – Superstore Sales Dataset
Key Columns Used:
Order Date
Sales
Profit
Region
Product Name
Category
Sub-Category
Discount
Quantity
Customer ID

🧹 Data Cleaning & Preparation (Python)
The following steps were performed:

1️⃣ Data Loading
df = pd.read_csv("sales_data.csv")

2️⃣ Data Inspection
Checked shape
Verified column names
Checked data types

3️⃣ Handling Missing Values
Removed null values
Verified completeness

4️⃣ Removed Duplicates
df = df.drop_duplicates()

5️⃣ Converted Date Column
df['Order Date'] = pd.to_datetime(df['Order Date'])

6️⃣ Feature Engineering
Created Month
Created Year
Created Profit Margin

7️⃣ Outlier Detection
Used 99th percentile method to remove extreme values.

8️⃣ Saved Cleaned Dataset
df_clean.to_csv("cleaned_sales_data.csv", index=False)

📊 Python Visualizations
📈 Monthly Sales Trend

Line chart showing revenue trend over time
Identifies seasonality and growth

📊 Sales by Region
Bar chart comparing regional performance

📊 Power BI Dashboard
🟢 Executive KPIs
Total Sales
Total Profit
Profit Margin %
Total Orders
Average Order Value
YoY Growth %

📈 Trend Analysis

Monthly Sales Trend
Year-over-Year Growth
YTD Sales

🏆 Top Performers

Top 5 Products by Sales
Sales by Region
Category Performance

📉 Advanced Insights
Discount vs Profit Analysis (Scatter Chart)
Loss Orders %
Sales per Customer
Customer Contribution Analysis

📐 DAX Measures Used
Core Measures
Total Sales = SUM('cleaned_sale_data'[Sales])
Total Profit = SUM('cleaned_sale_data'[Profit])
Total Orders = DISTINCTCOUNT('cleaned_sale_data'[Order ID])
Profit Margin % = DIVIDE([Total Profit], [Total Sales]) * 100
Average Order Value = DIVIDE([Total Sales], [Total Orders])

Advanced Time Intelligence
YTD Sales = TOTALYTD([Total Sales],'cleaned_sale_data'[Order Date])

Previous Year Sales =
CALCULATE([Total Sales],
SAMEPERIODLASTYEAR('cleaned_sale_data'[Order Date]))

YoY Growth % =
DIVIDE([Total Sales] - [Previous Year Sales],
[Previous Year Sales]) * 100

📌 Key Business Insights

1️⃣ Sales show consistent upward growth with peak performance during Q4 months.
2️⃣ West region generates the highest revenue contribution.
3️⃣ A small group of products contributes disproportionately to total sales.
4️⃣ High discount levels significantly reduce profitability.
5️⃣ Some categories generate high revenue but lower profit margins.

🧠 Skills Demonstrated

Data Cleaning & Preprocessing
Exploratory Data Analysis (EDA)
Outlier Detection
Feature Engineering
Data Visualization
Business Insight Generation
DAX & Time Intelligence
Interactive Dashboard Design

🛠 Tools & Technologies

Python
Pandas
Matplotlib
Seaborn
Power BI
DAX

🎯 Business Impact
This dashboard enables stakeholders to:
Monitor revenue performance
Identify profitable and loss-making segments
Evaluate discount strategies
Compare regional performance
Make data-driven strategic decisions

📎 How to Run the Project
Python Analysis
Open sales_analysis.ipynb
Run all cells

Cleaned dataset will be generated
Power BI Dashboard
Open PowerBI_Dashboard.pbix
Refresh data if required

📈 Future Improvements
Forecasting sales trends
Customer RFM analysis
Dynamic KPI selection
Drill-through detail pages
Profitability optimization modeling

👤 Author
Suhas K

Data Analytics Enthusiast
Focused on Python, Power BI, and Business Intelligence

⭐ Final Note
This project demonstrates the complete data analytics lifecycle — from raw dataset to executive-level dashboard — integrating Python analysis with Power BI visualization for actionable business insights
