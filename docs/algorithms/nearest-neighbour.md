# Nearest Neighbour

```{figure} ./nearest-neighbour.png
---
width: 160pt
align: center
---
Schematic of the algorithm.
```

The nearest neighbour interpolation is the simplest algorithm imaginable: find the source cell closest to the target cell, and assign its weight to the target cell. It is one of the few algorithms that works for both categorical and continuous data.

The areas of influence of the source cells form Thiessen polygons / a Delaunay diagram.
