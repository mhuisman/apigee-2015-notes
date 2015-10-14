What actual load are you going to need to support?

Apache open source mobile backend as a service

fully multi-tenant?

Installation -> Organization+

Organization -> Application* 

Application -> Users*, Devices*, Groups*, Security*, Roles*, Collection*

Collection -> Entities* (schemaless)


How to achieve web scale?

chose cassandra because it is horizontally scalable

elasticsearch (built on top of lucene)


Multi-Region indexing and consistency

post -> write -> cassandra replication , SNS queueu




