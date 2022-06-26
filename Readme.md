# <u>Graphs</u>

## Table of Contents
- [Introduction](Readme.md#Graphs)
- [Types of Graphs](Readme.md#types-of-graphs)
- [Graph Terminologies](Readme.md#terminologies-in-graph)

## Introduction

A graph is a non-linear data structure that consists of a set of non-empty **Vertices** with a set of **Edges**.Each edge joins two different Vertices.

<p align="center" >
    <img src="resources/simple_graph.png" width="35%" height="35%" title="Graph - Edge and Vertex">
</p>

### Types Of Graphs
 1. Undirected Graph
 2. Directed Graph

## Undirected Graph

If an edge between any two nodes is *not directly oriented*, then it is undirected graph
<p align="center">
    <img src="resources/undirected_graph.png" width="35%" height="35%" title="Directed Graph">
</p>

**(A,B) & (B,A) represents the same edge** 

## Directed Graph (or) *Digraph*

If an edge between any two nodes is *directly oriented, then it is directed graph

<p align="center">
    <img src="resources/digraph.png" width="35%" height="35%" title="Undirected Graph">
</p>

**(A,B) Shows the edge between A and B**

Here A is called the *Tail node* and B is called the *Head node*

### <u>Restriction On a Graph</u>

- A graph may not have an edge from a vertex V back to itself. If it has an eged to itself, then it is called **Self edges**.
- A graph may not have multiple occurrence of the same edges *(multigraph)*


## Terminologies in Graph

### <u> Path </u>

A path is a sequence of distinct Vertices each adjacent ot the next.

<div align="center">
    <img src="resources/path.png" width="35%" height="35%" title="Path of a Graph">

*Path from A to C is (A,B),(B,C)*
</div>

### <u> Cycle </u>

A cycle is a simple path in which first and last vertices are same.

<div align="center">
    <img src="resources/path.png" width="35%" height="35%" title="Cycle of a Graph">

*ABCD is cyclic as it starts and ends with the same vertex*
</div>

In a digraph. a cycle is referred as *Directed Cycle*.

**Note : The maximum number of edges in a graph with *n* vertices is *n(n+1)/2***

### <u> Complete Graph </u>

An n-vertex, undirected graph with *exactly n(n+1)/2 edges* is said to be a complete graph.

<div align="center">
    <img src="resources/complete_graph.png" width="35%" height="35%" title="Complete Graph">

*n=4, no of edges = 4(4+1)/2 = 6*
</div>

### <u> Subgraph </u>

A subgraph of G is a graph G' such that *V(G') is a subset of V(G)

<div align="center">
    <img src="resources/subgraph.png" width="80%" height="80%" title="Subgraph">

*Subgraphs of G*
</div>

### <u> Connected Graph </u>
#### <u>Undirected</u>

If there exists a path from any vertex to any other vertex, then that graph is called **connected graph**.
#### <u>Directed</u>

If for every pair of distinct vertices there is a directed path from every vertex to every other vertices, then that graph is called **Strongly connected graph**.

<div align="center">
    <img src="resources/strongly_connected.png" width="35%" height="35%" title="Connected Directed Graph">

*Strongly Connected Graph*
</div>

If any vertex dosen't have a directed path to any other vertices, then the graph is called **Weakly connected Graph**.

<div align="center">
    <img src="resources/weakly_connected.png" width="35%" height="35%" title="Connected Undirected Graph">

*Weakly Connected graph*
</div>

### <u>Degree of a graph </u>

#### <u>Unirected Graph Degree</u>

Undirected graph only have one degree, ie. the The number of edges connected directly to a node
<div align="center">
    <img src="resources/path.png" width="35%" height="35%" title="Undirected Graph Degree">

*The degree of A is 2*
</div>

#### <u>Directed Graph Degree</u>

Directed Graphs have two types of degrees, namely

- **Indegree** - The number of edges entering the node. 
- **Outdegree** - The number of edges leaving the node.

<br/>
<div align="center">
    <img src="resources/digraph.png" width="35%" height="35%" title="Directed Graph Degree">
</div>

| Node | Indegree | Outdegree |
|------|----------|-----------|
| A    | 1        | 1         |
| B    | 1        | 1         |

### <u>Source Vertex</u>
A vertex whose *indegree is zero* is referred as source vertex.

### <u>Sink Vertex</u>
A vertex whose *outdegree is zero* is referred as sink vertex.

### <u>Isolated Vertex</u>
If a graph has onlu one vertex in it, it is a isolated graph vertex.

### <u> Weighted Graph</u>
If every edge in the graph is assigned some weight (or) value, then the graph is called *Weighted Graph*

<div align="center">
    <img src="resources/weighted_graph.png" width="35%" height="35%" title="Weighted Graph">

*Weighted Graph*
</div>

### <u>Pendant Vertex</u>
A vertex whose indegree is 1 and outdegree is 0 is referred to as *Pendant Vertex*.

## Representation of a Graph

### <u>Incidence Matrix</u>
A graph containing m vertices and n edges can be represented by a matrix with m rows and n columns. The matrix is formed by storing 1 in the i<sup>th</sup> row and j<sup>th</sup> column corresponding to the matrix, if there exists a i<sup>th</sup> vertex connected to one end of the j<sup>th</sup> edge and a 0 if there is no i<sup>th</sup> vertex connected to any end of the j<sup>th</sup> edge of the graph, such a matrix is referred to as *incidence matrix*.

<br/>

<p align="center"><i>Consider the given weighted graph</i></p>

<div align="center">
    <img src="resources/incidence_matrix.png" width="35%" height="35%" title="Weighted Graph">
</div>


    incidence_matrix[i][j] = 1, if there is an edge
                             0, otherwise

The Incidence Matrix for this graph is given by:

|               | E<sub>1</sub> | E<sub>2</sub> | E<sub>3</sub> |
|---------------|---------------|---------------|---------------|
| V<sub>1</sub> | 1             | 0             | 0             |
| V<sub>2</sub> | 0             | 1             | 0             |
| V<sub>3</sub> | 0             | 0             | 1             |
| V<sub>4</sub> | 1             | 1             | 1             |
