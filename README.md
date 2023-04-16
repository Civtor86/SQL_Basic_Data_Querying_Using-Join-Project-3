# SQL_Data_Querying_Using-Join-Project-3
SQL_Data_Querying_Using Joins Function on PostGreSQL Project 3

SQL_Basic_Data_Querying Using Joins Function on PostGreSQL

This is my Third SQL project  where I explore the use of Join Function of SQL by creating and manipulating custom tables using PstGreSQL.
The DVD Rental Dataset is taken from the following website: https://downloads.mysql.com/docs/sakila-db.zip.


Introduction: As the General manager for the Sydney area at Airbnb, you want to know more about the different listings of houses your team has onboarded. You have access to information regarding the listings, neighbourhoods, reviews, and calendar. Each of these have their own separate table.

The task I need to accomplish on the said dataset are the following: 

1.	Using the DVD rental dataset, provide the SQL code and the output for this query criterion

    A.	Using the DVD rental dataset, provide the SQL code and the output for this query criterion. a Provide an Excel sheet report of the total sum of payments made by         each customer in the payments table. Present it in ascending order. There should be four columns: customer_id`, first_name`, last_name`,   and sum.

    B.	Provide the SQL syntax and output of customer IDs having an average payment amount of less than 3.

2.	Why would the following SQL syntaxes fail?

A. SELECT  first_name, last_name, district  FROM customer INNER JOIN address ON address_id = address_id. 

ANSWER: 
The "address id" column name is used in the ON clause of the query, but the table from which it should be retrieved is not specified, hence this SQL syntax will fail. Due to the fact that they are connected on that column, both tables (customer and address) include a column called "address id." So, SQL is unable to determine which table should be used for this column in the ON clause.

The "address id" column's table name or alias must be specified in the ON clause to correct this. The amended syntax is as follows:

District: SELECT first name, last name
from customer
Address for INNER JOIN
customer.address id = address.address id

With this approach, the "address id" column to utilize for the join condition is specified, and the query should succeed.


B.	SELECT  customer_id, SUM(amount3  FROM payment GROUP BY customer_id HAVING amount > 100

ANSWER: 
The column "amount" that is mentioned in the HAVING clause should actually be SUM(amount), since it is not included in the SELECT statement.


3.	Answer the following business scenario questions. Provide the SQL code and the output. 

A.	 One of the criteria for a customer to become part of the customer loyalty program is that they need to have an accumulated payment made to the DVD rental store of at least $200 or more. As a data analyst, you need to provide a list of customer IDs with a total accumulated payment of at least $200 or more.



