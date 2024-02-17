class Graph {
    constructor(vertices) {
        this.vertices = vertices;
        this.adjacencyList = new Map();
        for (let i = 0; i < this.vertices.length; i++) {
            this.adjacencyList.set(this.vertices[i], []);
        }
    }

    addEdge(u, v) {
        this.adjacencyList.get(u).push(v);
    }

    topologicalSort() {
        const visited = new Map();
        const stack = [];

        // Initialize visited map
        this.vertices.forEach(vertex => {
            visited.set(vertex, false);
        });

        // Depth-first search recursive function
        const dfs = (v, visited, stack) => {
            visited.set(v, true);

            const neighbors = this.adjacencyList.get(v);
            neighbors.forEach(neighbor => {
                if (!visited.get(neighbor)) {
                    dfs(neighbor, visited, stack);
                }
            });

            stack.push(v);
        };

        // Perform DFS on each vertex
        this.vertices.forEach(vertex => {
            if (!visited.get(vertex)) {
                dfs(vertex, visited, stack);
            }
        });

        // Reverse the order to get topological sort
        return stack.reverse();
    }
}

// Example usage:
const vertices = ['A', 'B', 'C', 'D', 'E', 'F'];
const graph = new Graph(vertices);
graph.addEdge('A', 'B');
graph.addEdge('A', 'C');
graph.addEdge('B', 'D');
graph.addEdge('C', 'D');
graph.addEdge('D', 'E');
graph.addEdge('E', 'F');

const sortedVertices = graph.topologicalSort();
console.log("Topologically Sorted Vertices:", sortedVertices);
