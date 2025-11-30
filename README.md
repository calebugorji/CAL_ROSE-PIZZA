# CAL_ROSE-PIZZA 
## Project Overview
  This data analysis project aims to provide insights into the sales performance of a pizza company over the past year. By analyzing various aspects of the sales data , we seek to identify trends , make data driven recommendation and gain a deeper understanding of the company's performance.

  ## Data Sources
  sale data: The primary dataset used for this analysis is the " pizza_sales csv " file containing detailed information about each sales made by the company.
  ["https://github.com/calebugorji/CAL_ROSE-PIZZA/blob/main/pizza_sales.csv"]

  ## Tools
  - SQL Server - Data analysis
  - PowerBi - Creating report

## Exploratory Data Analysis
 EDA involved exploring the sales data to answer key questions such as :
 - Total revenue
 - Average order value
 - Which products are the top sellers ?
 - What are the peak sales periods ?

   ## Data Analysis
   include some interesting code/features worked with
   ```SQL
   select *
   from pizza_sales;

   select COUNT(distinct order_id) as total_order
   from pizza_sales;

   select SUM(total_price) / 1000 as total_revenue
   from pizza_sales;

   select SUM(quantity) as total_pizza_sold
   from pizza_sales;

   select SUM(order_total) / COUNT(*) as Average_order_value
   from (
   select order_id,
         SUM(quantity * unit_price) as order_total 
   from pizza_sales
   group by order_id 
   ) as orders;

   select COUNT(*) * 1.0 / COUNT(distinct order_id) as Average_pizza_per_order
   from pizza_sales;

  ## Dashboard
  https://github.com/calebugorji/CAL_ROSE-PIZZA/blob/main/Cal_Rose%20dashboard.png

  ## Result/Findings
  The analysis results are summarized as follows
  1. The company's sales have been steadily increasing over the past year , with a noticable peak during the summer period.
  2. The classic pizza is the best-performing category in terms of sales and revenue.
  3. peak sales were made mostly at mid-day.

## Recommendations
Based on the analysis , we recommend the following actions 
- Invest in marketing and promotions during peak sales seasons to maximize revenue.
- Focus on expanding and promoting the classic pizza.
- Ensure that the quality of other pizza categories are looked into in order to improve their sales. 
