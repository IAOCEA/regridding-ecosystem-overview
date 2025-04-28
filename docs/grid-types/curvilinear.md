# Curvilinear Grids

```{figure} ./curvilinear.png
---
width: 160pt
align: center
---
A curvilinear grid.
```

Curvilinear grids look just like rectilinear grids, except that the arrangement of points does not follow straight lines anymore. This is often the effect of expressing the sampling points in a different projection.

Since the grid points don't stay on the coordinate axes anymore, we need to store the coordinates as two 2D arrays.
