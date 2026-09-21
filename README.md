# Sunrise Supermarket SQL Assignment

## Section 1 — Summary
This assignment was about using SQL to analyse a supermarket dataset by combining tables, calculating customer totals, and using window functions to answer business-related questions. I used Oracle Database and worked with a local pluggable database to run the queries and check the results. The dataset had different tables like customers, orders, products, and order items, and the main focus was on customer spending, order patterns, and revenue growth.


## Section 2 — Business Scenario
Sunrise Supermarket is a retail business that sells everyday products to customers in different areas. The customers are regular shoppers who place multiple orders over time, and management wants to understand who spends the most, how often people buy, and how sales change month by month. This helps the business make better decisions about customer loyalty, promotions, and sales planning.


## Section 5 — Query Explanations

### Query 1: Inner Join between orders and customers
What it does: This query joins the orders table and the customers table using customer_id, so each order is matched to the customer who made it.

Business interpretation: This helps the business see which customer bought what and when, which makes it easier to understand customer activity and order history.

### Query 2: Inner Join between order_items and products
What it does: This query links the order_items table with the products table using product_id, so each item in an order is connected to its product details.

Business interpretation: This shows which products were sold, how many were sold, and what price they were sold at, which helps the business understand product demand.

### Query 3: Left Join between customers and orders
What it does: This query uses a LEFT JOIN to show all customers and their orders, even if some customers did not place any order.

Business interpretation: This is useful because it helps the store see both active and inactive customers, which is important for customer retention and follow-up.

### Query 4: CTE for customer spend above average
What it does: This query creates a CTE to calculate each customer’s total spending and then filters for customers whose total is above the average.

Business interpretation: This helps identify the customers who spend more than the usual customer, which is useful for focusing on high-value buyers.

### Query 5: RANK customers by total spent
What it does: This query uses the RANK function to rank customers according to how much they spent, and customers with the same total can share the same rank.

Business interpretation: This makes it easy to see who the top customers are and compare their spending levels.

### Query 6: ROW_NUMBER for each customer’s orders
What it does: This query gives each order a row number for every customer so the orders can be listed in sequence.

Business interpretation: This helps the supermarket understand how often customers are buying and how their purchase pattern looks over time.

### Query 7: Running total of revenue over time
What it does: This query calculates a running total of revenue by date so the total keeps increasing as more sales happen.

Business interpretation: This shows how revenue grows during August and helps the business see whether sales are improving over time.

### Query 8: LAG to find days between consecutive orders
What it does: This query uses LAG to compare each customer’s current order date with the previous one and calculate the number of days between them.

Business interpretation: This helps the business understand customer buying habits and whether customers are ordering regularly or taking longer breaks between purchases.

## Section 6 — Overall Business Interpretation
From the results, the top three spenders were Emmanuel Nkurunziza with 15,600, Diane Uwase with 14,600, and Aline Mukamana with 10,800. This shows that a few customers are responsible for a big part of the store’s sales. The running total also shows that revenue increased steadily throughout August, which means the business was doing well and sales were growing over time. The order analysis also showed that some customers bought more than once, which means there is repeat buying behaviour. My advice to management would be to keep rewarding loyal customers and use this information to improve promotions, stock planning, and customer retention.


## Section 7 — Challenges
One of the biggest problems I faced was the ORA-01950 and ORA-01536 errors. These happened because the SYSTEM tablespace had quota issues, so Oracle would not allow the database operation to continue. It was frustrating because it blocked the work and made me spend time fixing the database setup instead of writing queries.

Another issue was that some data seemed to disappear because I had not run COMMIT after making changes. In Oracle, if you insert or update data and forget to commit, the data may not stay saved properly. I learned that saving the changes correctly is just as important as writing the SQL itself.

I also had to create the USERS tablespace manually because it was missing. Without it, Oracle could not place the objects properly, so I had to fix the environment before continuing. These problems were annoying at the time, but they taught me a lot about how Oracle works in real life.

## Section 8 — Integrity Statement
I did this work by myself using my own Oracle setup and my own screenshots. I did not copy answers from classmates or submit someone else’s work as my own. I did not use AI to generate the final SQL solution for me, and I only used it for checking my understanding. The screenshots in this project were taken from my own machine and reflect the actual work I did.

## Final Note
This project helped me understand how SQL joins, CTEs, and window functions can be used to answer real business questions. It also showed me that database work is not only about writing correct queries, but also about fixing setup problems, checking data carefully, and interpreting the results in a meaningful way.