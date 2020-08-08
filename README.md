# OSM
Open Street Map API for Python Matplotlib
By Ran N. Nof @ GSI, 2019  
  
## Installation



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

## Example of usage:
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
