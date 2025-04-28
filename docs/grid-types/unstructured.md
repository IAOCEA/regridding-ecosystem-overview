# Unstructured Grids

```{figure} ./unstructured.png
---
width: 160pt
align: center
---
An example for a unstructured grid: a triangular mesh.
```

Unstructured grids don't follow any patterns, and thus often the only way to represent them is as a list of connected geometries (a mesh). An example for this are triangular irregular networks (TINs), which consist of variable sized triangles.

However, to accelerate certain operations, the topology of the grid – information about neighbouring geometries – is also constructed, allowing to deduplicate the vertex coordinates of the mesh.
