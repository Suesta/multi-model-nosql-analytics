# Multi-Model NoSQL Analytics

Multi-model NoSQL analytics project combining **Cassandra**, **Neo4j**, and **MongoDB** to solve different data access patterns across wide-column, graph, and document-oriented databases.

The project focuses on designing query-driven data models, writing analytical queries, validating results, and comparing how different NoSQL paradigms handle data retrieval, aggregation, relationships, and updates.

## Project Overview

This project explores how different NoSQL databases can be used to solve practical analytical and operational problems in a shared mobility and graph-based data context.

The work is divided into three main database paradigms:

* **Cassandra** for query-driven wide-column modeling and partition-key design.
* **Neo4j** for graph traversal and relationship-based analytics.
* **MongoDB** for document queries, aggregation pipelines, and update operations.

The goal is not only to write queries, but also to justify the data modeling decisions behind them and understand how each database engine behaves depending on the access pattern.

## Technologies Used

* Cassandra
* CQL
* Neo4j
* Cypher
* MongoDB
* MongoDB Aggregation Framework
* NoSQL data modeling
* Query optimization
* Document-oriented databases
* Graph databases
* Wide-column databases

## Repository Contents

```text
.
├── M2.889_Suesta_Victor_nosql_pra1.pdf
└── README.md
```

The PDF contains the full technical report, including query design, database operations, outputs, and reasoning for each NoSQL engine.

## Main Topics Covered

### Cassandra: Query-Driven Wide-Column Modeling

The Cassandra section focuses on designing tables around specific access patterns. It includes:

* Analysis of insert and update behavior in Cassandra.
* Explanation of upsert behavior compared with relational databases.
* Correction of an incorrect primary key design that caused overwritten records.
* Creation of query-specific tables using appropriate partition and clustering keys.
* Evaluation of partitioning strategies for scalability across multiple nodes.
* Discussion of ordering behavior within partitions.

Key concepts demonstrated:

* Primary key design
* Partition keys
* Clustering keys
* Query-driven modeling
* Data distribution
* Avoiding inefficient filtering patterns
* Cassandra write behavior

### Neo4j: Graph-Based Analytics

The Neo4j section uses a graph model to analyze relationships between entities such as characters, films, planets, starships, organizations, species, and manufacturers.

It includes graph queries for:

* Counting related entities.
* Finding organizations with a specific number of leaders.
* Identifying manufacturers linked to vehicles appearing in multiple films.
* Traversing character, starship, and film relationships.
* Filtering paths based on node properties and relationship types.
* Classifying characters according to the vehicles they piloted.

Key concepts demonstrated:

* Graph traversal
* Relationship-based querying
* Pattern matching with Cypher
* Aggregation with `collect`, `count`, and `DISTINCT`
* Conditional classification using `CASE`
* Ordering and filtering graph query results

### MongoDB: Document Queries and Aggregation Pipelines

The MongoDB section focuses on querying and updating a document-oriented database for a shared bike system.

It includes:

* Filtering users based on age, usage, and credits.
* Retrieving bikes based on battery level, availability, and location.
* Aggregating array fields using `$unwind`.
* Grouping and calculating metrics with `$group`.
* Computing averages, minimums, and maximums.
* Analyzing recent rides while preserving trip directionality.
* Updating embedded arrays and related documents.

Key concepts demonstrated:

* Document filtering
* Field projection
* Sorting
* Aggregation pipelines
* Array processing
* Embedded document updates
* Multi-document consistency considerations
* Operational updates with `$inc`, `$set`, `$push`, and `$slice`

## Skills Demonstrated

This project demonstrates practical skills relevant to data science, analytics engineering, and data engineering roles:

* Designing data models based on query requirements.
* Choosing the right NoSQL paradigm for different access patterns.
* Writing efficient analytical queries.
* Interpreting database outputs and validating results.
* Working with structured, semi-structured, and graph-based data.
* Understanding trade-offs between denormalization, embedding, partitioning, and relationships.
* Comparing NoSQL behavior with traditional relational database concepts.
* Explaining technical decisions clearly and reproducibly.

## Why This Project Matters

Modern data systems often require more than one database model. A graph database may be better suited for relationship-heavy analysis, a document database for flexible nested structures, and a wide-column database for scalable query-driven access.

This project shows how the same analytical mindset can be adapted across different NoSQL technologies, depending on the structure of the data and the type of question being answered.

## How to Read the Report

The technical report is organized by database engine:

1. **Cassandra**: data modeling, partitioning, and query-specific table design.
2. **Neo4j**: graph traversal and relationship analysis.
3. **MongoDB**: document querying, aggregation pipelines, and update operations.

Each section includes the query, the obtained result, and a short explanation of the modeling or querying decision used to solve the problem.

## Author

**Víctor Suesta Arribas**
Mathematics Graduate & MSc Data Science Student
Focused on Data Science, Machine Learning, Analytics, and Data Engineering
