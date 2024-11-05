Directed Graph Management with String Operations
This code defines a Graph class that represents a directed graph and allows for various string-based operations, including insertion, search, and deletion. The graph maintains vertices as characters and manages edges with adjacency lists and weighted connections. Additionally, the program provides a simple CLI interface for interacting with the graph and a visualization feature using NetworkX and Matplotlib.

Detailed Breakdown of the Code:
Graph Class Initialization:

self.adj_list: Adjacency list representing the graph structure, where each key is a vertex and its value is a list of connected vertices.
self.adj_isend: Tracks incoming edge counts for vertices, where adj_isend[i] corresponds to the incoming edges for vertex i.
self.con_wei: 2D list for edge weights between vertices, where con_wei[i][j] holds the weight of the edge from vertex i to j.
self.cou: Counts the number of edges connected to each vertex.
String Insertion (insert_string):

Adds a new string as a path in the graph:
Converts each character to a numeric index and adds it as a vertex.
Updates the edge weight for each character transition in the string.
If a character in the string is already connected, increments the corresponding weight.
Vertex and Edge Management:

add_vertex: Ensures the specified vertex exists in the adjacency list.
add_edge: Adds a directed edge between two vertices. If the edge already exists, increments the weight; otherwise, it initializes the edge and weight.
Graph Printing (print_g):

Prints the adjacency list representation of the graph, where vertices are displayed as characters.
String Search (find_word):

Checks if a given string exists as a path in the graph by verifying that each character transition exists in the adjacency list.
String Deletion (delete_str):

Deletes a path corresponding to a given string if it exists:
Traverses the string in the adjacency list, removing edges with weights of 1 and decrementing weights for multi-edge connections.
Cleans up isolated vertices with no connections after deletion.
ASCII Conversion (convert_ascii):

Converts characters to numeric indices based on ASCII values, mapping lowercase and uppercase letters consistently.
User Interface:

CLI options allow users to:
Insert a string (option 1)
Search for a string (option 2)
Delete a string (option 3)
Print the graph’s adjacency list (option 4)
Visualize the graph with NetworkX and Matplotlib (option 5)
Exit (option 6)
Graph Visualization (visualize graph):

Uses NetworkX to create a visual representation of the graph, drawing vertices as nodes and edges with labels.
Key Points:
Weighted Edges: Tracks multiple occurrences of the same transition, useful for weighted path analysis.
Character-based Graph: Converts characters to numeric indices for vertex representation, allowing compatibility with any alphabetic string.
Interactive CLI: Provides a straightforward interface for string-based graph manipulation.
Graph Visualization: Offers a graphical view of the graph structure to aid in understanding the connections.
