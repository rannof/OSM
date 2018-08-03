# OSM
Open Street Map API for Python Matplotlib
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
