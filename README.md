# Infection

This notebook creates a graph using the networkx library.  The nodes of the graph represent people and the edges represent social connections.  Each node starts with a variety of attributes eg contagious, time since infection, # of people infected.  Then for a fixed number of time steps (not necessarily days) people interact with their connections.  Contagious people can pass on the disease when they interact with those connections.  At the end of the time step attributes are updated as needed. Various metrics are also stored at the end of each time step.


The first thing to check is whether the results of this simulation match with other models.


The results of a standard model (left) and my model (right) look similar.  A second simple sanity check is to make sure that the infection spreads exponentially early on in the model.  For this we can look at a log plot of the cases compared with an exponential plot.  

<img src="https://github.com/mkspillane/Infection/blob/master/images/Log_Growth.png" width="300" height="200">

This is a semi-log plot so exponential growth becomes a straight line.  The blue is the model and the yellow is an exponential function.
 