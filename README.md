# Reduced_EL_EQE

Jupyter notebook for analyzing reduced electroluminescence (EL) and external quantum efficiency (EQE) data in organic solar cells.

## Files

| File | Description |
|------|-------------|
| `Reduced_EL_EQE.ipynb` | Main notebook with analysis functions |

## Main Functions

| Function | Purpose |
|----------|---------|
| `planck_law(wavelength, temperature)` | Calculate black body spectrum using Planck's law |
| `photon_flux(wavelength, power)` | Convert power to photon flux (s⁻¹ nm⁻¹) |
| `Reduced_EL(wavelength, power)` | Calculate reduced EL spectrum (in eV units) |
| `Reduced_EQE(Energy, EQE)` | Calculate reduced EQE (EQE/Energy) |
| `normalize_to_local_max(x, y, energy_value, window)` | Normalize spectrum to local maximum |
| `find_intersection(el_x, el_y, eqe_x, eqe_y, region)` | Find intersection point between EL and EQE curves |

## What It Does

- Converts EL and EQE spectra to reduced representations
- Normalizes spectra to local maxima
- Finds intersection points between reduced EL and EQE curves
- Used for determining charge transfer state energies in organic photovoltaics

## Dependencies

- numpy
- matplotlib
- pandas
- scipy

## Author

mzjswjz
