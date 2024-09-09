# Data_Analysis
## Sales data of Atliq company using SQL and Power BI Tools

0. To access the sales DB in MySQL

USE Sale;
 
1. To see all customer records from customer table

SELECT * FROM customers;

2. To Query the total count of customers

SELECT count(*) FROM customers;

3. Querying all the transactions form Chennai market ( market code for chennai is "Mark001")

SELECT * FROM transactions where market_code='Mark001';

4. Show distrinct product codes that were sold in chennai

SELECT distinct product_code FROM transactions where market_code='Mark001';

5. Show transactions where currency is US dollars

SELECT * from transactions where currency="USD"

6. Show transactions in 2020 join by date table

SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

7.Show total revenue in year 2020,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

8. Show total revenue in year 2020, January Month,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

9. Show total revenue in year 2020 in Chennai

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";

![SQL](https://github.com/user-attachments/assets/6bab497f-debd-4da8-a7e6-109fc7b1931d)

![PowerBI](https://github.com/user-attachments/assets/c8d5a421-ceb4-4e20-9e7f-3c556c2f534f)
