# Regridding Satellite and Model Data to DGGS Using the Pangeo Ecosystem

Welcome! This Jupyter Book presents a practical evaluation of different Python-based regridding tools for mapping geospatial datasets to **Discrete Global Grid Systems (DGGS)**, particularly **HEALPix** and **H3**.

## Objectives

- Understand the fundamentals of regridding and its role in comparing gridded data.
- Explore offline, area-based regridding techniques.
- Compare regridding tools available in the Pangeo ecosystem:
  - `xesmf`
  - `uxarray`
  - `grid-weights`
- Evaluate their compatibility with DGGS such as HEALPix and H3.

## Why DGGS?

DGGS provide a hierarchical, equal-area tiling of the globe and are increasingly used in Earth observation and climate modeling. HEALPix, originally developed for astrophysics, offers excellent characteristics for global-scale geoscientific applications.

## Structure of the Book

This book is divided into the following sections:

```{tableofcontents}

```

## Citation

This work is developed by researchers at LOPS, CNES, and Development Seed {cite:p}`magin2025`.

## References

```{bibliography}
:style: unsrtalpha
```
