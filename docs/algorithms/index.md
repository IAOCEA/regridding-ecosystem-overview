# Interpolation algorithms

There are a lot of different ways to interpolate from one grid to another, with lots of different ways to categorize the algorithms.

The ones we'll look at here are:

- offline vs online
- point-based vs area-based

## Offline and Online

The difference between these two categories is that offline algorithms only consider the geometry of source and target grids, and thus are independent of the actual data. This allows expressing the interpolation operation as a weighted sum, where the weights can be pre-computed and cached to disk. Additionally, these weights can be reused between different variables or for multi-dimensional data, making the interpolation operation very efficient.

The general workflow is:

1. for each target cell, find the source cells to aggregate
2. compute the weights
3. apply the weights

Examples are:

- nearest-neighbour
- bilinear
- inverse distance weighting
- area-weighted
- binning

Online regridding, by contrast, works by determining approximation functions for the source data which are evaluated at the target cells. The first step (the construction of approximation functions) can be seen as a transformation of the input data.

Examples are:

- Splines
- Kriging
- Radial Basis Functions

## Point-based vs area-based

The algorithms can also be categorized based on whether they see the grid elements as points or areas. For the former, the data on that grid would be seen as the values of the underlying function sampled at that point, while for the latter the data is interpreted as an integration over the area.

Examples for point-based algorithms:

- nearest-neighbour
- bilinear
- inverse distance weighting
- Splines

Examples for area-based algorithms:

- area-weighted (first order conservative)
- binning
