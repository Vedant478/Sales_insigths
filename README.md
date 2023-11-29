
## Sales Insights Data Analysis Project

### Instructions to setup mysql on your local computer

1. Follow step in this video to install mysql on your local computer
https://www.youtube.com/watch?v=WuBcTJnIuzo

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`

## Star Schema and Realtionships

A star schema is a type of database schema commonly used in data warehousing and business intelligence applications. It is designed to organize data into a logical structure that facilitates efficient querying and reporting. The star schema consists of a central fact table linked to one or more dimension tables, forming a pattern that resembles a star when visualized.
Here are the key components of a star schema:

Fact Table:Central to the schema, the fact table contains quantitative data (facts) that can be aggregated. This data is typically numerical and represents business metrics such as sales, revenue, quantity, etc.
Each row in the fact table corresponds to a specific event or transaction and includes foreign keys that link to the dimension tables.

Dimension Tables:Surrounding the fact table are dimension tables, which contain descriptive attributes that provide context to the data in the fact table.
Each dimension table corresponds to a category or aspect of the business, such as time, geography, product, or customer.
Dimension tables are connected to the fact table through foreign key relationships.

The star schema is called so because, when visualized, the structure resembles a star with the fact table at the center and dimension tables radiating outwards. This design simplifies queries by allowing users to easily join the fact table with one or more dimension tables to retrieve relevant information. The schema is denormalized, meaning that redundant data is often included in dimension tables to minimize the need for complex joins and improve query performance.

![Star_schema ](https://github.com/Vedant478/Sales_insigths/assets/55829535/fa912b48-066b-4ee3-829c-264d80f24f3d)


## Demo Images 

## Mobile layout 

![mobile](https://github.com/Vedant478/Sales_insigths/assets/55829535/bd4dc7c0-3d8b-4276-802f-303a70f6e5af)

## Dashboard

![DashBoard_page 1](https://github.com/Vedant478/Sales_insigths/assets/55829535/538f4c8e-4ff4-4a2c-9cec-954dd3153f03)

![Dashboard_page2](https://github.com/Vedant478/Sales_insigths/assets/55829535/9fb518ed-3307-46fd-a61b-33ce270f703c)

## Demo Video

https://github.com/Vedant478/Sales_insigths/assets/55829535/9e2cc106-324c-4df9-ad68-6b5a248ac8e4



