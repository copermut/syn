---
layout: post
---
Background: [[Meta: Website graph implementation]]

> Data processed by triple stores tends to be logically linked, thus triple stores are included in the category of graph databases. However, triple stores are not “native” graph databases because they don’t support index-free adjacency, nor are their storage engines optimized for storing property graphs.

> Triple stores store triples as independent elements, which allows them to scale horizontally but prevents them from rapidly traversing relationships. In order to perform graph queries, triple stores must create connections from individual, independent facts – adding latency to every query.

> Because of these trade-offs in scale and latency, the most common use case for triple stores is offline analytics rather than for online transactions.

via: [Neo4j Blog: Graph Databases for Beginners: Other Graph Data Technologies](https://neo4j.com/blog/other-graph-database-technologies/)