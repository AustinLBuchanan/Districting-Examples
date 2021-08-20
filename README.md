# Districting-Examples
Examples on how to generate political districting plans. All codes are written using Python, with NetworkX used for handling graphs, Gurobi used as MIP solver, and GeoPandas used to draw maps. Used in an undergraduate Operations Research course at Oklahoma State University (IEM 4013).

# The MIPs
The MIP models are summarized in [Two_districting_models.pdf](https://github.com/AustinLBuchanan/Districting-Examples/blob/main/Two_districting_models.pdf).

# The Data
The Oklahoma county graph is duplicated from [Daryl DeFord's page](http://people.csail.mit.edu/ddeford/dual_graphs), which has graphs for other states and other levels (e.g., census tracts, census blocks, etc). These files contain [other data](https://people.csail.mit.edu/ddeford/data_cols.html) (e.g., demographic data) besides the graph itself. The Oklahoma shapefiles are duplicated from [Eugene Lykhovyd's page](https://lykhovyd.com/files/public/districting), which has other states too.

It is possible to download the files individually, but the naming conventions are different. Daryl uses [FIPS codes](https://www.nrcs.usda.gov/wps/portal/nrcs/detail/?cid=nrcs143_013696) while Eugene uses postal codes. So, Daryl's Oklahoma county file is called [COUNTY_40.json](http://people.csail.mit.edu/ddeford/COUNTY/40.html) while Eugene's are called [OK_counties.shp](https://lykhovyd.com/files/public/districting/OK/counties/maps/) (shx,prj,...). 

A clean way to get both datasets with intuitive names (e.g., OK_county.json and OK_county.shp) is to run my [data downloaders](https://github.com/AustinLBuchanan/data-downloader).

These codes will download the data for all 50 states and store them in the directory:
C://districting-data-2010//

# The Codes
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

[D6-Min-Moment-of-Inertia.ipynb](https://github.com/AustinLBuchanan/Districting-Examples/blob/main/D6-Min-Moment-of-Inertia.ipynb) shows how to:
  - read a graph from a .json file (using the GerryChain reader)
  - print the names of the counties, their populations, and their lat-long coordinates
  - build a MIP model in Gurobi to minimize moment of inertia
  - read a shapefile with GeoPandas
  - draw the districting plan on a map with GeoPandas
  
[D7-Min-Moment-of-Inertia-with-Contiguity.ipynb](https://github.com/AustinLBuchanan/Districting-Examples/blob/main/D7-Min-Moment-of-Inertia-with-Contiguity.ipynb) shows how to:
  - read a graph from a .json file (using the GerryChain reader)
  - print the names of the counties, their populations, and their lat-long coordinates
  - build a MIP model in Gurobi to minimize moment of inertia
  - add the contiguity constraints of Shirabe ([2005](https://onlinelibrary.wiley.com/doi/full/10.1111/j.1538-4632.2005.00605.x) and [2009](https://journals.sagepub.com/doi/abs/10.1068/b34104)). See [Oehrlein and Haunert, 2017](http://www.josis.org/index.php/josis/article/viewArticle/379) and [Validi et al., 2020](http://www.optimization-online.org/DB_HTML/2020/01/7582.html) for more details.
  - read a shapefile with GeoPandas
  - draw the districting plan on a map with GeoPandas

# Past Student Projects

Here are some examples of student projects from the Spring 2021 semester of IEM 4013:
  - [Idaho](https://github.com/KyleHumphreys/IEM-4013-Idaho-Districting)
  - [Nebraska](https://github.com/Jay-dnn/4013-Final-Report)
  - [Iowa](https://github.com/Jared-Johnson294/Redisctricing-Iowa)
  - [Alabama](https://github.com/livey2021/LEWVEYZAL-IEM4013-Group-Project)
  - [New Mexico](https://github.com/nathan-whitehead/New-Mexico-Redistricting-Plan)
  - [Kansas](https://github.com/William-Jackson-Ricky/Kansas-Redistricting-for-Dr.-Buchanan)
  
