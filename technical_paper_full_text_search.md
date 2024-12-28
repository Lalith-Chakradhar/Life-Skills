# Full Text Search

## What is full-text search?

Unlike traditional search methods that rely on exact word or phrase matches, a full-text search refers to a search of all of the documents' contents within the full-text queries’ range(s) that are relevant. This includes topic, phrasing, citation, or additional text attributes.

## Different search platforms for full-text search

## Elasticsearch

### What is Elasticsearch?

Elasticsearch is a distributed database that can 

1. Handle large volumes of data continuously.
2. Scale automatically.
3. Continuously add new data.

### Characteristics of Elasticsearch

1. NoSQL, JSON-based data store.
2. Interaction with Elasticsearch happens through RESTful URLs.
3. Can store a large variety of data formats like Logs, metrics and applications' trace data.

### Features of Elasticsearch in comparison to Relational databases 

1. In RDBMS (Relational DataBase Management System), the data is stored in the form of databases whereas in Elasticsearch, the data is stored in the form of Indices.

2. In RDBMS, specific data is stored in tables whereas in Elasticsearch, it is stored in the form of Patterns/Types.

3. In RDBMS, Rows are the individual records that contain data whereas in Elasticsearch, we have something called as Documents.

4. In RDBMS, there are columns that describe about the data whereas in Elasticsearch, we have something called as Fields.

### Elasticsearch is typically used in the format of 'ELK Stack'?
Let's expand ELK Stack -
1. We have Elasticsearch Data Store (E in ELK) which stores the unstructured data.
2. Then in order to view and interact with data in Elasticsearch Data store, we have Kibana (K in ELK), which is basically web based User Interface. Using Kibana, we can build different dashboards, different widgets/visualizations on Elasticsearch data which is consistently updated whenever new data comes in.
3. Furthermore, in order to add data we have something known as Logstash (L in ELK). Logstash is an open-source, server-side processing pipeline and it is mainly used for inputting data (like SDKs and other data), transforming the data and output the data to stash.

## Solr

### What is Solr?

Solr is an open source search client that is coded in Java and a part of project Apache Lucene. It is an improvement over Lucene. Though Elasticsearch is widely preferred nowadays, Solr is still a good, robust search client.

### Major Features in Solr
1. Solr is a fully text-only search. It can search in full-text databases.
2. It does not have the capability of searching through metadata.
3. It does full text indexing. That means each character is indexed! Think about indexing having terabytes of data!
4. It gives results in seconds.
5. Solr searches in the form of search terms. It highlights the matched data, by passing the search query term to the JAVA API and then the response gives the search results. It is quite robust in nature.
6. It performs faceted search. Solr takes the search term, matches it to one attribute and removes all other attributes in its search results.
7. Can accommodate real-time indexing. So, whenever a search process is happening and new data is added in between by another server, Solr takes care of modifying the indices on adding new data, without affecting its searching capabilities!
8. Supports dynamic clustering. This is the ability to maintain many servers for reliability of Solr, even if one server fails, backup data on other servers ensures continued functionality.
9. Can easily be integrated with databases in projects.
10. It supports NoSQL features.
11. It has good capabilities in document handling.
12. Majorly used in handling searches in Big Data.

## Lucene

### What is Lucene?

1. Lucene is a high performance, open source text search engine that is written entirely in Java. It is cross-platform and versatile.

2. Lucene is capable of high-performance indexing which can take more than 150 gigabytes of search data per hour. It requires minimal RAM - 1 MB and does fast incremental indexing. The indexed stored data is 80% smaller compared to indexed original text.

3. Lucene offers very powerful searching algorithms like -
	i. Ranked searching 
	ii. Multifaceted queries support
	iii. Fielded search and Any-field Sorting
	iv. Multi-index search
	v. Concurrent update & search
	vi. Memory efficient & typo-tolerant
	vii. Pluggable Ranking Models
	viii. Configurable Storage Engine

### How Lucene works?

1. The documents where the data is stored goes through an analyzer and creates tokens. Tokens are individual words of the data in the Document.

2. Now these tokens end up in Inverted index. This inverted index is basically a hash map where the token is a key and the frequency of the token's occurrence, as well as the document the term appears is the value. 

3. Now the inverted index data is stored in Optimized Inverted Index, where the data is compressed and is efficiently stored on the data store.

### Lucene Reverse Index 

1. Every three indices is merge-sorted into one index. The factor of three indices is default and can be configured.

2. These indices are merge-sorted at various levels such that we have very large old indices and very small new indices. It is very useful for time series data.

3. The results are ranked and sorted, cached and based on sort keys. So the search is really, really fast.

### Lucene Analyzer - This  analyzer is a collection of text filters.

### Lucene Data Types

Lucene provides several data types to search and store different kinds of data. These data types determine how the data is processed, indexed, and stored in the index. 

1. Integer
2. Long (used for Dates)
3. Float
4. Double
5. Text
	i. Keyword (string) / Not Analyzed
	ii. Text / Analyzed
6. Binary


## In summary, Lucene is the foundation, and Solr and Elasticsearch are full-featured search engines built on top of Lucene.

## References

1. [What is Elasticsearch?](https://www.youtube.com/watch?v=ZP0NmfyfsoM)
2. [What is Solr](https://www.youtube.com/watch?app=desktop&v=0tH36OfNwNw)
3. [Introduction to Apache Lucene & Elasticsearch](https://www.youtube.com/watch?v=BvgGgkN3clI)
