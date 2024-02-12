# Ex.No: 1  Implementation of Breadth First Search 
### DATE:12-06-2024                                                                            
### REGISTER NUMBER : 212221220040
### AIM: 
To write a python program to implement Breadth first Search.
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function bfs and take the set “visited” is empty and “queue” is empty
4. Search start with initial node and add the node to visited and queue.
5. For each neighbor node, check node is not in visited then add node to visited and queue list.
6.  Creating loop to print the visited node.
7.   Call the bfs function by passing arguments visited, graph and starting node.
8.   Stop the program.

### Program:
# Using a Python dictionary to act as an adjacency list
graph = {
  '5' : ['3','7'],
  '3' : ['2', '4'],
  '7' : ['8'],
  '2' : [],
  '4' : ['8'],
  '8' : []
}
visited = set() # Set to keep track of visited nodes of graph.
def dfs(visited,graph,node):  #function for dfs 
    if node not in visited:
        	print (node)
        	visited.add(node)
        	for neighbour in graph[node]:
        	    dfs(visited,graph,neighbour)
# Driver Code
print("Following is the Depth-First Search")
dfs(visited,graph,'5')
~~~
~~~
### Output:
![Screenshot 2024-02-12 160705](https://github.com/PREETHI-B0/AI_Lab_2023-24/assets/136311079/9410902b-2e10-424d-b3dc-714d26259aff)
~~~
~~~
### Result:
Thus the breadth first search order was found sucessfully.
~~~
