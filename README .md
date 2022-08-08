
# Sales Insights
The aim of the projects was to generate the sales insights of the business in Power Bi.Using these sales insights dashboard,the stakeholders can make some very significant decisions regarding their business.


# Roadmap

The projects was divided into two parts

## Data Analysis using MySQL

A SQL dump of the company's database was loaded in MySQL and analysis was done.
Some them were:
Show all customer records

SELECT * FROM customers;

1)Show total number of customers
SELECT count(*) FROM customers;

2)Show transactions for Chennai market (market code for chennai is Mark001

SELECT * FROM transactions where market_code='Mark001';

3)Show distrinct product codes that were sold in chennai

SELECT distinct product_code FROM transactions where market_code='Mark001';

4)Show transactions where currency is US dollars

SELECT * from transactions where currency="USD"

5)Show transactions in 2020 join by date table

SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

6)Show total revenue in year 2020,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

7)Show total revenue in year 2020, January Month,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

8)Show total revenue in year 2020 in Chennai

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";

## Creating a dashboard in PowerBI

A sales insights dashboard was generated in PowerBI to understand various insights regarding its sales.
Some of the PowerBI features used were:
•Bar Graphs
•Line Chart
•Slicers
•Conditional column
•Data Transform

## Screenshots

![Salesinsights1](https://user-images.githubusercontent.com/102639991/183400415-364b7c6d-7e6e-4566-910f-12fa7656ae32.png)
![Salesinsights2](https://user-images.githubusercontent.com/102639991/183400436-f77c40b9-b970-4522-8b92-8ca1827d579f.png)
![SalesInsights3](https://user-images.githubusercontent.com/102639991/183400449-defef653-dc4f-42de-bc8a-60d835429bd9.png)
![Salesinsights4](https://user-images.githubusercontent.com/102639991/183400460-2ba051a1-9a5f-4ad5-9f37-f1623cd7ce74.png)
![Salesinsights5](https://user-images.githubusercontent.com/102639991/183400473-af00d029-cc52-4021-b252-934d365e80bc.png)
## Insights

1) Due to obvious reasons,the revenue crashed after March 2020 and was an all time in June 2020
2) Even though,the revenue crashed in 2020,it was always gradually decreasing since 2018.
3) Delhi occupies most of the market place and others are not even close.
4) Electrical Sara Stores is the topmost customer the company don't want to loose at any cost.
5) There is no particular month where the revenue can be predicted to be extra ordinary.
6) The company does not have any signature product which is always expected to be one of its leading revenue generators.