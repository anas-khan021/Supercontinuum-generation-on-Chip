# Supercontinuum Generation in an Integrated Waveguide using Split Step Fourier Method

This project simulates ultrashort pulse propagation and spectral broadening in an integrated nonlinear waveguide platform using the Split Step Fourier Method (SSFM).

The simulation investigates how dispersion and nonlinear effects interact during pulse propagation to generate broadband spectra (supercontinuum generation).

Developed during my internship work in ultrafast photonics and nonlinear waveguide optics.

---

## Overview

Supercontinuum generation is a nonlinear optical phenomenon in which a narrow-band ultrashort laser pulse evolves into a broadband optical spectrum.

This simulation models pulse evolution through:

- Single Mode Fiber (SMF)
- Integrated Nonlinear Waveguide (WG)
- Dispersion effects
- Kerr nonlinearity
- Spectral broadening
- Higher order dispersion terms (up to β₁₀ support)

The propagation is solved numerically using the Split Step Fourier Method.

---

## Physical Effects Included

### Linear Effects
- Group Velocity Dispersion (β₂)
- Third Order Dispersion (β₃)
- Higher Order Dispersion (β₄–β₁₀)

### Nonlinear Effects
- Self Phase Modulation (SPM)
- Kerr Nonlinearity
- Pulse Compression
- Spectral Broadening

### Components Supported
- Single Mode Fiber (SMF)
- Nonlinear Waveguide
- Dispersion Compensating Fiber (DCF)
- Erbium Doped Fiber (EDF)
- Saturable Absorber
- Optical Filter

---

## Simulation Parameters

| Parameter | Value |
|----------|-------|
| Central Wavelength | 1960 nm |
| Spectral Window | 350 THz |
| Grid Size | 4096 points |
| Initial Pulse Duration | 4.4 ps |
| Peak Power | 2 kW |
| Waveguide Length | 1 mm |
| Numerical Method | Split Step Fourier Method |

---

## Method

The pulse evolution is computed using the nonlinear Schrödinger equation:

\[
\frac{\partial A}{\partial z}
=
-\frac{i\beta_2}{2}\frac{\partial^2A}{\partial t^2}
+
i\gamma |A|^2A
\]

The simulation alternates between:

1. Nonlinear propagation in time domain
2. Linear propagation in frequency domain
3. Iterative propagation along the device

---

## Results

### Pulse Evolution

Comparison between input and output temporal pulse profiles.

![Pulse Evolution](pulse+spectrum_good_p=0.5kW, dur=200fs.jpg)

Observed:
- Pulse reshaping
- Temporal compression/broadening
- Nonlinear temporal dynamics

---

### Spectral Evolution

Comparison of initial and output optical spectra.

Observed:
- Spectral broadening
- Supercontinuum generation
- Nonlinear frequency conversion

---
Here the characteristics of the pulse is P=0.5kW, dur=200fs

### Temporal Propagation Along Waveguide

Pulse evolution as a function of propagation distance.

![Propagation Time Domain](images/propagation_time_domain.png)

Observed:
- Pulse compression
- Nonlinear pulse dynamics
- Evolution of temporal envelope

---

### Spectral Broadening Along Propagation

Evolution of optical spectrum during propagation.

![Propagation Spectrum](images/propagation_spectrum.png)

Observed:
- Progressive bandwidth expansion
- Supercontinuum formation
- Dispersion–nonlinearity interaction

---

## Requirements

Install dependencies:

```bash
pip install numpy matplotlib scipy pyqtgraph addict
```

---

## Run

```bash
python SC_on_chip_best_khan.py
```

---

## Skills Demonstrated

- Python Scientific Computing
- Nonlinear Optics
- Supercontinuum Generation
- Waveguide Photonics
- Split Step Fourier Method
- Dispersion Engineering
- Numerical Simulation
- Scientific Visualization

---

## Author

Mohammad Anas Khan

ICB Dijon 
Internship in Ultrafast Photonics and Waveguide Optics
