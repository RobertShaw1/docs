---
layout: default
description: The Graphs tab provides a viewer facility for graph data stored in ArangoDB
---
Graphs
======

The *Graphs* tab provides a viewer facility for graph data stored in ArangoDB.
It allows browsing ArangoDB graphs stored in the *_graphs* system collection or
a graph consisting of an arbitrary vertex and [edge collection](appendix-glossary.html#edge-collection).

![manage graphs](images/graphsView.png)

Please note that the graph viewer requires SVG support in your browser.
Especially Internet Explorer browsers older than version 9 are likely to not
support this.

![display graphs](images/graphViewer.png)

Left Toolbar Functions:

- Fold/Unfold a node / drag graph
- Drag a node
- Edit a node or edge
- Drag and drop a new edge between two nodes
- Add a node
- Remove a node

Top Toolbar Functions:

- Filter graph by attribute
- Add node by attribute 
- Configure labels of nodes or edges
- Group nodes by attribute
- Limit count of rendered nodes
