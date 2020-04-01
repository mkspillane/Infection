# Infection

This notebook creates a graph using the networkx library.  The nodes of the graph represent people and the edges represent social connections.  Each node starts with a variety of attributes eg contagious, time since infection, # of people infected.  Then for a fixed number of time steps (not necessarily days) people interact with their connections.  Contagious people can pass on the disease when they interact with those connections.  At the end of the time step attributes are updated as needed. Various metrics are also stored at the end of each time step.


The first thing to check is whether the results of this simulation match with other models.

<img src="https://upload.wikimedia.org/wikipedia/commons/3/32/Sirsys-p9.png" width="300" height="200"> <img src="https://github.com/mkspillane/Infection/blob/master/images/Normal.png" width="300" height="200">

The results of a standard model (left) and my model (right) look similar.  

A second simple sanity check is to make sure that the infection spreads exponentially early on in the model.  For this we can look at a log plot of the cases compared with an exponential plot.  

<img src="https://github.com/mkspillane/Infection/blob/master/images/Log_Growth.png" width="300" height="200">

This is a semi-log plot so exponential growth becomes a straight line.  The blue is the model and the yellow is an exponential function.

With those sanity checks perform we can test out other features.  For example, we can see how social distancing flattens the curve. To test this we run two identical simulations. In the first nodes (people) continue to behave as normal ignoring the infection.  In the second after 1% of the population has become infected nodes interact with fewer nodes each time step. 

<img src="https://github.com/mkspillane/Infection/blob/master/images/social_distancing.png" width="450" height="200">
The dashed lines represent the same variables with moderate social distancing implemented.

Another option is quarantining symptomatic people.  Here we run 3 simulations where people with mild symptoms are progressively more likely to self-quarintine.  
<img src="https://github.com/mkspillane/Infection/blob/master/images/symp_quar.png" width="450" height="200">

We can see that this is much less successful that having the whole population decrease interactions.

Another feature that we can play with is the infection rate.  For some infections the rate varies with the external temperature.  This can lead to a resurgence in the infection as the weather starts to cool again.

<img src="https://github.com/mkspillane/Infection/blob/master/images/Resurgence.png" width="300" height="200">


