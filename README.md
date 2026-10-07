# Analysis Repository

This repository contains the data processing and analysis workflows used for the study of near-inertial and internal waves around the Kermadec Ridge.

## Repository Structure

### `adcp_proc.ipynb`
Processes the raw moored ADCP observations and produces time-depth velocity datasets used in all subsequent analyses.

**Input:**
- Raw ADCP data

**Output:**
- Time-depth velocity datasets

---

### `Analysis_chapter1.ipynb`
Main analysis notebook containing the majority of calculations, visualisations, and figures used in Paper 1.

Examples include:
- Data map
- Current velocity analysis
- PSD plots
- Pycnocline estimations from WOA
- Near-inertial and semidiurnal current calculations
- Coherent and incoherent tidal analysis 
- Figure generation

**Input:**
- Processed ADCP datasets from `adcp_proc.ipynb`

---

### `critical_slope.ipynb`
Calculates the bathymetric criticality parameter and related topographic diagnostics.

**Input:**
- Bathymetry data
- Stratification from CTD casts

**Output:**
- Critical slope estimates
- Criticality maps and figures

---

### `slab_model.ipynb`
Implements the slab model used to investigate wind-driven near-inertial currents and compare model results with observations.

**Input:**
- Wind forcing data from era5
- MLD depth estimates from WOA
- Processed ADCP observations

**Output:**
- Slab model simulations
- Observation-model comparisons

---

## Workflow

The notebooks should generally be run in the following order:

1. `adcp_proc.ipynb`
2. `Analysis_chapter1.ipynb`
3. `critical_slope.ipynb`
4. `slab_model.ipynb`

## Data Requirements

The analysis requires:
- ADCP observations
- Bathymetry data (GEBCO) and MBES 
- Wind reanalysis products from ERA5
- Hydrographic climatology (WOA23)
- CTD casts

Data files are not included in this repository.

## Author

Renske Koets  
PhD Candidate, University of Auckland
