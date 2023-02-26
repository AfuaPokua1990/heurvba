# heurvba
Working with an emergency response team and need to decide which critical locations to visit and in which order. The following rules are adopted to prioritise more urgent locations without compromising on travelling time: 

If the locations are organised in C clusters, where the first cluster is the most urgent, and the last cluster is the least urgent, the team is only allowed to visit locations in the d most urgent clusters which have not been completely visited. For example: if your team has visited all locations in the most urgent cluster C1, and the team still has to visit some locations in the cluster C2, if d=3, the next location you visit can only be part of clusters 2, 3, 4, or 5 (i.e., clusters c, c+1,…, c+d). Furthermore, each cluster-location has a score for completion. More urgent clusters have higher scores. You are also given a maximum time T to complete the mission. 

The aim is to define the best sequence of locations to visit before returning to your team base within the time frame, so that your overall score (the sum of the scores of the completed locations) is maximised. The problem can be formalised as follows:
•	The locations i= 0,1, …, n.  The location 0 is the starting and ending point of your tour (i.e., the team base)
•	The distance between the locations are given, dij , i,j=0,.., n (as well as the coordinates of each location for ease of representation).  
•	The time available to complete the tour is at most T units. The time spent at each location is considered to be negligible. 
•	The clusters c=1,…,C. and their associated scores si, with si > sj, if i < j. Note that this data structure index starts from 1, because the location 0 is not associated to a cluster. 
The problem definition is similar to the TSP, but with additional components (time limits, clusters, cluster scores).

Task:

•	Develop a constructive heuristic to solve the team routing optimisation problem.
•	Develop a local search heuristic to solve the team routing optimisation problem.
•	Develop a metaheuristic to solve the team routing optimisation problem.

Ten instances in “.txt” format are provided. The computational experiments will be performed on these instances. The instances contain:
•	The number of locations
•	The number of clusters
•	The maximum tour duration
•	The value of d
•	The scores associated to each cluster
•	The cluster to which each location belongs
•	The coordinates X of the locations
•	The coordinates Y of the locations. 

Attached is an Excel file containing a VBA module. This module has code for reading the instances and filling suitable data structures, as well as a function that evaluates the feasibility of a given solution, and provides the objective value if it is feasible. The total execution time of the final algorithms should be no more than five (5) minutes.
