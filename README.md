# Map Topology
### This repository contains graphlet decomposition of city of Tallinn, Estonia based on OpenStreetMap (OSM) data of January 2020<br>
#### This repository also helps you create a graphlet decomposition from any other OSM data across the world.

## Quick Start
If you only want to use the extracted graphlet decomposition from Tallinn's historical map of 2020, download all the dataset files in the [output folder](https://github.com/maraso-TTU/MapTopology/blob/main/output/).

```
.
├── graphlet.csv
├── graphlet.cpg
├── graphlet.dbf
├── graphlet.prj
├── graphlet.shp
└── graphlet.shx
```

## Custom Usage
If you want to use the code with Estonia data, please follow the [How to Use](#how-to-use) section.

If you want to extract graphlets for another region on earth, see [Providing your own data](#providing-your-own-data) at the end of this README.

## How to use
You need to **A) install requirements**, **B) download your desired map and put it in the maps folder**, and **C) run the Jupyter Notebook**.

### A) Requirements
1. Download and extract this repo on your machine (or clone this repo).
2. To install Python requirements, use `pip install -r requirements.txt` in your terminal. The code is developed and tested with Python 3.11
3. To install lib_orca, clone it from [PyORCA](https://github.com/qema/orca-py), put it in the root folder of the MapTopology project, and rename its folder to 'lib_orca'. Then go to the 'lib_orca' folder in your terminal and run 'make'. This will install the Python ORbit Counting Algorithm wrapper on your machine.

### B) Data
The code will use the Shapefile in maps folder which includes the historical road network of Estonia from January 2020. If you want to use the code with your own map, please follow [Providing your own data](#providing-your-own-data) section.

### C) Run the Notebook
To run the notebook, use `jupyter notebook` in your terminal. Then in your browser, double click on [`extractTopology.ipynb`](https://github.com/maraso-TTU/MapTopology/blob/main/extractTopology.ipynb) and run the notebook with your files.

To make working with the output easier, we create a .shp file at the end. This way you can visualize the graphlet decomposition of all nodes of the map using different GIS tools:
![dataset visualization](https://github.com/maraso-TTU/MapTopology/blob/main/output_visualization.png)

## Providing your own data
You can download any OSM file (generally any Shapefile which includes road network) and put it in the maps folder and run the code to extract graphlet out of it.


You can find a list of continents at https://download.geofabrik.de/, and then by clicking on the continent, you can select the country you want. For example, We reached to this URL for Estonia: https://download.geofabrik.de/europe/estonia.html. On this page, if you click on `raw directory index`, you'll see historical maps of Estonia since January 2014.


Then you can download the `.shp.zip` file of the desired year. Extract it on your machine. You'll see lots of files inside this folder. Select all files whose names start with `gis_osm_roads_free` and put them inside a new folder inside the `maps` folder of this repo.

Then you can use the Jupyter notebook.

**Hint:** The road network of a country is too huge. In the Jupyter notebook, you can define a bounding box to limit it to the city you want to extract features from.
