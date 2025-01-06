# Pizza Hut Sales Analysis using SQL and Power BI

## Project Overview

This project aims to perform a comprehensive sales analysis of Pizza Hut's business using SQL and Power BI. By analyzing sales data, we uncover valuable insights about sales trends, customer behavior, product performance, and more. This project utilizes SQL to query the raw sales data, followed by data visualization and interactive reporting in Power BI.

## Table of Contents

- [Project Overview](#project-overview)
- [Tech Stack](#tech-stack)
- [Data Source](#data-source)
- [Data Analysis with SQL](#data-analysis-with-sql)
- [Power BI Dashboard](#power-bi-dashboard)
- [Steps for Running the Project](#steps-for-running-the-project)
- [Key Insights](#key-insights)
- [Screenshots](#screenshots)
- [Conclusion](#conclusion)
- [Contributing](#contributing)

## Tech Stack

- **SQL**: Used for querying data from the database.
- **Power BI**: Used for creating interactive dashboards, visualizations, and reports.
- **Excel/CSV**: For input/output of data (in case of local data storage) and for data cleaning.
  
## Data Source

The dataset for this project is a simulated or anonymized sales dataset from Pizza Hut. The dataset includes transactional data, which includes:

- **Sales Date**: Date of the transaction.
- **Product ID**: Identifies the products sold.
- **Store ID**: Store location where the sale occurred.
- **Total Sale**: Amount of the sale.
- **Quantity Sold**: Number of units sold in each transaction.
- **Customer ID**: An identifier for the customer making the purchase (if applicable).
  
The dataset is just a sample(dummy) dataset created manually for the purpose of this analysis.

## Data Analysis with SQL

### Steps Performed:
1. **KPI's**: SQL was used to find the key performing indicators.
2. **Aggregations and Calculations**: Queries were created to calculate total orders by day, total orders by month, sales % by pizza category, sales % by pizza size, and more.
3. **Filtering and Grouping**: Utilized `GROUP BY`, `WHERE`, and `HAVING` clauses to analyze sales by different dimensions like time period, and product specifications.
4. **Performance Analysis**: Generated reports that show the highest-performing pizzas, and identified trends and patterns in sales over time.

### Some SQL Queries from this project:
```sql
-- List no. of pizzas sold by pizza category
SELECT pizza_category, SUM(quantity) as Total_Quantity_Sold
FROM pizza_sales
WHERE MONTH(order_date) = 2
GROUP BY pizza_category
ORDER BY Total_Quantity_Sold DESC

```

```sql
-- Find the top 5 pizzas with most revenue
SELECT Top 5 pizza_name, SUM(total_price) AS Total_Revenue
FROM pizza_sales
GROUP BY pizza_name
ORDER BY Total_Revenue DESC

```

## Power BI Dashboard

The data processed using SQL was imported into **Power BI**, where interactive dashboards and visualizations were created to explore and present the data. The Power BI dashboard's Home Page includes the following features:

1. **Sales Trends**: Area chart and Column chart showing sales performance over time (daily and monthly).
2. **Product Performance**: Doughnut charts depicting the sales percentage by pizza category and by pizza sizes.
3. **Revenue**: Total pizzas sold by each specefic pizza category
4. **Slicers**: pizza category slicer to understand sales by choosing particular category(s), and date slicer to see sales of particular time like a particular month or quarter.

And The Power BI dashboard's Best/Worst Seller Page has following features -  

1. **Top 5 Pizzas**: By Revenue , By Quantity Sold, and By Total Orders.
2. **Bottom 5 Pizzas**: By Revenue , By Quantity Sold, and By Total Orders.
3. **Sales Insights**: Total Revenue, Average pizzas per order, Average order value, Total pizzas sold.

### Key Features of the Power BI Report:
- Interactive slicers for filtering data by date, and pizza category.
- Trendline analysis to track sales growth and seasonality.
- Dynamic charts that update based on user input.

## Steps for Running the Project

### Prerequisites
To run this project, you'll need the following:
- **SQL Server** or any compatible SQL-based database tool (e.g., MySQL, PostgreSQL).
- **Power BI Desktop** installed on your local machine.

### Running SQL Queries:
1. Import the sales dataset into your SQL database (e.g., using `.csv` or `.xlsx` file).
2. Execute the provided SQL queries to clean, analyze, and aggregate data.
3. Export the cleaned data to CSV or connect directly to Power BI for reporting.

### Power BI Setup:
1. Open **Power BI Desktop**.
2. Import the processed dataset from SQL (via CSV or direct connection).
3. Use the imported data to create the various visualizations outlined above.
4. Publish the dashboard to Power BI service (optional) for sharing and collaboration.

## Key Insights

- **Sales Trends**: The analysis revealed a consistent spike in sales during certain holidays and weekends(friday and saturday evenings mostly), suggesting a seasonal pattern in demand.
- **Top Products**: Specific pizzas (e.g., "The Thai Chicken Pizza", and "Classic Deluxe Pizza") dominate sales, while "Brie Carre Pizza" showed lowest sales volumes.
- **Sales Performance by Pizza Size and Category**: Certain categories specially classic category had higher sales volume, alse Large Size pizzas had maximum sales.
- **Customer Behavior**: Analysis of repeat customers and average spend per order highlighted the importance of loyalty programs.

## Screenshots

![Power BI Dashboard](https://github.com/Ayushj321/Pizza-Hut-Analysis-using-SQL-and-PowerBI/blob/6619e471221e240652905dac1e609803b3e6e76e/Project%20Images/Screenshot%202025-01-06%20170136.png)

*Power BI Dashboard showing sales trends*


![Power BI dashboard](https://github.com/Ayushj321/Pizza-Hut-Analysis-using-SQL-and-PowerBI/blob/6619e471221e240652905dac1e609803b3e6e76e/Project%20Images/Screenshot%202025-01-06%20170304.png)

*Power BI dashboard shwoing Best/ Worst Selling Pizzas*

## Conclusion

This project demonstrates the power of combining SQL and Power BI for analyzing business data. By leveraging SQL to clean and process large datasets and Power BI for visualization, we were able to uncover meaningful insights into Pizza Hut's sales performance. These insights can be helpful for business stakeholders to optimize product offerings, improve sales strategies, and enhance customer experiences.

## Contributing

If you'd like to contribute to this project, feel free to fork the repository, make changes, and submit a pull request. Whether it's improving the analysis, adding more visualizations, or optimizing the code, all contributions are welcome!

### Steps for Contributing:
1. Fork the repository.
2. Create a new branch for your changes (`git checkout -b feature/your-feature-name`).
3. Make the necessary changes or improvements.
4. Commit your changes (`git commit -am 'Add new analysis/visualization'`).
5. Push your changes to your fork (`git push origin feature/your-feature-name`).
6. Open a pull request.
