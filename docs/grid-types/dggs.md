# Discrete Global Grid Systems

```{image} ./dggs.png
:width: 160pt
:align: center
```

Projection-based grids have increasingly distorted grid cells the further away from the projection center / line they are.

Discrete global grid systems (DGGS) aim to minimize the distortion by approximating the surface of the earth (usually a sphere) by evenly subdividing it into planar faces. These faces are then recursively subdivided to form a hierarchy / tree of cells.

There is (in general) no way to arrange these cells into two dimensions that encode the topology, and thus in-memory we have to represent them as a 1D array (a list of cells).
