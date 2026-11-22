# MSc Research — Hydrogen Transport and Flow Assurance

**Abbas Rajaei · MSc Advanced Chemical Engineering · University of Bradford**

This page brings together two related research studies. The published study concerns gas-hydrate equilibrium in hydrogen-rich mixtures. The second study examines how impurities change the hydraulic performance of hydrogen transmission pipelines, including reduced-order mathematical correlations.

> **Research status:** Study 1 is a peer-reviewed publication. Study 2 is a separate research manuscript; it is not presented as a published paper. The full manuscript PDF and graphical abstract are being prepared for public upload.

## Study 1 — Gas-hydrate phase equilibrium in hydrogen-rich mixtures

**Published:** *International Journal of Hydrogen Energy*, volume 94, pages 765–773 (2024).  
**[Read the published article (DOI: 10.1016/j.ijhydene.2024.11.030)](https://doi.org/10.1016/j.ijhydene.2024.11.030)**

This study investigated how hydrogen concentration, impurity composition and pressure affect the equilibrium conditions for gas-hydrate formation. Hydrate dissociation boundaries were predicted over **2–15 MPa** for binary hydrogen mixtures containing CH₄, C₂H₆, C₃H₈, CO₂ and H₂S, as well as selected multicomponent hydrogen–hydrocarbon systems. The objective was to identify conditions at which solid hydrates may be thermodynamically stable and create flow-assurance concerns.

### Thermodynamic modelling

- **Aspen HYSYS v14:** Peng–Robinson equation of state with the Ng–Robinson hydrate model.
- **HydraFlash:** CPA-based fluid modelling with SRK treatment for non-associating components and van der Waals–Platteeuw hydrate theory.
- **Model evaluation:** Predicted pressure–temperature hydrate-equilibrium boundaries were compared with published experimental measurements.

Among the investigated impurities, **H₂S** produced the strongest shift towards higher predicted hydrate formation temperatures. C₃H₈ and C₂H₆ also raised predicted hydrate stability temperatures. Predictive accuracy depended on mixture and pressure: HYSYS generally agreed better with several datasets, while HydraFlash performed better over certain intervals.

## Study 2 — Impurity effects on hydrogen-pipeline hydraulics

**Research output:** Separate unpublished research manuscript.

This study developed a physics-based computational framework linking composition-dependent thermophysical properties with local pipeline hydraulics. The analysis used **NIST REFPROP** for density, dynamic viscosity and compressibility factor, the **Darcy–Weisbach** equation for frictional pressure gradient, and the **Haaland** correlation for turbulent friction factor.

The calculations evaluated **2,160 impurity-containing states** for nine binary mixtures of hydrogen with CH₄, CO₂, Ar, CO, C₂H₆, H₂S, N₂, C₃H₈ and O₂. The study examined three operating constraints:

1. Fixed bulk velocity.
2. Fixed total mixture mass flow.
3. Equivalent hydrogen mass delivery.

The distinction between fixed *mixture* mass flow and fixed *hydrogen* delivery is important: impurities displace hydrogen in the stream, so transporting the same total mass does not transport the same quantity of hydrogen.

### Numerical framework

The local frictional pressure gradient is defined as

```math
G = -\left(\frac{\mathrm dP}{\mathrm dL}\right)_f = \frac{f\rho v^2}{2D}
```

and the corresponding local frictional hydraulic-power requirement per unit length is

```math
\mathcal P_{\mathrm{hyd}} = QG
```

These quantities describe the local frictional contribution. They are **not** predictions of full-pipeline compression work or compressor shaft power.

### Reduced-order mathematical correlations

**Model A — State-resolved correlation.** An impurity-specific seven-coefficient correlation predicts the normalized local hydraulic-power requirement from impurity concentration, pressure and temperature. The coefficients were fitted by ordinary least squares and assessed by grouped cross-validation.

**Model B — Cubic screening correlation.** A concentration-dependent cubic model estimates impurity levels associated with specified increases in local hydraulic-power requirements. It supports screening without repeating the REFPROP-based calculation sequence.

| Research result | Value |
|---|---:|
| Evaluated impurity-containing states | **2,160** |
| Binary hydrogen–impurity systems | **9** |
| State-resolved model: grouped-CV relative RMSE | **0.44%** |
| Maximum absolute grouped-CV relative error | **1.86%** |
| Local frictional hydraulic-power ratio at 10 mol% impurity under equivalent hydrogen delivery | **2.227–4.056×** pure hydrogen |

The mathematical correlations are screening models valid within the studied domain. They should not be extrapolated to untested operating conditions without validation.

### Availability and scope

The full Study 2 manuscript and original graphical abstract have not yet been uploaded to this GitHub page. The manuscript is separate from the published hydrate-equilibrium paper. No REFPROP library files, software source, or experimental pipeline validation data are provided here.

---

**Suggested CV link:** This project page may be linked as `MSc Hydrogen Transport Research` while the standalone project repository is being completed.
