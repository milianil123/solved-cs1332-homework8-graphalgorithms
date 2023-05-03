Download Link: https://assignmentchef.com/product/solved-cs1332-homework8-graphalgorithms
<br>
For this assignment, you will code 3 different graph algorithms. This homework has many files included, so be sure to read ALL of the documentation given before asking questions.

<h2>Graph Data Structure</h2>

You are provided a Graph class. The important methods to note from this class are:

<ul>

 <li>getVertices returns a Set of Vertex objects (another class provided to you) associated with a graph.</li>

 <li>getEdges returns a Set of Edge objects (another class provided to you) associated with a graph.</li>

 <li>getAdjList returns a Map that maps Vertex objects to Lists of VertexDistance This Map is especially important for traversing the graph, as it will efficiently provide you the edges adjacent to any vertex (the outgoing edges of any vertex). For example, consider an adjacency list where vertex A is associated with a list that includes a VertexDistance object with vertex B and distance 2 and another VertexDistance object with vertex C and distance 3. This implies that in this graph, there is an edge from vertex A to vertex B of weight 2 and another edge from vertex A to vertex C of weight 3.</li>

</ul>

<h2>Vertex Distance Data Structure</h2>

In the Graph class and Dijkstra’s algorithm, you will be using the VertexDistance class implementation that we have provided. In the Graph class, this data structure is used by the adjacency list to represent which vertices a vertex is connected to. In Dijkstra’s algorithm, you should use this data structure along with a PriorityQueue. When utilizing VertexDistance in this algorithm, the vertex attribute should represent the destination vertex and the distance attribute should represent the minimum cumulative path cost from the source vertex to the destination vertex.

<h2>DFS</h2>

Depth-First Search is a search algorithm that visits vertices in a depth based order. Similar to pre/post/inorder traversal in BSTs, it depends on a Stack-like behavior to work. In your implementation, the Stack will be the recursive stack, meaning you should not create a Stack data structure. It searches along one path of vertices from the start vertex and backtracks once it hits a dead end or a visited vertex until it finds another path to continue along. <strong>Your implementation of DFS must be recursive to receive credit.</strong>

<h2>Single-Source Shortest Path (Dijkstra’s Algorithm)</h2>

The next algorithm is Dijkstra’s Algorithm. This algorithm finds the shortest path from one vertex to all of the other vertices in the graph. This algorithm only works for non-negative edge weights, so you may assume all edge weights for this algorithm will be non-negative. In order to keep track of the cumulative distance from the source vertex to the vertices you visit in this algorithm, you will need to use the VertexDistance data structure we are providing you. At any stage throughout the algorithm, the PriorityQueue of VertexDistance objects will tell you which vertex currently has the minimum cumulative distance from the source vertex.

There are two commonly implemented terminating condition variants for Dijkstra’s Algorithm. The first variant is where you depend purely on the PriorityQueue to determine when to terminate. You only terminate once the PriorityQueue is empty. The other variant, the classic variant, is the version where you maintain both a PriorityQueue and a visited set. To terminate, still check if the PriorityQueue is empty, but you can also terminate early once all the vertices are in the visited set. <strong>You should implement the classic variant for this assignment. </strong>The classic variant, while using more memory, is usually more time efficient since there is an extra condition that could allow it to terminate early.

<h2>Self-Loops and Parallel Edges</h2>

In this framework, self-loops and parallel edges work as you would expect. If you recall, self-loops are edges from a vertex to itself. Parallel edges are multiple edges with the same orientation between two vertices. In other words, parallel edges are edges that are incident on precisely the same vertices. These cases are valid test cases, and you should expect them to be tested. However, most implementations of these algorithms handle these cases automatically, so you shouldn’t have to worry too much about them when implementing the algorithms.

<h2>Prim’s Algorithm</h2>

A tree is a graph that is acyclic and connected. A spanning tree is a subgraph that contains all the vertices of the original graph and is a tree. An MST has two main qualities: being minimum and a spanning tree. Being minimum dictates that the spanning tree’s sum of edge weights must be minimized.

By the properties of a spanning tree, any valid MST must have |<em>V </em>| − 1 edges in it. However, since all undirected edges are specified as two directional edges, a valid MST for your implementation will have 2(|<em>V </em>| − 1) edges in it.

Prim’s algorithm builds the MST outward from a single component, starting with a starting vertex. At each step, the algorithm adds the cheapest edge connected to the incomplete MST that does not cause a cycle. Cycle detection can be handled with a visited set like in Dijkstra’s..

<h2>Visualizations of Graphs</h2>