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
- **Total Profit**: SUM(Orders[Profit])
Shows the cumulative profit earned across all transactions. It’s the core profitability metric used throughout the report.

 - **Total Sales**:SUM(Orders[Sales])
Represents the total revenue generated from all product sales.

- **Profit Margin**: DIVIDE([Total Profit], [Total Sales], 0)
This ratio indicates how efficiently the company is converting sales into actual profit.

- **Average Discount**: AVERAGE(Orders[Discount])
Provides insight into the typical discount offered, helping assess the impact on profit.

- **Shipping Cost**: SUM(Orders[Shipping Cost])
Used to understand logistics expenses and their effect on profitability.

- **Rank by Profit**: RANKX(ALL(Country), [Total Profit])
Ranks countries or regions based on total profit, used to filter or highlight top performers dynamically.

- **Average Profit per City**: AVERAGEX(VALUES(City), [Total Profit])
Helps identify underperforming cities.

- **Orders Count**: COUNT(Orders[Order ID]):
Used to filter out cities with fewer than 10 orders in analyses.

---
### Few of the Questions Answered
- Question 1.

a) What are the three countries that generated the highest total profit for Global Superstore in 2014?

b) For each of these three countries, find the three products with the highest total profit. Specifically,
what are the products’ names and the total profit for each product?
- Question 2.

a) Identify the 3 subcategories with the highest average shipping cost in the United States.
- Question 3.

a) Assess Nigeria’s profitability (i.e., total profit) for 2014. How does it compare to other African
countries?

b) What factors might be responsible for Nigeria’s poor performance? You might want to investigate
shipping costs and the average discount as potential root causes.
- Question 4.

a) Identify the product subcategory that is the least profitable in Southeast Asia.
Note: For this question, assume that Southeast Asia comprises Cambodia, Indonesia, Malaysia, Myanmar
(Burma), the Philippines, Singapore, Thailand, and Vietnam.

b) Is there a specific country in Southeast Asia where Global Superstore should stop offering the
subcategory identified in 4a?
- Question 5.

a) Which city is the least profitable (in terms of average profit) in the United States? For this analysis,
discard the cities with less than 10 Orders. b) Why is this city’s average profit so low?
- Question 6.

a) Which product subcategory has the highest average profit in Australia?
- Question 7.

a)Who are the most valuable customers and what do they purchase?

---
### Visuals Breakdown
## 📊 Global Store Sales Dashboard

![Global Store Analysis](./Global%20store%20Analysis%201.png)

![Dashboard 2](./Global%20store%20Analysis%202%20png.png)

---
- **Question 1a**: Top 3 Countries by Profit

Chart: Bar Chart

X-axis: Total Profit

Y-axis: Country

Explanation: This visual dynamically displays the top 3 countries based on total profit using a calculated RANKX measure and slicer to filter only the highest performing markets.

Result: United States, India, and China were the top 3 countries by total profit.

- **Question 1b**: Top 3 Products by Country

Chart: Matrix

Row: Country

Column: Product Name (Filtered by top 3 using rank measure)

Values: Total Profit

Explanation: The matrix shows the top 3 most profitable products for each of the top 3 countries identified in 1a. A rank measure ensures only the top 3 products per country are shown.

Result: For instance, Binders and Copiers were top in the US, while India had other product combinations.

---
- **Question 2a**: Highest Average Shipping Cost by Sub-Category (U.S.)
Chart: Column Chart

X-axis: Sub-Category

Y-axis: Average Shipping Cost

Filters: Country = United States

Explanation: This chart identifies the top 3 product sub categories with the highest average shipping cost in the U.S. This helps pinpoint products that may be inflating logistics expenses.

Result: Copiers, Machines and Tables tend to have the highest average shipping costs in the U.S., likely due to their size and weight.

---
- **Question 3a**: Total Profit by country(Nigeria in the year 2014)

Chart: Filled Map

Location: Country

Tooltip: Total Profit

Explanation: This map visualizes total profit distribution globally, with Nigeria highlighted through a slicer for regional focus.

Result: When hovered, Nigeria’s profit is shown and visually contrasted with global data.

- **Question 3b**: Profit by Country (with Highlight)

Chart: Bar Chart/Cards

X-axis: Country

Y-axis: Total Profit

Explanation: KPIs were created to show Nigeria’s total profit separately. A duplicate chart was used without the slicer to compare with other countries. Nigeria is conditionally formatted for visual emphasis.

Result: Nigeria appears visibly lower, allowing easy comparison with higher profit countries.

---
- **Question 4a**:Product subcategory that is the least profitable in Southeast Asia.
 Chart: Bar Chart

X-axis: Country (Only 8 Southease Asia countries selected)

Y-axis: Total Profit

Filter: Country (limited to South-East Asia)

Explanation: To get the subcategory that is least profitable among selected southeast Asia countries.

Result: Products like Tables,Accessories and Supplies are least profitable with a negative value.

- **Question 4b**:  Is there a specific country in Southeast Asia where Global Superstore should stop offering the
subcategory identified in 4a?

Chart: Stacked Barchart

Y axis: Country

X axis: Total Profit

Filter: Sub-category which was filted to Table

Explanation: This visual shows the country with least profit of the item Table

Result: Some countries had products with negative profit, suggesting over-discounting or poor sales, countries like Indonesia,Thailand,Myanmar.

---
- **Question 5a**: Least Profitable US City (With ≥10 Orders)

Chart:   Table

Filter: Cities in the United States with at least 10 orders (via COUNTROWS)

Explanation: Aimed at identifying the least profitable city in the US based on average profit.

Result: Burlington was identified as the least profitable US city with an average profit of -300.24.

- **Question 5b**: Investigating Burlington’s Low Profitability

Visuals:

KPI Cards comparing Burlington's metrics with US average (e.g., profit, shipping cost, discount)

Product Profit Bar Chart: X-axis = Product Name, Y-axis = Total Profit

Explanation: This breakdown helps explain why Burlington performs poorly—highlighting excessive discounts, low sales, or unprofitable products.

Result: Burlington’s higher discounts and lower sales volume caused poor profit; some products generated consistent losses.  

---
- **Question 6**: Which product subcategory has the highest average profit in Australia? 
Chart: Column Chart
X axis: Sub category

Y axis: Total Profit

Filter: Country(Australlia)

Result: Appliances, Copiers and Phones  are the product subcategories with the highest  Average profit in Australlia.

---
- **Question 7**: Who are the most valuable customers and what do they purchase?
  
Chart: Table 

Row: Customer Name

Column: Sub category

Value: Total sales

Explanation: Displays the 5 top customers based on both sales and profit contribution, highlighting what was purchased and also the total sales.

Result: Customers like Tom Ashbrook, Jane Waco were high contributors in both sales and profit.

---
### Key Insights
- **Top Performers Identified**: The United States, India, and China lead in total profit, suggesting strong market presence and product-market fit.

- **Low-Performing Cities**: Burlington in the U.S. stands out as the least profitable city despite having over 10 orders—indicating operational or pricing inefficiencies.

- **Impact of Discounts**: In cities like Burlington, excessive discounts are correlated with low or negative profits, revealing an unsustainable pricing strategy.

- **Product-Specific Losses**: Some products consistently generate losses in specific regions highlighting the importance of localized product performance tracking.

- **Shipping Cost Burden**: High shipping costs are another contributing factor to poor profitability, especially in less accessible or remote cities.

- **Sales Concentration**: A few products contribute significantly to overall profits, underscoring the need to prioritize high-margin, high-demand products.

  ---
 ### Business Recommendations
- **Expand in Profitable Regions**: Increase investment, marketing, and inventory for high-performing countries (US, India, China) to capitalize on demand.

- **Revise Discount Policies**: Implement stricter discounting guidelines in loss-making cities; introduce data-driven pricing controls to protect margins.

- **Optimize Product Mix**: Discontinue or reevaluate poorly performing products in specific regions; focus on those with proven high profitability.

- **Improve Shipping Logistics**: Consider local warehousing or regional hubs to reduce delivery costs in low profit cities.

- **Tailor Regional Strategies**: Use regional dashboards to guide city-specific initiatives, aligning local campaigns with the most successful product segments.

- **Leverage Data Monitoring**: Regularly update dashboards and set alerts for declining profit trends to enable proactive management.

  ---
   ### Conclusion
This project has been an eye-opening journey into the power of data analytics. By diving deep into the Global Superstore dataset, I was able to uncover meaningful patterns from the countries generating the highest profits to cities struggling with performance due to factors like heavy discounts and high shipping costs. Using Power BI and DAX, I transformed raw data into clear, actionable visuals that tell a compelling business story. More than just numbers, this dashboard highlights how informed decisions can be made when insights are presented the right way. It’s a reminder that behind every dataset lies a story worth telling and with the right tools, we can bring that story to life.













