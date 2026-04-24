# excel-dashboard-project--report-analysis
🛒 US Retail Sales Performance Dashboard
Power BI | Sales Analytics | Data Visualization
---
📌 Project Overview
This project analyzes 9,994 retail sales transactions from a US-based superstore (2014–2017) using Power BI. The goal was to uncover profitability patterns, regional performance differences, and product-level insights through an interactive 3-page dashboard.
---
🔍 Key Findings
💰 Total Revenue: $2.30M | Total Profit: $286.40K
📦 Tables sub-category generates negative profit despite high sales volume — a critical loss driver
🌍 West region leads in sales, but East region shows strong profitability
🖥️ Technology category is the most profitable category
🚚 59.72% of orders use Standard Class shipping
🏙️ New York City is the highest profit-generating city ($62,036)
📉 Higher discounts correlate with lower profit — especially in Furniture
---
📊 Dashboard Pages
Page 1 — Sales Overview
KPI Cards: Total Sales, Total Profit, Order Count, Customer Count
Sales by Region & Category (Clustered Bar Chart)
Monthly Sales & Profit Trend (Line Chart)
Top 10 Products by Sales (Bar Chart)
Ship Mode Distribution (Donut Chart)
Filters: Year Range (2015–2018), Customer Segment
Page 2 — Profitability Analysis
Profit by Sub-Category — reveals loss-making products
Profit by Supplier (Bar Chart)
Sales vs Profit by Supplier (Scatter Chart)
Discount vs Profit by Category (Line Chart)
Page 3 — Geographic Analysis
US Map — Profit by State & Region
City-level Profit Ranking Table
---
🗂️ Data Sources
Table	Source	Rows
Superstore_Sales_Clean	Kaggle — Sample Superstore Dataset	9,994
Product_Details	Supplementary product cost & supplier data	1,862
Takvim (Calendar)	DAX generated calendar table	—
> **Note:** The Superstore dataset is a widely-used demo dataset originally created by Tableau for educational purposes.
---
🔗 Data Model
```
Superstore_Sales_Clean
    └── Product ID ──── Product_Details (Many-to-One)
    └── Order Date ──── Takvim/Calendar (Many-to-One)
```
---
📐 DAX Measures
```dax
Toplam Satış = SUM('Superstore_Sales_Clean'[Sales])
```
```dax
Toplam Kâr = SUM('Superstore_Sales_Clean'[Profit])
```
```dax
Average Order Value = DIVIDE([Toplam Satış], DISTINCTCOUNT('Superstore_Sales_Clean'[Order ID]), 0)
```
---
🛠️ Tools & Techniques
Power BI Desktop — Dashboard design & visualization
Power Query — Data transformation & cleaning
DAX — Custom measures (Total Sales, Total Profit, Profit Margin)
Data Modeling — Table relationships (Many-to-One)
Map Visualization — US State & Region level geographic analysis
---
📁 Repository Structure
```
us-retail-sales-dashboard/
├── US_Retail_Sales_Dashboard.pbix
├── data/
│   ├── Superstore_Sales_Clean.xlsx
│   └── Product_Details.xlsx
├── screenshots/
│   ├── page1_overview.png
│   ├── page2_profitability.png
│   └── page3_map.png
└── README.md
```
---
👩‍💻 About
Buse | Industrial Engineer transitioning into Data Analytics
Connecting engineering mindset with data storytelling — this project applies efficiency and process thinking to retail sales analysis.


Dashboard created with Power BI Desktop. Dataset source: Kaggle.
