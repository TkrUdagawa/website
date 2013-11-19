Graph
===================

In this sample program, we will introduce how to do graph mining by using jubagraph function from Jubatus Client.

By using graph mining function, we can find the center node or the shortest path in a graph structure. This is useful for the analysis of social community, network structure, and etc.

----------------------------------
Abstract of sample program
----------------------------------

In this sample, we will describe the Jubagraph usage through a program of the shortest path detection for train routes. 

At first, we will create the train route graph by using the CreateGraph() function. In this example, we will build the graph with the train route of Yamanote-line and Chuo-line, in Tokyo, Japan.

After the graph is built, we can find the shortest path between any 2 stations by putting the 2 Station IDs into the SearchRoute() function.

For example, to find the route between "Shinagawa-Station" on Yamanote-line and "Ochanomizu-Station" on Chuo-line, basically we can get 2 patterns. One is transfer at "Shinjuku-Station" for Chuo-line (clockwise), another one is transfer at "Tokyo-Station" for Chuo-line (counterclockwise). By using this program, the route of the least stations to pass is returned. In other words, only the route via "Tokyo-Station" will be returned.

--------------------------------
Processing flow 
--------------------------------

Main flow of using Jubatus Client

* CreateGraph

 1. Connection settings to Jubatus Server

  Set the HOST and RPC port of Jubatus Server

 2. Register the pre-set query

  Register the queries which are used for the shortest path calculation.

 3. Create graph

  Get the stations information on Yamanote-line and Chuo-line, and create a route graph.

 4. Set Station ID

  Display the stations in the route-graph by their Station ID.


* SearchRoute

 1. Connection settings to Jubatus Server

  Set the HOST and RPC port of Jubatus Server

 2. Prepare the query

  Prepare the query for the shortest path calculation.

 3. Get the shortest path

  Calculate the shortest path between the two stations assigned in the query at step. 2.

 4. Display the result

  Display the result in step. 3.

--------------------------------
Sample Programs
--------------------------------

.. toctree::
   :maxdepth: 2

   graph_python
   graph_ruby
   graph_java
