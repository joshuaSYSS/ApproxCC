# Approximate Connected Component
Here, I provide the implementation for a randomized algorithm approximating the numbers of connected components in a graph.

## Source
This algorithm is based on Lecture 5: Bounded Degree Graph Algorithms, CSCI 1951-W Sublinear Algorithms for Big Data

## How to use it?
Please keep the code where I highlighted in comments, while other codes can be modified to your own needs.<br>
To get the approximated connected component value, simply provide necessary parameters, and call the function `approxCC`.

## Approximation Bounds
The number of connected component is within `εn` with probability `1 - δ`.

## Time Complexity
O((d / ε<sup>2</sup>) * log(d / ε))

## Idea
Let n<sub>u</sub> be the number of nodes in the connected component where the node u is located.<br>
The number of connected component = sum(1 / n<sub>u</sub>) for all node u.<br><br>
Prove:<br>
For a component C, (sum(1 / n<sub>u</sub>) for all node u ∈ C) = 1.<br><br>
Therefore, we can use a subsample to approximate the number of connected components.<br><br>
Then, since the bottleneck is at breadth-first-search, we simply limit the depth for searching without affecting the accuracy.<br><br>

Code is implemented on 23rd June, 2025, by [Joshua CHOI](https://joshuasyss.github.io/).
