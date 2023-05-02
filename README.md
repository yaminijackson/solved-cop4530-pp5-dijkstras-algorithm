Download Link: https://assignmentchef.com/product/solved-cop4530-pp5-dijkstras-algorithm
<br>
For Programming Project 5, you will be implementing a undirected weighted Graph ADT and performing Dijkstra’s Algorithm to find the shortest path between two vertices. Your graph can be implemented using either an adjacency list, adjacency matrix, or an incidence matrix. Your graph will implement methods that add and remove vertices, add and remove edges, and calculate the shortest path. Each vertex in your graph will have a string label that will help identify that vertex to you and the test file.

A large portion of this assignment is researching and implementing Dijkstra’s Algorithm. There is information about this algorithm in your textbook and widely available on the web.

<strong>Abstract Class Methods </strong>

<strong>void addVertex(std::string label) </strong>

Creates and adds a vertex to the graph with label. No two vertices should have the same label.

<h2>void removeVertex(std::string label)</h2>

Removes the vertex with label from the graph. Also removes the edges between that vertex and the other vertices of the graph.

<h2>void addEdge(std::string label1, std::string label2, unsigned long weight)</h2>

Adds an edge of value weight to the graph between the vertex with label1 and the vertex with label2. A vertex with label1 and a vertex with label2 must both exist, there must not already be an edge between those vertices, and a vertex cannot have an edge to itself.

<h2>void removeEdge(std::string label1, std::string label2)</h2>

Removes the edge from the graph between the vertex with label1 and the vertex with label2. A vertex with label1 and a vertex with label2 must both exist and there must be an edge between those vertices

<h2>unsigned long shortestPath(std::string startLabel, std::string endLabel, std::vector&lt;std::string&gt; &amp;path)</h2>

Calculates the shortest path between the vertex with startLabel and the vertex with endLabel using Dijkstra’s Algorithm. A vector is passed into the method that stores the shortest path between the vertices. The return value is the sum of the edges between the start and end vertices on the shortest path.

<h1>Examples</h1>

Below in an example of the functionality of the implemented graph:

<strong>std::vector&lt;std::string&gt; vertices1 = { “1”, “2”, “3”, “4”, “5”, “6” }; std::vector&lt;std::tuple&lt;std::string, std::string, unsigned long&gt;&gt; edges1 = { {“1”, “2”, 7}, {“1”, “3”, 9}, {“1”, “6”, 14}, {“2”, “3”, 10}, {“2”, “4”, 15}, {“3”, “4”, 11}, {“3”, “6”, 2}, {“4”, “5”, 6}, {“5”, “6”, 9} }; </strong>

<strong>for (const auto label : vertices1) g.addVertex(label); for (const auto &amp;tuple : edges1) g.addEdge(std::get&lt;0&gt;(tuple), std::get&lt;1&gt;(tuple), std::get&lt;2&gt;(tuple)); g.shortestPath(“1”, “5”, path); // == 20 g.shortestPath(“1”, “5”, path); // = { “1”, “3”, “6”, “5” } </strong>

<h1>Deliverables</h1>

Please submit complete projects as zipped folders. The zipped folder should contain:

<ul>

 <li>cpp (Your written Graph class)</li>

 <li>hpp (Your written Graph class)</li>

 <li>hpp (The provided base class)</li>

 <li>cpp (Test file)</li>

 <li>hpp (Catch2 Header)</li>

</ul>

And any additional source and header files needed for your project.

<h1>Hints</h1>

Though it may be appealing to use an adjacency matrix, it might be simpler to complete this algorithm using an adjacency list for each vertex.

I suggest using a separate class for your edge and vertex.

Remember to write a destructor for your graphs!

<h1>Rubric</h1>

Any code that does not compile will receive a zero for this project.

<table width="624">

 <tbody>

  <tr>

   <td width="466"><strong>Criteria</strong></td>

   <td width="157"><strong>Points</strong></td>

  </tr>

  <tr>

   <td width="466"><strong>Should calculate the distance of the shortest path for graph 1</strong></td>

   <td width="157">5</td>

  </tr>

  <tr>

   <td width="466"><strong>Should have the labels for the shortest path for graph 1</strong></td>

   <td width="157">5</td>

  </tr>

  <tr>

   <td width="466"><strong>Should calculate the distance of the shortest path for graph 2</strong></td>

   <td width="157">5</td>

  </tr>

  <tr>

   <td width="466"><strong>Should have the labels for the shortest path for graph 2</strong></td>

   <td width="157">5</td>

  </tr>

  <tr>

   <td width="466"><strong>Should calculate the distance of the shortest path for graph 3</strong></td>

   <td width="157">5</td>

  </tr>

  <tr>

   <td width="466"><strong>Should have the labels for the shortest path for graph 3</strong></td>

   <td width="157">5</td>

  </tr>

  <tr>

   <td width="466"><strong>Code implements Dijkstra’s Algorithm</strong></td>

   <td width="157">6</td>

  </tr>

  <tr>

   <td width="466"><strong>Code uses object oriented design principles  (Separate headers and sources, where applicable)</strong></td>

   <td width="157">2</td>

  </tr>

  <tr>

   <td width="466"><strong>Code is well documented</strong></td>

   <td width="157">2</td>

  </tr>

  <tr>

   <td width="466"><strong>Total Points</strong></td>

   <td width="157"><strong>40</strong></td>

  </tr>

 </tbody>

</table>


