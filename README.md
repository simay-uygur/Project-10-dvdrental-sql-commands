# Project-10-dvdrental-sql-commands
There are some commands on the dvdrental database which was taken from PostgreSQL website.

These are the wanted tasks for SQL queries given by Patika.

List the data in the title and description columns from the film table.
List all columns from the film table where the film length (length) is greater than 60 AND less than 75.
List all columns from the film table where the rental rate (rental_rate) is 0.99 AND the replacement cost (replacement_cost) is either 12.99 OR 28.99.
What is the value in the last_name column for the customer whose first_name value is 'Mary' in the customer table?
List the data from the film table where the length (length) is NOT greater than 50 AND the rental rate (rental_rate) is NOT 2.99 or 4.99.


ALL QUERIES: 

-- Q1
SELECT title, description FROM film;

-- Q2
SELECT * 
FROM film 
WHERE length > 60 AND length < 75;

-- Q3
SELECT * 
FROM film 
WHERE rental_rate = 0.99 AND (replacement_cost = 12.99 OR replacement_cost = 28.99);  

-- Q4
-- just Mary Smith exits 
SELECT first_name, last_name
FROM customer 
WHERE first_name = 'Mary';

-- Q5
SELECT *
FROM film
WHERE  ( NOT length > 50 AND NOT (rental_rate = 2.99 OR rental_rate = 4.99));
