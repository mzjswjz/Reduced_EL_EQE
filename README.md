# Reduced_EL_EQE

This repository contains tools for analyzing reduced electroluminescence (EL) and external quantum efficiency (EQE) spectra, commonly used in the study of organic and perovskite solar cells.

## What is EL EQE?

**Electroluminescence (EL)** is light emission from a device when an electric current passes through it. In solar cells, EL provides information about:
- Radiative recombination processes
- Quasi-Fermi level splitting
- Device quality and defects

**External Quantum Efficiency (EQE)** measures the fraction of incident photons that generate electron-hole pairs and are collected as current.

## What Does "Reduced" Mean?

The "reduced" quantities normalize the spectra to remove the photon energy dependence, revealing the underlying physics:

### Reduced EL

The reduced EL spectrum is defined as:

$$\phi_{EL}^{reduced}(E) = \frac{\phi_{EL}(E)}{E^3}$$

Where:
- $\phi_{EL}(E)$ = measured EL intensity at photon energy $E$
- $E$ = photon energy (eV)
- The $E^3$ factor accounts for the photon density of states

### Reduced EQE

The reduced EQE is defined as:

$$EQE_{reduced}(E) = \frac{EQE(E)}{E}$$

Where:
- $EQE(E)$ = measured external quantum efficiency at photon energy $E$

## Analysis Methods

This tool performs:

1. **Data loading and preprocessing**:
   - Import EL spectra (wavelength vs. intensity)
   - Import EQE spectra (wavelength vs. efficiency)
   - Convert between wavelength and energy scales

2. **Reduction calculations**:
   - Apply the $E^3$ reduction to EL data
   - Apply the $E$ reduction to EQE data
   - Normalize spectra to local maxima for comparison

3. **Intersection analysis**:
   - Find the intersection point between reduced EL and reduced EQE
   - This intersection relates to the open-circuit voltage and radiative efficiency

4. **Visualization**:
   - Plot original and reduced spectra
   - Overlay EL and EQE for comparison
   - Mark intersection points

## Key Equations

**Photon energy conversion:**
$$E = \frac{hc}{\lambda} = \frac{1240}{\lambda \text{ (nm)}} \text{ eV}$$

**Reduced EL (alternative form using wavelength):**
$$\phi_{EL}^{reduced}(\lambda) = \frac{\phi_{EL}(\lambda)}{(hc/\lambda)^3}$$

**Relationship to detailed balance:**
The intersection of reduced EL and EQE curves provides information about the radiative open-circuit voltage ($V_{oc}^{rad}$) and the non-radiative recombination losses in the device.

## Usage

Open `Reduced_EL_EQE.ipynb` in Jupyter Notebook:

1. Load your EL and EQE data files (CSV format)
2. Run the reduction calculations
3. Visualize the reduced spectra
4. Analyze the intersection point for device characterization

## Applications

This analysis is particularly useful for:
- Determining the radiative efficiency limit of solar cells
- Quantifying non-radiative recombination losses
- Comparing different device architectures
- Studying the effect of processing conditions on device physics

## Dependencies

- Python 3.x
- NumPy
- Pandas
- Matplotlib
- SciPy (for interpolation and peak finding)

## Author

mzjswjz
