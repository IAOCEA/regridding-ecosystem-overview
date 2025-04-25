# Regridding Satellite and Model Data to DGGS Using the Pangeo Ecosystem

This Jupyter Book explores and evaluates different regridding libraries in the Pangeo ecosystem for mapping satellite and model data to Discrete Global Grid Systems (DGGS), with a focus on HEALPix and H3 grids.

## 📚 About the Book

Regridding (or resampling/remapping) is a crucial preprocessing step in geosciences to allow for data comparison across different spatial grids. In this project, we compare multiple Python-based libraries (such as **XESMF**, **Uxarray**, and **grid-weights**) for their ability to perform offline, area-based interpolation to and from DGGS.

This work is part of a collaboration between:

- **LOPS (Univ Brest–Ifremer–CNRS–IRD, France)**
- **CNES (Centre National d’Études Spatiales, France)**
- **Development Seed (USA)**

## 📂 Contents

The book is organized into the following chapters:

- Overview of regridding and grid types
- Regridding to H3 with XESMF
- Regridding to HEALPix with XESMF
- Using Uxarray for HEALPix
- Using grid-weights for HEALPix

Each chapter includes practical code examples and evaluation of the libraries’ capabilities with respect to DGGS compatibility, performance, and ease of use.

## 💡 Technologies Used

- Python & Jupyter
- XESMF
- Uxarray
- grid-weights
- Pangeo ecosystem tools

## 🚀 How to Use

To build and serve the Jupyter Book locally:

```bash
# Create and activate a virtual environment (optional but recommended)
python -m venv .venv
source .venv/bin/activate

# Install dependencies using PEP 621 (pyproject.toml)
pip install .

# Or if you're editing and want dev support
pip install -e .[dev]

# Build the book
jupyter-book build .
```

## How to cite

Magin, J., Delouis, J.-M., Zawadski, L., Petiton, J., Jones, M., and Odaka, T.: Regridding Satellite and Model Data to DGGS (HEALPix) Using the Pangeo Ecosystem, EGU General Assembly 2025, Vienna, Austria, 27 Apr–2 May 2025, EGU25-18285, DOI: [10.5194/egusphere-egu25-18285](https://doi.org/10.5194/egusphere-egu25-18285), 2025.
