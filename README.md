# sorting
Topological sorting is used for ordering tasks or nodes in a directed acyclic graph (DAG) such that for every directed edge uv from vertex u to vertex v, u comes before v in the ordering. Here's a JavaScript implementation of topological sorting using depth-first search (DFS):
I defined a Graph class representing the directed graph.
The addEdge method adds an edge between two vertices.
The topologicalSort method performs topological sorting using depth-first search (DFS). It initializes a stack to store the sorted vertices and a visited map to keep track of visited vertices.
I defined a helper DFS function that explores all vertices reachable from a given vertex recursively.
I then performed DFS on each vertex in the graph and push the visited vertices onto the stack.
Finally, I reversed the stack to obtain the topologically sorted order.
You can create a Graph object, add edges between vertices, and then call the topologicalSort method to get the topologically sorted vertices.
