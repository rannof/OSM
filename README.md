# OSM
Open Street Map API for Python Matplotlib
By Ran N. Nof @ GSI, 2019  

## Description
An OSM object is an API to Python's [matplotlib Axes class](https://matplotlib.org/3.1.1/api/axes_api.html).
Once an Axes is created, an OSM object with the Axes can be initialise.
With every draw of the axes, the tiles will be updated, showing map tiles (similar to google map or bing map).
See [example](#Example) below.

## Installation

Clone from git
```bash
git clone https://github.com/rannof/OSM.git
```
Install requirements
- matplotlib
- httplib2
```
pip install -r requirements.txt 
```
or
```
conda install -c conda-forge --file requirements.txt
```
Or use python virtual environment:
1. Go into the OSM folder
```bash
cd OSM
```
2. Set a virtual environment in .venv folder
```bash
python3 -m venv .venv
```
3. Install requirements
```bash
pip install -r requirements.txt
```

## Configuration
### Map Tiles
You may change the map tiles by setting TILEURL parameter.
Checkout: 
https://leaflet-extras.github.io/leaflet-providers/preview/
for different tiles.
Please note you might need to adgust the TILEPAT parameter as well.
### Saving tiles locally
Create a folder name tiles will allow saving the tiles locally.
Saving the tiles will allow speeding up plots on your next plot or will allow  working offline. Please note only tiles that are used will be saved locally and plotting different area or zoom level will require online connection.
Choosing a different tile url will require deleting (or renaming) the tiles folder to allow new data to be downloaded.

## Example
```python
import matplotlib.pyplot as plt
from osm import OSM

ax = plt.gca()
ax.osm = OSM(ax)
ax.set_aspect('equal')
ax.set_xlim(34, 36)
ax.set_ylim(29.5, 34)
ax.osm.draw()
```
![EXAMPLEMAP](https://github.com/rannof/OSM/blob/master/example.png)
