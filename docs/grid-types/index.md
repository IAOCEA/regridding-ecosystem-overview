# Geospatial grids

In the geosciences, a lot of data describes continuous surfaces and is stored in a discretized form (as a lot of real numbers that contain the evaluation at certain sampling points).

In the following, we'll call the choice of where to evaluate these surfaces a "grid", and only look at horizontal ("spatial") grids.

## Grid Types

Various kinds grids exist, but can be broadly divided into 4 categories:

- rectilinear (and regular) grids
- curvilinear grids
- discrete global grid systems (DGGS)
- unstructured grids

### Rectilinear Grids

Rectilinear grids arrange the sampling points along lines along the coordinate axes of a projection, forming rectangular cells. This allows us to describe the grid using 1D coordinates.

If the distance between the points is constant along both coordinate axes, the grid is called "regular".

<!-- Add a graphic describing the grid -->

### Curvilinear Grids

Curvilinear grids look just like rectilinear grids, except that the arrangement of points does not follow straight lines anymore. This is often the effect of expressing the sampling points in a different projection.

Since the grid points don't stay on the coordinate axes anymore, we need to store the coordinates as two 2D arrays.

<!-- Add a graphic describing the grid -->
