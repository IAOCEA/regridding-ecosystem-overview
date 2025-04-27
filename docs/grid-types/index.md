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

The simplest and by far most commonly used grid is a regular longitude / latitude grid, i.e. a regular grid following the equirectangular projection.

<!-- Add a graphic describing the grid -->

### Curvilinear Grids

Curvilinear grids look just like rectilinear grids, except that the arrangement of points does not follow straight lines anymore. This is often the effect of expressing the sampling points in a different projection.

Since the grid points don't stay on the coordinate axes anymore, we need to store the coordinates as two 2D arrays.

<!-- Add a graphic describing the grid -->

### Discrete Global Grid Systems

Projection-based grids have increasingly distorted grid cells the further away from the projection center / line they are.

Discrete global grid systems (DGGS) aim to minimize the distortion by approximating the surface of the earth (usually a sphere) by evenly subdividing it into planar faces. These faces are then recursively subdivided to form a hierarchy / tree of cells.

There is (in general) no way to arrange these faces into a two-dimensional grid, and thus in-memory we have to represent these as a 1D array (a list of cells).

### Unstructured Grids

Unstructured grids don't follow any patterns, and thus often the only way to represent them is as a list of connected geometries (a mesh). An example for this are triangular irregular networks (TINs), which consist of variable sized triangles.

However, to accelerate certain operations, the topology of the grid – information about neighbouring geometries – is also constructed, allowing to deduplicate the vertex coordinates of the mesh.
