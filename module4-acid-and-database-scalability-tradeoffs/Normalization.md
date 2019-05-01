# Normalization

-- database normalization reduces the redundancy of data. It structures a database in accordance to a "normal form" to reduce redundancy and improve data integrity. 

Example of non-normalization:
![example of non-normalization][notNormalization]

[notNormalization]: ./NotNormalization.png

-- This table is a bit more complex than it needs to be. We have to have the customer's name and the customer's ID everytime they do a transaction. This is inefficient. 

-- As is seen here, we store Abraham's name twice and Jacob's name three times. 


The insight of database normalization is that you don't need to do that. 

A normalized database would have two separate tables:

Example of normalization:
![example of normalization][Normalization]

[Normalization]: ./Normalized.png

You would use joins or foreign keys to expose the relationship between the two tables. The customer ID in this instance would be a foreign key the is both in the customer table and in the transaction table. You can use the customer table to identify the cust ID names in the transaction table. 

1NF

2NF

3NF

EKNF

BCNF

4NF

ETNF

5NF

DKNF

6NF

Why ever use anything else? 

