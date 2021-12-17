# Weighted Directed Graphs
## Assignment 2 - Object Oriented Programming
**Netanel Levine**   
**Yanir Cohen**
--- 
In this project we will illustrate to the best of our capabilities a graph and algorithms on this graph.  
The graph resembles a small area with significant places and ways to transport between each place.  
This can be used for a variety of purposes (best route between cities,routes etc). In our project we will try to simulate it as closly as can be to a small area as we said before.
 
---
## Project UML

<img src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/uml/Arcithecture.png">
---

## Structure

Our project structure
1. Node, Node represents a significant place in our university i.e building,market etc.
   Each node holds information regarding itself, street name, tag etc.
3. Location , GeoLocation represents the real life (latitude and longitude).
5. Edge , Edge resembles a way of trasport (road,sidewalk etc) between two nodes.  
   Edges contain information as well for example road 4 ,etc.
   Not all edges are two way edges. Because there are one way roads.
   In addition the cost of each edge is not the same for similar reasons.

## Graph:
Graph is built upon founded on those.
Graph contains all the nodes and all the edges in a given place, nodes can be added and removed, same goes for edges.  
Through it we will represent a small area with places of significance and a way to modify them quickly providing elasticity.

## Algorithms:
Algorithms are the main event over here. As can be seen this graph can represent real life places.
As so we would like the best way from a node to another node, this will be done by calculating the best way through each edges from each node. This will be done with Shortest path.  
In addition we would like to know the time of each trip, as for we can retrieve the cost of the way from one node to another. This will be done with Shortest path dist.  
Moreover we would like to know the best way between one node with a few stops on the way. This will be done through the best effor TSP.  
At last we would like to know the center of the place, which place is probably closest to all. This will be done through Center.  
Those are the main functions we will use to represent as closely as possible real life situations.

## Gui:
Finally, we would like a visualistic way to show the users the graph, edges, best roads etc.  
As a result we created user interface which will visualize the graph and algorithms mentioned above.  
It will display the nodes and edges between all the nodes. Algorithms will be easily activated to illustrate the situations.  
This will be a user friendly gui which aspires to be easy to use, adjustable and illustrate our project as best as we can.  
In conclusion, you will be able to see the way and understand much better what is the best result for your request.

## Results
Here are the results of the algorithm on a connected graph.  
The left column has the function we activated. The first row has the number of nodes.
|        | **1000/20000** | **10000/200000** | **100000/2000000** | **1000000/200000000** |
|-----------|--------|--------|--------|--------|
|**is Connected**|	0.01s	 | 0.2s  |	 5-17s  | NULL  |
|**TSP 10 Nodes** |0.02s	 | 0.5-1s   |	1-10s  | NULL  |
|**Center** |2s	 | 5.5m   |	NULL   | NULL  |
|**Shortest Path** |0.02s | 0.04s   |	5s   | NULL  |

We are able to generate a graph with 1mk nodes and 20mk edges but are unable to run any algorithm on it, due to heap space.
The results vary depends on how th graph is generated.

Since we did not create the graph randomly most of the time, it didn't take so much time.

---
## GUI
Implementing the GUI was a major part (and not easy at all) of this project
because we wanted to give the user the Max comfort and simplicity that we could think of.

### Structure
the GUI contains 4 classes:
1. **MyFrame** - MyFrame is the main part of this section, basically it holds all the components of the programs
   and creating them.

2. **MyPanel** - MyPanel is where the magic happen, MyPanel is the main panel that holds all the graph structure
   and responsible for drawing it correctly.

3. **Help** - Help is a small class that creates only a new JFrame to the main frame. The purpose of Help
   is to open a new window that contains all the shortcuts available.

4. **MyGraph_GUI** - MyGraph_GUI creates the main JFrame and then activating the GUI.

### Tutorial
Here we attached a simple image of the GUI.<br>
**The frame of the GUI has 4 main parts:**
1. **Menu Bar**
2. **Buttons Panel**
3. **The Graph**
4. **Action Log**
<img align="left"  src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/InitIMG.jpg">  

### Explanation of the parts
1. **Menu Bar/Buttons Panel** - From them the user can execute all kind of features.  
  Not all the features in the Menu Bar appears in the Buttons Panel, but all the features in Buttons Panel appears in the Menu Bar.  

    **Features list:**
<br><br>***Note: the obvious features doesn't have an explanation/examples because their pretty simple.***<br>
      1. **Algorithms:**<br>
         - isConnected *// also in the Algorithms bar*,  [jump to isConnected](#isConnected)
         - TSP *// also in the Algorithms bar*,  [jump to TSP](#TSP)
         - Center *// also in the Algorithms bar*,  [jump to Center](#Center)
         - ShortestPath *// also in the Algorithms bar*,  [jump to ShortestPath](#ShortestPath)
      2. **Edit Graph:**<br>
         - Remove Node *// also in the Edit bar*, [jump to Remove Node](#Remove-Node)
         - Remove Edge *// also in the Edit bar*, [jump to Remove Edge](#Remove-Edge)
         - Add Node *// also in the Edit bar*, [jump to Add Node](#Add-Node)
         - Add Edge *// also in the Edit bar*, [jump to Add Edge](#Add-Edge)
      3. **View settings:**<br>
         - Hide/Show Buttons *// only in the View bar*, [jump to Hide/Show Buttons](#hideshow-buttons)
         - Full Screen *// only in the View bar*
         - Default Screen *// only in the View bar*
         - Costume Screen *// only in the View bar*
      4. **Help:**<br>
         - Shortcuts *// only in the Help bar*, [jump to Shortcuts](#Shortcuts)
      5. **File:**<br>
         - Load *// also in the File bar*
         - Save *// also in the File bar*
         - Clear *// also in the File bar*
         - Reset Graph *// also in the File bar*
         - Exit *// only in the File bar*<br>
         

2. **The Graph** - The Graph holds all the relevant data in order to keep updating the drawings.
3. **Action Log** - The Action Log purpose is helping the user to control and monitor all the changes he did with the graph.
  Every Button click or action made in the program the Action Log writes it down, for example: if the user clicked on the
  Center button, so after he got an update through a popup message it's also written in the Action Log.

<br><br>

### isConnected:
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/1.png"> 

[Arduino](https://en.wikipedia.org/wiki/Arduino) (/ɑːrˈdwiːnoʊ/) -  After isConnected is pressed, the user receives a popup window with answer to the question:  
***is the Graph strongly connected?*** 
<br>[jump to Tutorial](#explanation-of-the-parts)<br><br><br><br><br><br><br><br><br><br><br><br><br>


### TSP:
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/2.png"> 

[Arduino](https://en.wikipedia.org/wiki/Arduino) (/ɑːrˈdwiːnoʊ/) - In the TSP we decided to give the user two ways to type the input:  
1. One long String.
2. Each time one String.
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>


**One long String:**
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/22.png">

 - This option allows the user to type
all the input in one time without the
need to type each time one Node.
* The String format is:  
***"5 3 9 12 15 7 0"***, each Node is seperated with a single *space* character.
<br><br><br><br><br><br><br><br><br><br><br>


**Each time one String:**
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/222.png">

 - This option will create a new popup window that asks the user to enter another Node, this process will finish once the user type *"done"/"DONE"*.
   <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>


**Output:**
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/2222.png">

- The path will be colored in light purple on the Graph.
- At the action log the user can see:<br>
  1. List of the Nodes he entered.<br>
  2. List of the path in the right order that go through every one of the Nodes he entered.<br>
  3. In case of any Invalid input the user will receive a popup window mentioning the problem, and it will be written in the action log too.<br>
  <br>[jump to Tutorial](#explanation-of-the-parts)<br><br><br><br>

### Center:
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/3.png"> 

[Arduino](https://en.wikipedia.org/wiki/Arduino) (/ɑːrˈdwiːnoʊ/) - Once the user pressed the Center 3 things will happen:<br>
1. Popup window will with the ID of the Node that our Algorithm chose to be the Center.
2. The Node with this ID will change his color from blue to red, and also the white box where his ID written will change to yellow.
3. The action log will write also this Node as the Center.
   <br><br><br><br><br><br>


**Output:**
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/33.jpg">
 <br>[jump to Tutorial](#explanation-of-the-parts)<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### ShortestPath:
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/4.png"> 

[Arduino](https://en.wikipedia.org/wiki/Arduino) (/ɑːrˈdwiːnoʊ/) - Once the user pressed the ShortestPath 3 things will happen:<br>
1. Popup window will open and ask the user to enter source Node and destination Node
2. The ShortestPath that our Algorithm chose will be marked in green.
3. The action log will write 2 things:
   1. Weight of the ShortestPath.
   2. String represents the ShortestPath in the right order.
      <br><br><br><br>


**Output:**  
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/44.png">
In case the user entered an invalid input, he will get a popup window about this problem and this will also be written in the log.<br>
There are 2 types of wrong inputs:<br>
1. No input at all or String of chars, something that is not an Integer.
2. source/destination/both are not in the Graph.
<br>[jump to Tutorial](#explanation-of-the-parts)<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### Remove Node:
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/5.jpg"> 

[Arduino](https://en.wikipedia.org/wiki/Arduino) (/ɑːrˈdwiːnoʊ/) - Remove Node is simple, give me ID, and I'll delete the Node.  
After the user types the key the program check if this Node is in the Graph, if true it deletes the Node, else meaning wrong input.<br>
Wrong values/inputs are:
1. No input or a String.
2. ID that is not in the Graph.



**Output:**  
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/55.png">
If the input is valid the user will see that the Node he picked was removed from the Graph and all it's Edges too.<br>
Otherwise, the user will get a popup window with the problem, and it will be added to the action log.
If the Node was deleted at the Action log will be written, the Node number that was removed.
   <br>[jump to Tutorial](#explanation-of-the-parts)<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### Remove Edge:
3. The action log will write 2 things:
    1. Weight of the ShortestPath.
    2. String represents the ShortestPath in the right order.
       <br><br><br><br>


**Output:**  
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/6.jpg">
In case the user entered an invalid input, he will get a popup window about this problem and this will also be written in the log.<br>
There are 2 types of wrong inputs:<br>
1. No input at all or String of chars, something that is not an Integer.
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/66.png"> 

[Arduino](https://en.wikipedia.org/wiki/Arduino) (/ɑːrˈdwiːnoʊ/) - Once the user pressed the ShortestPath 3 things will happen:<br>
1. Popup window will open and ask the user to enter source Node and destination Node
2. The ShortestPath that our Algorithm chose will be marked in green.
2. source/destination/both are not in the Graph.
   <br>[jump to Tutorial](#explanation-of-the-parts)<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### Add Node:
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/7.png"> 

[Arduino](https://en.wikipedia.org/wiki/Arduino) (/ɑːrˈdwiːnoʊ/) - Once the user pressed the ShortestPath 3 things will happen:<br>
1. Popup window will open and ask the user to enter source Node and destination Node
2. The ShortestPath that our Algorithm chose will be marked in green.
3. The action log will write 2 things:
    1. Weight of the ShortestPath.
    2. String represents the ShortestPath in the right order.
       <br><br><br><br>


**Output:**  
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/77.jpg">
In case the user entered an invalid input, he will get a popup window about this problem and this will also be written in the log.<br>
There are 2 types of wrong inputs:<br>
1. No input at all or String of chars, something that is not an Integer.
2. source/destination/both are not in the Graph.
   <br>[jump to Tutorial](#explanation-of-the-parts)<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### Add Edge:
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/8.png"> 

[Arduino](https://en.wikipedia.org/wiki/Arduino) (/ɑːrˈdwiːnoʊ/) - Once the user pressed the ShortestPath 3 things will happen:<br>
1. Popup window will open and ask the user to enter source Node and destination Node
2. The ShortestPath that our Algorithm chose will be marked in green.
3. The action log will write 2 things:
    1. Weight of the ShortestPath.
    2. String represents the ShortestPath in the right order.
       <br><br><br><br>


**Output:**  
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/88.jpg">
In case the user entered an invalid input, he will get a popup window about this problem and this will also be written in the log.<br>
There are 2 types of wrong inputs:<br>
1. No input at all or String of chars, something that is not an Integer.
2. source/destination/both are not in the Graph.
   <br>[jump to Tutorial](#explanation-of-the-parts)<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### Hide/Show Buttons:
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/9.jpg"> 

[Arduino](https://en.wikipedia.org/wiki/Arduino) (/ɑːrˈdwiːnoʊ/) - Once the user pressed the ShortestPath 3 things will happen:<br>
1. Popup window will open and ask the user to enter source Node and destination Node
2. The ShortestPath that our Algorithm chose will be marked in green.
3. The action log will write 2 things:
    1. Weight of the ShortestPath.
    2. String represents the ShortestPath in the right order.
       <br><br><br><br>


**Output:**  
<img align="left" width="75%" src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/99.png">
In case the user entered an invalid input, he will get a popup window about this problem and this will also be written in the log.<br>
There are 2 types of wrong inputs:<br>
1. No input at all or String of chars, something that is not an Integer.
2. source/destination/both are not in the Graph.
   <br>[jump to Tutorial](#explanation-of-the-parts)<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### Shortcuts:

<p align="center">
<img src="https://github.com/netanellevine/Weighted_Graph_Algorithms/blob/main/ReadMePics/10.png" width="900" height="700" border="10"/>
</p>


---

## How to use:

Let's begin with cloning the repository.
```
git clone https://github.com/netanellevine/Weighted_Graph_Algorithms.git && cd Weighted_Graph_Algorithms
```
Then we would like to run the jar to view the graph.  
For that we have few options:

**1.**  type/copy the blockquotes below as is.
- First, it loads an empty graph and will open an empty frame with all the GUI options.
- Second, now create a graph you desire or load one.

```
java -jar weighted-graphs.jar
```
**2.** type/copy the blockquotes below and add it to the end the line ***random***.
- Load a random generated graph (that we created already).
- The graph is loaded, play with all the features.
```
java -jar weighted-graphs.jar random
```
**3.** type/copy the blockquotes below and add an existing json_file in order to parse it into a graph.
- Load a graph with json file as a String.
- The graph is loaded, play with all the features.
```
java -jar weighted-graphs.jar <json-file>
```
In the data directory we have a few examples of some graph representation in json format.
for example: **"\Weighted_Graph_Algorithms\data\G1.json"**

---
## Sources:

- <a href="https://www.youtube.com/watch?v=CerlT7tTZfY&t">Djikstra's algorithm using a priority queue - Youtube</a>
- <a href="https://www.geeksforgeeks.org/connectivity-in-a-directed-graph/">Check if a graph is strongly connected</a>
