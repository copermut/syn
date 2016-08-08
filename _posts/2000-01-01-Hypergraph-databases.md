---
layout: post
---
Background: [[Meta: Website graph implementation]]

> A hypergraph is a graph model in which a relationship (called a hyperedge) can connect any number of given nodes. While a property graph permits a relationship to have only one start node and one end node, the hypergraph model allows any number of nodes at either end of a relationship.

> Hypergraphs can be useful when your data includes a large number of many-to-many relationships.

> ...In theory, hypergraphs should produce accurate, information-rich data models. However, in practice, it’s very easy for us to miss some detail while modeling.

> advantages of graph database over hypergraph:
> - more familiar and explicit data modeling technique (resulting in less confusion for a development team).
> - can also fine-tune the model with properties, which is something we can’t do with a single hyperedge.

> Because hyperedges are multidimensional, hypergraph models are more generalized than property graphs. Yet, the two are isomorphic, so you can always represent a hypergraph as a property graph (albeit with more relationships and nodes).

> While property graphs are widely considered to have the best balance of pragmatism and modeling efficiency, hypergraphs show their particular strength in capturing meta-intent. For example, if you need to qualify one relationship with another (e.g., I like the fact that you liked that car), then hypergraphs typically require fewer primitives than property graphs.

via: [Neo4j Blog: Graph Databases for Beginners: Other Graph Data Technologies](https://neo4j.com/blog/other-graph-database-technologies/)

- HypergraphDB
- Trinity  (Microsoft Research)
- [AtomSpace](https://github.com/opencog/atomspace) (OpenCog)