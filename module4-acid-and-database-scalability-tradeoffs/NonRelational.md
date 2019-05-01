Why should we use anything else besides relational databases? 

Scalability

mapreduce

> mapreduce is a paradigm that builds on functional programming. All programming is that treats functions as first-class citizens. The functions themselves are objects and you can pass them around. 

> Higher Order Function takes a function as an argument and does things with that function. 

The map higher order function will create a new object and do something to that object. 

The reduce higher order function will take a function and will aggregate the sequence to one thing. 

Example of mapreduce:
![example of mapreduce][mapreduce]

[mapreduce]: ./mapreduce.png

-- calculating the mean/average of something is very approachable with mapreduce. 

Why not both?? 

## NewSQL = ACID + CAP

-- What is CAP?

- Consistency -- every read receives the most up to date write or an error
- Availability -- every request receives a non-error response - without the guarantee that it contains the most recent write
- Partition Tolerance -- The system continues to operate despite an arbitrary number of messages being dropped or delayed by the network between nodes. 

CAP is a theorem that says it is impossible to provide two of these three guarantees. 

ACID systems choose consistency over Availability. 

Other approaches choose BASE (eventual consistency) approach. Maybe we don't give you the latest thing every time, but eventually will update. 


* BASE -- **B**asically **A**vailable, **S**oft state, **E**ventual consistency

NewSQL is an area of active research. The companies that use them have different standards for their version of their database. 






