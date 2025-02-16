# Map Topology
This repository helps you make a graphlet decomposition from OSM data.

If you want to only use the final results for extracted graphlets from Estonia historical map of 2020, download the zip file in from output folder.<br>
If you want to use the code with your desired map, Please follow the how to use section.<br>
There is a [section](#you-can-use-this-code-to-extract-topological-features-of-all-osm-data-across-the-world)
 at the end of this readme file helping you on how to download historical data from OSM.

## How to use
You need to **a) install requirements**, **b) download your desired map and put it in the maps folder**, and **c) run the Jupyter Notebook**.

### a) Requirements
1. Download and extract this repo on your machine (or clone this repo).
2. To install the requirements, use `pip install -r requirements.txt` in your terminal.
3. To install lib_orca, clone it from [PyORCA](https://github.com/qema/orca-py), put it in the root folder of the MapTopology project, and rename its folder to 'lib_orca'. Then go to the 'lib_orca' folder in your terminal and run 'make'. This will install the Python ORbit Counting Algorithm wrapper on your machine.

### b) Data
Extract the zip file inside the maps folder, which includes the historical road network of Estonia from January 2020.

### c) Run the Notebook
To run the notebook, use `jupyter notebook` in your terminal. Then in your browser, double click on [`extractTopology.ipynb`](https://github.com/maraso-TTU/MapTopology/blob/main/extractTopology.ipynb) and run the notebook with your files.

To make working with the output easier, we create a .shp file at the end. This way you can visualize the graphlet decomposition of all nodes of the map using different GIS tools:
![visualization](https://github.com/maraso-TTU/MapTopology/blob/main/output_visualization.png)

## You can use this code to extract topological features of all OSM data across the world
You can download any OSM file and put it in the maps folder.

We used this URL for Estonia: https://download.geofabrik.de/europe/estonia.html. If you click on `raw directory index` on this page, you'll see historical maps of Estonia since January 2014.

You can find a list of continents at https://download.geofabrik.de/, and then by clicking on the continent, you can select the country you want.

Then you can download the `.shp.zip` file of the desired year. Extract it on your machine. You'll see lots of files inside this folder. Select all files whose names start with `gis_osm_roads_free` and put them inside a new folder inside the `maps` folder of this repo.

Then you can use the Jupyter notebook.

**Hint:** The road network of a country is too huge. In the Jupyter notebook, you can define a bounding box to limit it to the city you want to extract features from.
