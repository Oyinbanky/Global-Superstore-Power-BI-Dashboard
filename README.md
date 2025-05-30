# Global-Superstore-Power-BI-Dashboard
 An interactive Power BI dashboard analyzing Global Superstore sales data to uncover trends, identify high and low performing regions and products, and provide insights for improving profitability  trends within a global retail dataset through dynamic visuals, DAX-powered insights, and interactive dashboard.
### Project Description
Global Superstore is a global online retailer based in New York, boasting a broad product catalog and aiming to be a one-stop-shop for its customers. Global The superstore’s clientele, hailing from 147 different countries, can browse through an endless offering with more than 10,000 products. This large selection comprises three main categories: office supplies (e.g., staples), furniture (e.g., chairs), and technology (e.g., smartphones). The project is designed to help Global Superstore analyze and draw out meaningful insight from the Superstore dataset which would aid management in making informed decisions to improve performance and profitability by using data modeling, DAX measures, and interactive visuals, the dashboard helps identify the most and least profitable countries, cities, and product segments. The project also dives deep into underperforming locations (like Burlington, USA) to explore the root causes of low profit through metrics such as average discount, shipping cost, and sales volume. The insights derived aim to guide data driven decisions in marketing, product selection, and operational efficiency.

---
### Tools Used
- Power BI Desktop: The primary tool for data visualization and dashboard development. It was used for importing, cleaning, modeling, and visualizing the Global Superstore dataset.

- Power Query: Utilized for data transformation tasks such as filtering, merging, removing duplicates, creating custom columns, and applying conditional logic before loading data into the model.

- DAX (Data Analysis Expressions): Used extensively to create custom measures and calculated columns for KPIs like profit margin, average discount, ranking by profit, and filtering based on business rules (e.g., cities with more than 10 orders).

- Power BI Visualizations: A mix of bar charts, tables, filled maps, KPI cards, and matrix were used to create a visually engaging report. Conditional formatting and tooltips were used to enhance interactivity.

- Slicers and Filters: Dynamic slicers were added to allow users to explore data by region, country, and city. These slicers were also configured to isolate analysis in specific questions.

- GitHub: Used for project documentation.

   ---
 ### Dataset Information
- Source: Global Superstore Sample Dataset(Provided by Digitaley Drive)
- Fields: Order Date, Customer Name, Segment, Country, City, Region, Product Name, Sales, Profit, Discount, Quantity, etc.

  ---
  ### Dasboard Features
 - Slicer-enabled comparisons by country, region, and city

 - Highlighted KPIs: Total Sales, Total Profit, Profit Margin, Average Discount, Shipping Cost

 - Visual insights into top countries, underperforming cities, and product profitability

 - Dynamic charts powered by DAX measures and filters

   ---
   ### Some of the KPIs used and measures
- **Total Profit: SUM(Profit)**:
Shows the cumulative profit earned across all transactions. It’s the core profitability metric used throughout the report.

 - **Total Sales: SUM(Sales)**:
Represents the total revenue generated from all product sales.

- **Profit Margin**: Total Profit / Total Sales
This ratio indicates how efficiently the company is converting sales into actual profit.

- **Average Discount**: AVERAGE(Discount)
Provides insight into the typical discount offered, helping assess the impact on profit.

- **Shipping Cost**: SUM(Shipping Cost)
Used to understand logistics expenses and their effect on profitability.

- **Rank by Profit**: RANKX(ALL(Country), [Total Profit])
Ranks countries or regions based on total profit, used to filter or highlight top performers dynamically.

- **Average Profit per City**: AVERAGEX(VALUES(City), [Total Profit])
Helps identify underperforming cities.

- **Orders Count**: COUNTROWS('Orders'):
Used to filter out cities with fewer than 10 orders in analyses.

---
### Visuals Breakdown
## 📊 Global Store Sales Dashboard

![Global Store Analysis](./Global%20store%20Analysis%201.png)





