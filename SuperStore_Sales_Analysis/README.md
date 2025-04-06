Super Store Sales Analysis - Power BI Project
Overview:
This Power BI project presents a comprehensive Sales Dashboard for a global online 
retailer, Global Super Store, which operates across multiple regions and product 
categories like Furniture, Office Supplies, and Technology. The dashboard is designed
to help the Sales Manager analyze product performance, customer behavior, and regional
trends for better business planning.

Project Objective:
To build an interactive and insightful report using historical sales data that includes:
Product performance across different categories.
Regional profit contribution.
Manager-based access to data (RLS).
Q&A natural language analysis.
Interactive bookmarks for toggling visual content.

Features:
Report Pages
Sales Summary
KPIs: Total Sales, Total Profit, Profit Ratio

Charts:
Clustered Column Chart: Sales by Year & Category
Donut Chart: Sales by Category
Table: Region-wise Profit Contribution (with conditional formatting)
Tree Map: Category/Sub-category contribution
Stacked Bar Chart: Market-wise Sales
Bookmark Navigation: Toggle between Sales and Profit line charts
Q&A Analysis
Power BI Q&A visual for natural language queries

Trained synonyms:
"Revenue" = Sales
"Income" = Profit
"Income Percentage" = Profit Ratio
Map Visual: Sales by Country
Data Transformations
Cleaned and transformed multiple Excel files in Power Query Editor.
Promoted headers, removed unnecessary columns, and structured data relationships.

Measures Used:
Total Sales = SUMX(Orders, Orders[Unit Price] * Orders[Quantity])
Total Profit = SUM(Orders[Profit])
Profit Ratio = DIVIDE([Total Profit],[Total Sales],0)
As of Date = "Report as of date: " & Max(Orders[Order Date])
UserPrincipalName = USERPRINCIPALNAME()
Row-Level Security (RLS)
Static and Dynamic roles created based on region and email ID.
Implemented using USERPRINCIPALNAME() and a reference Country Access table.

Publishing:
Report was published to Power BI Service with proper RLS configurations.
Roles tested using “View as Role” and shared accordingly.

Tools Used:
Microsoft Power BI Desktop
Power Query Editor
DAX
Excel (for raw data and access control)

Author
Deepak Mahapatra
