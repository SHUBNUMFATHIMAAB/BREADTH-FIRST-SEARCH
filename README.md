ExpNo 3 : Implement Breadth First Search Traversal of a Graph
Name:
Register Number:
Aim:
To Implement Breadth First Search Traversal of a Graph using Python 3.

Theory:
Breadth-First Traversal (or Search) for a graph is like the Breadth-First Traversal of a tree. The only catch here is that, unlike trees, graphs may contain cycles so that we may come to the same node again. To avoid processing a node more than once, we divide the vertices into two categories:

Visited
Not Visited
A Boolean visited array is used to mark the visited vertices. For simplicity, it is assumed that all vertices are reachable from the starting vertex. BFS uses a queue data structure for traversal.

How does BFS work?
Starting from the root, all the nodes at a particular level are visited first, and then the next level nodes are traversed until all the nodes are visited. To do this, a queue is used. All the adjacent unvisited nodes of the current level are pushed into the queue, and the current-level nodes are marked visited and popped from the queue. Illustration: Let us understand the working of the algorithm with the help of the following example. Step1: Initially queue and visited arrays are empty.

<img width="832" height="302" alt="image" src="https://github.com/user-attachments/assets/e4c35346-2b8b-46f7-a1ea-27c95b902cee" />

Queue and visited arrays are empty initially. 

Step2: Push node 0 into queue and mark it visited.

<img width="815" height="288" alt="image" src="https://github.com/user-attachments/assets/360d19db-a2b6-4fe8-be2f-ca89d86661ab" />

Push node 0 into queue and mark it visited. 

Step 3: Remove node 0 from the front of queue and visit the unvisited neighbours and push them into queue.

<img width="817" height="293" alt="image" src="https://github.com/user-attachments/assets/3d825a02-3255-4104-8217-d89640d34399" />

Step 4: Remove node 1 from the front of queue and visit the unvisited neighbours and push them into queue.

<img width="817" height="286" alt="image" src="https://github.com/user-attachments/assets/9c5f7d9c-ec5c-4f8c-a1ac-d0a25fa06139" />

Step 5: Remove node 2 from the front of queue and visit the unvisited neighbours and push them into queue.

<img width="820" height="286" alt="image" src="https://github.com/user-attachments/assets/3fd43964-0ff6-4abb-a90d-a4c6b1c1c8d0" />

Step 6: Remove node 3 from the front of queue and visit the unvisited neighbours and push them into queue. As we can see that every neighbours of node 3 is visited, so move to the next node that are in the front of the queue.

<img width="802" height="286" alt="image" src="https://github.com/user-attachments/assets/adc52672-4970-4c9d-9f23-621fa2b098d5" />

Steps 7: Remove node 4 from the front of queue and visit the unvisited neighbours and push them into queue. As we can see that every neighbours of node 4 are visited, so move to the next node that is in the front of the queue.

<img width="820" height="295" alt="image" src="https://github.com/user-attachments/assets/698682d6-cb61-4661-a3c2-802ce7d283a8" />

Remove node 4 from the front of queue and visit the unvisited neighbours and push them into queue. Now, Queue becomes empty, So, terminate these process of iteration.

Algorithm:
Construct a Graph with Nodes and Edges
Breadth First Uses Queue and iterates through the Queue for Traversal.
Insert a Start Node into the Queue.
Find its Successors Or neighbors and Check whether the node is visited or not.
If Not Visited, add it to the Queue. Else Continue.
Iterate steps 4 and 5 until all nodes get visited, and there are no more unvisited nodes.

Sample Input
5 6
0 1
0 2
1 2
1 3
2 4
3 4
Sample Output
['0', '1', '2', '3', '4']

Output:
<img width="272" height="201" alt="image" src="https://github.com/user-attachments/assets/50238949-cb3f-498e-b884-63874c9c71f0" />

Result:
Thus,a Graph was constructed and implementation of Breadth First Search for the same graph was done successfully.
