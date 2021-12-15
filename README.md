# Weighted Directed Graphs
## NEED TO FINISH README!
## Assignment 2 - Object Oriented Programming 
**Netanel Levine**   
**Yanir Cohen**    
--- 
This project is about simulating and illustrating algorithms on graphs. In this project we will load graphs from Json files and will activate specific algorithms on those graphs. In addition we will create a UI that illustrates the algorithm we activated on the graph.
 
---
## Project UML

   <p align="center">
    <img src="https://github.com/yanir75/weighted-graphs/blob/main/uml/Graph%20UML.png">
   </p>

---

## Results
|      functions\Number of nodes     | **1000** | **10000** | **100000** | **1000000** |
|-----------|--------|--------|--------|--------|
|**is Connected**|	0.01s	 | 0.2s  |	 0.5s  | 2.8s  | 
|**TSP 10 Nodes** |0.02s	 | 0.5s   |	1s  | 36.9s  | 
|**Center** |2s	 | 5.5m   |	NULL   | NULL  | 
|**Shortest Path** |0.002s | 0.01s   |	5s   | 14s  | 

------
##GUI
   <p align="center">
    <img src="https://github.com/yanir75/weighted-graphs/blob/main/uml/graph.png">
   </p>
---

## Sources:

  - <a href="https://www.youtube.com/watch?v=CerlT7tTZfY&t">Djikstra's algorithm using a priority queue - Youtube</a>
  - <a href="https://www.geeksforgeeks.org/connectivity-in-a-directed-graph/">Check if a graph is strongly connected</a>
