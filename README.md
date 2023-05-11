# SQL
--SQL ESSENTIAL TRAINING

--DB Browser for SQLite
-- SQL Single line Comment
/* SQL mult-line comment */
--WSDA_Music.db using this table
-- SQL CASE INSENSITIVE

SELECT FirstName, LastName, Email FROM Customer

--ALIASES
SELECT FirstName AS "Customer First Name", 
LastName AS "Customer Last Name", 
Email AS "EMAIL"
FROM 
Customer


--SORTING

--ascending
SELECT FirstName AS "Customer First Name", 
LastName AS "Customer Last Name", 
Email AS "EMAIL"
FROM 
Customer
ORDER BY
LastName ASC

--desc
SELECT FirstName AS "Customer First Name", 
LastName AS "Customer Last Name", 
Email AS "EMAIL"
FROM 
Customer
ORDER BY
LastName DESC

--multiple sort
SELECT FirstName AS "Customer First Name", 
LastName AS "Customer Last Name", 
Email AS "EMAIL"
FROM 
Customer
ORDER BY
FirstName ASC,
LastName DESC

--LIMIT RESULT
SELECT FirstName AS "Customer First Name", 
LastName AS "Customer Last Name", 
Email AS "EMAIL"
FROM 
Customer
ORDER BY
FirstName ASC,
LastName DESC
LIMIT 5

--Operator Types
/*
ARITHMETIC OPERATORS
Add(+), Substract(-), Multifly(*), Divide(/), Modulo(%)

COMPARISION OPERATORS
Equal to(=)
Not equal to(<>)
Greater than(>)
Less than (<)
Greater than or equal to(>=)
less than or eqaul to (<=)

LOGICAL OPERATOTS
AND
OR
LIKE
IN 
BETWEEN
*/

--EXAMPLE OF OPERATORS

--EQUAL TO
SELECT 
InvoiceDate, 
BillingAddress,
BillingCity, 
total 
FROM
Invoice
WHERE total=1.98
ORDER BY
InvoiceDate

SELECT 
InvoiceDate, 
BillingAddress,
BillingCity, 
total 
FROM
Invoice
WHERE 
BillingCity = 'Brussels'
ORDER BY
InvoiceDate

--BETWEEN
SELECT 
InvoiceDate, 
BillingAddress,
BillingCity, 
total 
FROM
Invoice
WHERE 
total BETWEEN 1.98 AND 5.00
ORDER BY
InvoiceDate

--IN
SELECT 
InvoiceDate, 
BillingAddress,
BillingCity, 
total 
FROM
Invoice
WHERE 
total IN (1.98,3.96)
ORDER BY
InvoiceDate

SELECT 
InvoiceDate, 
BillingAddress,
BillingCity, 
total 
FROM
Invoice
WHERE 
BillingCity IN ('Brussels', 'Orlando')
ORDER BY
InvoiceDate

--LIKE
SELECT 
InvoiceDate, 
BillingAddress,
BillingCity, 
total 
FROM
Invoice
WHERE 
BillingCity LIKE 'B%'
ORDER BY
InvoiceDate

SELECT 
InvoiceDate, 
BillingAddress,
BillingCity, 
total 
FROM
Invoice
WHERE 
BillingCity LIKE '%B%'
ORDER BY
InvoiceDate

--Query to find record for specific date 
SELECT 
InvoiceDate, 
BillingAddress,
BillingCity, 
total 
FROM
Invoice
WHERE 
InvoiceDate = '2010-05-22 00:00:00'
ORDER BY
InvoiceDate

--Query with Date function 
SELECT 
InvoiceDate, 
BillingAddress,
BillingCity, 
total 
FROM
Invoice
WHERE 
DATE(InvoiceDate) = '2010-05-22'
ORDER BY
InvoiceDate

--Query with two conditions with AND Operator
SELECT 
InvoiceDate, 
BillingAddress,
BillingCity, 
total 
FROM
Invoice
WHERE 
DATE(InvoiceDate)>'2010-05-22' AND total <3.00
ORDER BY
InvoiceDate

--Query with two conditions with OR operator
SELECT 
InvoiceDate, 
BillingAddress,
BillingCity, 
total 
FROM
Invoice
WHERE 
BillingCity LIKE 'P%' OR BillingCity LIKE 'B%'
ORDER BY
InvoiceDate

--query WITH AND and OR operator
SELECT 
InvoiceDate, 
BillingAddress,
BillingCity, 
total 
FROM
Invoice
WHERE 
total>3.00 AND BillingCity LIKE 'P%' OR BillingCity LIKE 'B%'
ORDER BY
InvoiceDate

--PEMDAS( Parenthesis, Exponents, Multiplication, Division, Addition, Substraction)
--query with parenthesis or brackets
SELECT 
InvoiceDate, 
BillingAddress,
BillingCity, 
total 
FROM
Invoice
WHERE 
total>3.00 AND [BillingCity LIKE 'P%' OR BillingCity LIKE 'B%']
ORDER BY
InvoiceDate
