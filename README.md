
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

## Demo Images 

## Mobile layout 

![mobile](https://github.com/Vedant478/Sales_insigths/assets/55829535/bd4dc7c0-3d8b-4276-802f-303a70f6e5af)

## Dashboard

![DashBoard_page 1](https://github.com/Vedant478/Sales_insigths/assets/55829535/538f4c8e-4ff4-4a2c-9cec-954dd3153f03)

![Dashboard_page2](https://github.com/Vedant478/Sales_insigths/assets/55829535/9fb518ed-3307-46fd-a61b-33ce270f703c)

## Demo Video

https://github.com/Vedant478/Sales_insigths/assets/55829535/9e2cc106-324c-4df9-ad68-6b5a248ac8e4



