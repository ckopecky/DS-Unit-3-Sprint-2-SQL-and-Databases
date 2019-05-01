SQL Practice

Select `City` from `Customers` Table

`SELECT City FROM Customers;`

Select all the _different_ values from the `Country` column in the `Customers` table

`SELECT DISTINCT Country FROM Customers;`

Select all records where City column has value Berlin

`SELECT * FROM Customers WHERE City = 'Berlin';`

Use the NOT keyword to select all records where City is NOT Berlin

`SELECT * FROM Customers WHERE NOT City = 'Berlin'`

Select all records where customer ID has value of 32

`SELECT * FROM Customers WHERE CustomerID = 32`

Select all records where thr City column has value 'Berlin' and postalCcode column has the value 12209

`SELECT * FROM Customers WHERE City = 'Berlin' AND PostalCode = 12209`

Select all records where City is Berlin and all records where City is London

`SELECT * FROM Customers WHERE City = 'Berlin OR City = 'London'`

Select all records from the Customers table, sort the result alphabetically by City. 

`SELECT * FROM Customers ORDER BY City ASC`

Select all records from the customers table and sort the result reverse alphabetically in City column

`SELECT * FROM Customers ORDER BY City DESC`

Select all records from the Customers table, sort the result alphabetically, first by the column Country, then by the column City. 

`SELECT * FROM Customers ORDER BY Country, City`

Insert a new record in the customers table

`INSERT INTO Customers (keys to insert) VALUES (values to insert);`

Select all records from customers where the postalcode is empty

`SELECT * FROM Customers WHERE PostalCode IS NULL;`

Select all records from the Customers table where the PostalCode column is NOT empty

`SELECT * FROM Customers WHERE PostalCode IS NOT NULL;`

Update the city column of all records in the Customers table to Oslo.

`UPDATE Customers SET City = 'Oslo'`

Set the value of the city columns to Oslo, but only the ones where the Country has the value Norway.

`UPDATE Customers SET City = 'Oslo' WHERE Country = 'Norway';`

Update the City value and the Country value where CustomerID - 32

`UPDATE Customers SET City = 'Oslo', Country = 'Norway' WHERE CustomerID = 32;`

Delete all records from the Customers table where the Country value is 'Norway'

`DELETE FROM Customers WHERE Country = 'Norway';`

Delete all records from the customers table

`DELETE FROM Customers`;

`TRUNCATE Customers;` 

Delete from and Truncate removes the rows from table,but the schema is preserved. 

Use the MIN frunction to select the record with the smallest value in the price column.

#### Aggregator (Reduce) Statements: 


`SELECT MIN(Price) FROM Products;`

Highest? 

`SELECT MAX(Price) FROM Products;`

Number of records that have the Price value set to 18

`SELECT COUNT (*) WHERE Price = 18;`

Calculate the average price of all products

`SELECT AVG(Price) FROM Products;`

Sum? 

`SELECT SUM(Price) FROM Products;`

All records where city column starts with letter 'a'?

`SELECT * FROM Customers WHERE City LIKE 'a%';`

contains letter 'a'?

`SELECT * FROM Customers WHERE City LIKE '%a%';`

ends with letter 'a'?

`SELECT * FROM Customers WHERE City LIKE '%a';`

starts with letter 'a' and ends with letter 'b'

`SELECT * FROM Customers WHERE City LIKE 'a%b';`

does not start with letter a

`SELECT * FROM Customers WHERE City NOT LIKE 'a%';`

second letter of city is an 'a'

`SELECT * FROM Customers WHERE City LIKE '_a%';`

a, c or s === first letter in City?

`SELECT * FROM Customers WHERE City LIKE '[acs]%';`

* almost like regular expressions

first letter starts with anything from a-f

`SELECT * FROM Customers WHERE City LIKE '[a-f]%';`

