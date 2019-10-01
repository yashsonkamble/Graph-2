# Graph-2

## Problem1: Critical Connections in a Network (https://leetcode.com/problems/critical-connections-in-a-network/)

There are n servers numbered from 0 to n-1 connected by undirected server-to-server connections forming a network where connections[i] = [a, b] represents a connection between servers a and b. Any server can reach any other server directly or indirectly through the network.

A critical connection is a connection that, if removed, will make some server unable to reach some other server.

Return all critical connections in the network in any order.

Example 1:

Input: n = 4, connections = [[0,1],[1,2],[2,0],[1,3]]

Output: [[1,3]]

Explanation: [[3,1]] is also accepted.
 
Constraints:

1 <= n <= 10^5

n-1 <= connections.length <= 10^5

connections[i][0] != connections[i][1]

There are no repeated connections.

## Problem2: Minimize Malware Spread (https://leetcode.com/problems/minimize-malware-spread/)

In a network of nodes, each node i is directly connected to another node j if and only if graph[i][j] = 1.

Some nodes initial are initially infected by malware.  Whenever two nodes are directly connected and at least one of those two nodes is infected by malware, both nodes will be infected by malware.  This spread of malware will continue until no more nodes can be infected in this manner.

Suppose M(initial) is the final number of nodes infected with malware in the entire network, after the spread of malware stops.

We will remove one node from the initial list.  Return the node that if removed, would minimize M(initial).  If multiple nodes could be removed to minimize M(initial), return such a node with the smallest index.

Note that if a node was removed from the initial list of infected nodes, it may still be infected later as a result of the malware spread.

Example 1:

Input: graph = [[1,1,0],[1,1,0],[0,0,1]], initial = [0,1]

Output: 0

Example 2:

Input: graph = [[1,0,0],[0,1,0],[0,0,1]], initial = [0,2]

Output: 0

Example 3:

Input: graph = [[1,1,1],[1,1,1],[1,1,1]], initial = [1,2]

Output: 1
 

Note:

1 < graph.length = graph[0].length <= 300

0 <= graph[i][j] == graph[j][i] <= 1

graph[i][i] = 1

1 <= initial.length < graph.length

0 <= initial[i] < graph.length
