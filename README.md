# Infection

This notebook creates a graph using the networkx library.  The nodes of the graph represent people and the edges represent social connections.  Each node starts with a variety of attributes eg contagious, time since infection, # of people infected.  Then for a fixed number of time steps (not necessarily days) people interact with their connections.  Contagious people can pass on the disease when they interact with those connections.  At the end of the time step attributes are updated as needed. Various metrics are also stored at the end of each time step.


The first thing to check is whether the results of this simulation match with other models.


![Image1](https://upload.wikimedia.org/wikipedia/commons/3/32/Sirsys-p9.png)
Standard SIR model using differential equations.

![Image2](https://github.com/mkspillane/Infection/blob/master/images/Normal.png)
Results from a run of this model.
