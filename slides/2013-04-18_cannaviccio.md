#Web Index
### Vertices trasformation and visualization
![ScreenShot](image.png)
- - -
## Problem description

### Vertices trasformation and visualization
The representation of cluster is stored in JSON file.
A cluster describe a set of contiguous cells not shared with other clusters.

The fields of JSON represent the description of the composition of a single cluster in term of vertices and simplicial cells.
In the JSON file there are informations about the position and the attributes for each vertices. There are also informations about the vertices that form a single cell.

The aim of this sub-task is apply the <b>transformations</b> for single vertices and the <b>visualization</b> on screen of the cluster.

## Problem solution

###Vertices trasformation
The JSON files that represent the clusters are organized in fields. 
- <b>Vertices</b> are represented by an array of arrays that show the coordinates of points (two for 2D model, three for 3D model).

```javascript 
              "vertices": [ [2, 2, 2] , 
                            [−2,−2, 2] , 
                            [−2.5, 2.8,−2.3] , 
                            [1.2,−1.7,0] 
              ];
```
- <b>Vertices attributes</b> are represented by an array of arrays that show the values of COLOR and BRIGHTNESS of single point.

```javascript
              "v_attributes": [ [0.5, 0.8, 1] ,
                                [28.44, 3, ] , 
                                [28.44, 3] , 
                                [3.4, 0] 
              ];             
```
- <b>Cells</b> are also rappresented by an array of arrays containing the indexes of the vertices for max order cells.
  (for a 3D model each cell is composed by 4 vertices)

```javascript
              "cells": [ [0, 1, 2, 3] ];
```

The function apply each attribute to the vertex in order.

###Visualization
![ScreenShot](image2.png)

After the transformation of vertices and the organization in cells, the cluster can be visualized. The input of the function is the cluster's ID and the output is the viewing of the model using plasm.js library.


