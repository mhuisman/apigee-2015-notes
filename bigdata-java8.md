What is big data?

Is it the size?  Is it the location?  Is it the representation?

Doesn't have a clear definition.  

Big Data as 'global' data -- data that is ubiquitous, all around us in the world -- have simple, easy access to all of it.

A lot of big data platforms/frameworks do not allow for sufficient separation of concerns -- must write a ton of boilerplate / deal with a number of abstractions that are not directly related to the business logic being written

Frameworks are an indication of failure in the underlying programming language - making difficult tasks easier.  But which one to choose?  Which ones will survive?  Cutting edge frameworks may be 'neat' but much more risky to rely upon.

Java not a great language for data processing - developer required to deal with a lot of boilerplate code and competing abstractions.  Common pattern - sequential dealing with data/result sets.  

Java 8 - streams, lambdas

monadic style programming model

intermediate operations 

terminal operations 

Streams great in non-distributed environment, but have practical difficulties in a distributed environment:

DStream - Distributable Stream

https://github.com/hortonworks/dstream

Abstracts away data stream configuration, so you can write your code once irrespective of data source providing it.
