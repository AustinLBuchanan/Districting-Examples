# Districting-Examples
Examples on how to generate political districting plans. All codes are written using Python, with NetworkX used for handling graphs, Gurobi used as MIP solver, and GeoPandas used to draw maps. Used in an undergraduate Operations Research course at Oklahoma State University (IEM 4013).

The MIP models are summarized in [Two_districting_models.pdf](https://github.com/AustinLBuchanan/Districting-Examples/blob/main/Two_districting_models.pdf).

The Oklahoma county graph is duplicated from [Daryl DeFord's page](http://people.csail.mit.edu/ddeford/dual_graphs), which has graphs for other states and other levels (e.g., census tracts, census blocks, etc). These files contain [other data](https://people.csail.mit.edu/ddeford/data_cols.html) (e.g., demographic data) besides the graph itself. The Oklahoma shapefiles are duplicated from [Eugene Lykhovyd's page](https://lykhovyd.com/files/public/districting), which has other states too.

[D1-Min-Deviation.ipynb](https://github.com/AustinLBuchanan/Districting-Examples/blob/main/D1-Min-Deviation.ipynb) shows how to:
  - read county populations from a text file
  - build a MIP model in Gurobi to minimize population deviation
  
[D2-Min-Cut-Edges.ipynb](https://github.com/AustinLBuchanan/Districting-Examples/blob/main/D2-Min-Cut-Edges.ipynb) shows how to:
  - read a graph from a file (using NetworkX)
  - build a MIP model in Gurobi to minimize cut edges
  - check if the resulting districts are connected (using NetworkX)
  
[D3-Min-Cut-Edges-with-GeoPandas.ipynb](https://github.com/AustinLBuchanan/Districting-Examples/blob/main/D3-Min-Cut-Edges-with-GeoPandas.ipynb) shows how to:
  - read a graph from a .json file (using the GerryChain reader)
  - print the names of the counties and their populations
  - build a MIP model in Gurobi to minimize cut edges
  - read a shapefile with GeoPandas
  - draw the districting plan on a map with GeoPandas
  
[D4-Min-Cut-Edges-with-GeoPandas-and-Contiguity.ipynb](https://github.com/AustinLBuchanan/Districting-Examples/blob/main/D4-Min-Cut-Edges-with-GeoPandas-and-Contiguity.ipynb) shows how to:
  - read a graph from a .json file (using the GerryChain reader)
  - print the names of the counties and their populations
  - build a MIP model in Gurobi to minimize cut edges
  - add the contiguity constraints of [Hojny et al. (MPC, 2021)](https://link.springer.com/article/10.1007/s12532-020-00186-3)
  - read a shapefile with GeoPandas
  - draw the districting plan on a map with GeoPandas

[D5-Min-Perimeter-with-GeoPandas-and-Contiguity.ipynb](https://github.com/AustinLBuchanan/Districting-Examples/blob/main/D5-Min-Perimeter-with-GeoPandas-and-Contiguity.ipynb) shows how to:
  - read a graph from a .json file (using the GerryChain reader)
  - print the names of the counties and their populations
  - build a MIP model in Gurobi to minimize total perimeter length of the districts
  - add the contiguity constraints of [Hojny et al. (MPC, 2021)](https://link.springer.com/article/10.1007/s12532-020-00186-3)
  - read a shapefile with GeoPandas
  - draw the districting plan on a map with GeoPandas
  
