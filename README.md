# SQL
--DB Browser for SQLite
-- SQL Single line Comment
/* SQL mult-line comment */
--WSDA_Music.db using this table

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
