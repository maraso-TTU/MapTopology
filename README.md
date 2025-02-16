# Map Topology
This repository helps you make a graph from historical OSM files and extract topological feature out of it . 

**How to use** <br>
You need to **a) install requirements**, **b) download your desired map and feed it to the code** and **c) run the Jupyter Notebbok**.<br>

**a) Requirements**<br>
1- Download and extract this repo on your machine (or clone this repo).<br>
2- To install the requirements you need to use `pip install requirements.txt` in your teminal.<br>
3- To install lib_orca you can clone it from [PyORCA](https://github.com/qema/orca-py), put it in the root folder of MapTopology project and rename its folder to  'lib_orca'. Then go to 'lib_orca' folder  in your terminal and then run 'make'. This will make ORbit Counting Algorithm Python wrapper installed in your machine.

**B) Data**<br>
You need to extract the zip file inside the maps folder which includes historical road network of Estonia from January 2020.

**C) Run the Notebook**<br>
To run the notebook, you need to run `jupyter notebook` in your terminal. Then in your browser double click on  [`extractTopology.ipynb`](https://github.com/maraso-TTU/MapTopology/blob/main/extractTopology.ipynb) and run the notebook with your files.

<br>

To make working with the output easier we made a .shp file at the end. In this way you can visulize the graphlet decomposition of all nodes of the map using different GIS tools:
![visualization](https://github.com/maraso-TTU/MapTopology/blob/main/output_visualization.png)



## You can use this code to extract topological features of all the OSM data across the world.
You can download any OSM file and put it in the maps folder. <br> 
We used this url for Estonia: https://download.geofabrik.de/europe/estonia.html.  If you click on `raw directory index` in this page you see historical maps of Estonia since January 2014.<br>
You can find list of continents at https://download.geofabrik.de/ and then by click on the continent you can select the country you want.
Then you can download the `.shp.zip` file of the desired year. Extract it on your machine. Then you see lots of files inside this folder. You need to select all files their name starts with `gis_osm_roads_free` and put it inside a new folder inside the `maps` folder of this repo.<br>
Then you can use the jupyter notebook.<br>
**hint:** The road network of a country is too huge. In the jupyter notebook you can define a bonding box to limit it to the city you want to extract features from that.
