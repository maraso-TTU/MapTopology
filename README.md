# Map Topology
This repository helps you make a graph from historical OSM files and extract topological feature out of it . 

**How to use** <br>
You need to **a) install requirements** and **b) download your desired map and feed it to the code**.<br>

**a) Requirements**<br>
Download and extract this repo on your machine (or clone this repo).<br>
To install the requirements you need to use `pip install requirements.txt` in your teminal.<br>


**B) Data**<br>
You need to extract the zip file inside the maps folder which includes historical road network of Estonia from January 2020.



## You can use this code to extract topological features of all the OSM data across the world.
You can download any OSM file and put it in the maps folder. <br> 
We used this url for Estonia: https://download.geofabrik.de/europe/estonia.html.  If you click on `raw directory index` in this page you see historical maps of Estonia since January 2014.<br>
You can find list of continents at https://download.geofabrik.de/ and then by click on the continent you can select the country you want.
Then you can download the `.shp.zip` file of the desired year. Extract it on your machine. Then you see lots of files inside this folder. You need to select all files their name starts with `gis_osm_roads_free` and put it inside a new folder inside the `maps` folder of this repo.<br>
Then you can use the jupyter notebook.<br>
**hint:** The road network of a country is too huge. In the jupyter notebook you can define a bonding box to limit it to the city you want to extract features from that.
