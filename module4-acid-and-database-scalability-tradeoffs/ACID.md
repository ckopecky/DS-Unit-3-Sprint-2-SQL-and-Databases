Horizontal scaling --- Non-relational world you can scale horizontally -- lots of little boxes. Way better economically
Vertical scaling --- traditional relational database. Have a master node that figures out what the query is supposed to do. 

# ACID

**A**tomicity, **C**onsistency, **I**solation, **D**urability

-- relational databases guarantee these properties. They keep a log of everything that is happenening so if something happens, they can undo it and fix things. 

## Atomicity 

-- a transaction (arbitrary bundle of queries) is a single "unit". Either every statement in the transaction succeeds or it fails completely. Database is left unchanged if it fails completely. A bank would want to have Atomicity. 

    -- Allison and Bob both have an account at the same bank. 
    Allison is sending $20 bucks to Bob. Somewhere behind the 
    scenes, the bank will subtract the money in Allison's 
    account and add it to Bob's account. You can imagine that 
    there is some SQL going on here that takes money from Alli-
    -son's account and adds it to Bob's account. If some of the 
    SQL statements failed, the entire transaction would fail. 
    If atomicity did not exist, Allison would be out $20. 

## Consistency 

-- when you execute the transaction it can only leave the database in a valid state. What does that mean? Enforcement of the schema. It will prevent you from inserting something that goes outside of the schema, but does not guarantee that the transaction is correct. 

-- You will never end up in a state where the database has something it's not supposed to. 

## Isolation 

-- transactions are often conducted concurrently (i.e. writing and reading to multiple tables at the same time). Isolation ensures that concurrent execution of transactions leaves the database in the same state that would have been obtained if the transactions were executed sequentially. Think about when someone accesses the same account at the same time from multiple ATM machines across the country. 

## Durability 

-- even if you have a true system failure, the system (the database) will be able to recover to a good state. 


>i.e. if a flight booking 
reports that a seat has 
successfully been booked, 
then the seat will remain 
booked even if the system crashes


**If you do migrations all the time, your database will start to look really ugly. A schema change in an ACID database should not be taken lightly.**


-----------------

