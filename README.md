# Pizza Sales Analysis

## Project Description
This project provides an in-depth analysis of pizza sales data using Power BI and SQL queries. The objective is to extract meaningful insights, track key performance indicators (KPIs), and visualize trends in sales performance.

## Features
- Key performance indicators (KPIs):
  - Total Revenue
  - Average Order Value
  - Total Pizzas Sold
  - Total Orders
  - Average Pizzas per Order
- Sales trends analysis:
  - Daily order trends
  - Hourly order trends
  - Percentage of sales by pizza category
  - Percentage of sales by pizza size
  - Top 5 and bottom 5 best sellers

## Installation and Usage

### Prerequisites
Ensure you have the following software installed:
- **Power BI Desktop** (latest version)
- **Microsoft SQL Server Management Studio (SSMS)**

### Steps to Run the Project
1. Clone this repository:
   ```bash
   git clone https://github.com/manojgangavarapu/Pizza-Sales-Report
   ```
2. Open the Power BI file `Pizza Sales Report.pbix`.
3. Load the dataset into Power BI.
4. Run the provided SQL queries from `Pizza sales sql Queries.docx` to analyze data.
5. Refresh the data and explore the dashboards for insights.

## SQL Queries
The SQL queries used in the project include:
```sql
-- Total Revenue
SELECT SUM(total_price) AS Total_Revenue FROM pizza_sales;

-- Average Order Value
SELECT SUM(total_price) / COUNT(DISTINCT order_id) AS Avg_Order_Value FROM pizza_sales;

-- Total Pizzas Sold
SELECT SUM(quantity) AS Total_Pizza_Sold FROM pizza_sales;

-- Total Orders
SELECT COUNT(DISTINCT order_id) AS Total_Orders FROM pizza_sales;

-- Average Pizzas per Order
SELECT CAST(SUM(quantity) AS DECIMAL(10,2)) / CAST(COUNT(DISTINCT order_id) AS DECIMAL(10,2)) AS avg_pizzas_per_order FROM pizza_sales;
```

## Project Structure
```
.
├── Pizza Sales Report.pbix        # Power BI Dashboard File
├── Pizza sales sql Queries.docx   # SQL Queries for Analysis
├── README.md                      # Project documentation
```

## Sample Visualizations
![Dashboard Screenshot](![image](https://github.com/user-attachments/assets/4bd66461-790f-4f52-9e90-79efb997f7e5)
)

## Contributing
Contributions are welcome! Follow these steps to contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m "Add new feature"`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

