# Flat files: 
## idea:
No-setup write persistence. Simple full data retrieval.

## use when:
* temporary local persistence
* always full data retrieval

## breaks under requirements:
* concurrent write access
* consistency guarantee
* complex querying

## tradeoffs:
* high reading complexity for partial data

## examples: 
* json
* csv

# Relational databases:
## use when:
* ACID guarantees needed -> consistency necessary
* complex queries (JOINS)

## breaks under requirements:
* strong horizontal scaling
* flexible schema

## examples:
* SQLLite
* Redis

# Key-Value stores
## idea
Data consists of key and value only. 

## use when:
* extreme performance is needed?
* caching ??
* no query beyond key

## breaks under requirements:
* queries beyond key needed

## examples
* Redis
* DynamoDB

# Document databases
## idea
Data stored in documents such as json files. Can each json be completely different? what are the guarantees?

## use when
Data is sourced from different schemas, not unter your control. -> fields vary from schema to schema.
But how can I then use the data?

## Examples
* MongoDB
* CouchDB