# MiniFlow
The goal of this project is to demystify two concepts at the heart of neural networks - backpropagation and differentiable graphs.

Backpropagation is the process by which neural networks update the weights of the network over time. (You may have seen it in this video earlier.)

Differentiable graphs are graphs where the nodes are differentiable functions. 

## What is a Neural Network

A neural network is a graph of mathematical functions such as linear combinations and activation functions. The graph consists of nodes, and edges.

Nodes in each layer (except for nodes in the input layer) perform mathematical functions using inputs from nodes in the previous layers. For example, a node could represent f(x, y) = x + yf(x,y)=x+y, where xx and yy are input values from nodes in the previous layer.

Similarly, each node creates an output value which may be passed to nodes in the next layer. The output value from the output layer does not get passed to a future layer (because it is the final layer).

Layers between the input layer and the output layer are called hidden layers.

The edges in the graph describe the connections between the nodes, along which the values flow from one layer to the next. These edges can also apply operations to the values that flow along them, such as multiplying by weights and adding biases. MiniFlow won't use a separate class for edges - instead, its nodes will perform both their own calculations and those of their input edges. This will be more clear as you go through these lessons.

## Forward Propagation

By propagating values from the first layer (the input layer) through all the mathematical functions represented by each node, the network outputs a value. This process is called a forward pass.

## Graphs

The nodes and edges create a graph structure. 

There are generally two steps to create neural networks:

* Define the graph of nodes and edges.
* Propagate values through the graph.

**MiniFlow** works the same way. You'll define the nodes and edges of your network with one method and then propagate values through the graph with another method. 
