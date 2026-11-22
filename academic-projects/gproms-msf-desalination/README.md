# Modelling and Simulation of Multi-Stage Flash Desalination Using gPROMS

**Abbas Rajaei · MSc Advanced Chemical Engineering · University of Bradford**  
**Module:** Desalination Technology (CPE7004-B) · **Individual Coursework 2, January 2024**

This project page summarises a submitted MSc coursework report on the steady-state and dynamic modelling of a **once-through multi-stage flash (OT-MSF) desalination process** in gPROMS. The coursework also included a separate comparison of reverse-osmosis model predictions with laboratory measurements.

> **Document status:** Technical summary is public. The full 32-page submitted coursework PDF is prepared but still requires upload to GitHub. The original executable gPROMS model files are not available.

## Steady-state mathematical model

The coursework formulated flash-stage mass and energy balances and heat-transfer relationships for the brine heater and condensers. It included equations for brine and distillate flows, salinity, temperature distribution, and the performance ratio.

A degrees-of-freedom analysis gave **N + 13** specifications for N stages using the equation and variable count in the report. The three-stage example therefore required **16** operating/model specifications.

At a nominal freshwater production rate of **1.2 kg/s**, gPROMS simulations were used to examine the effect of **one to six flash stages** on heat recovery, steam requirement, equipment area and annualised cost.

## Performance and stage-number trade-offs

| Stages | Performance ratio | Steam flow (kg/s) | Total heat-transfer area (m²) | Total annualised cost (reported units) |
|---:|---:|---:|---:|---:|
| 1 | 0.840 | 1.416 | 372.22 | 2.03 × 10⁶ |
| 2 | 0.960 | 1.247 | 244.10 | 2.56 × 10⁶ |
| 3 | 1.136 | 1.055 | 211.06 | 3.18 × 10⁶ |
| 4 | 1.399 | 0.857 | **203.80** | 3.60 × 10⁶ |
| 5 | **1.824** | **0.657** | 214.11 | 4.26 × 10⁶ |
| 6 | 2.620 | 0.456 | 253.38 | 4.76 × 10⁶ |

*Data from Table 2 of the submitted coursework. The report does not clearly specify the currency used for the annualised-cost values.*

Increasing stage count generally reduced the heating-steam requirement, but increased the calculated annualised cost under the selected cost assumptions. The **minimum heat-transfer area occurred at four stages (203.8 m²)**. Increasing to five stages improved the performance ratio by approximately **30%**, while increasing area by approximately **5%**.

The coursework selected **five stages** on the basis of the performance-ratio versus heat-transfer-area trade-off. This was **not** the minimum-annualised-cost choice, and it is not a universal optimum for other plant sizes or cost assumptions.

## Dynamic modelling

The gPROMS dynamic simulations examined the influence of changes in seawater temperature and top-brine temperature.

**Seawater temperature:** A base case of **24 °C** was changed to **18 °C at 30 minutes** and then to **28 °C at 60 minutes**. The simulated responses included brine flow, cooling-water and feed flows, steam requirement, and performance ratio.

**Top-brine temperature:** A separate disturbance increased the top-brine temperature from **90 °C to 92 °C**. The resulting transient process responses were evaluated.

The coursework also discussed the impacts of heat-exchanger fouling and non-condensable gases on thermal performance and reviewed published control strategies. The literature review of PID and advanced controllers is **not** presented as a controller developed in this coursework.

## Reverse-osmosis comparison

An additional task compared gPROMS predictions for permeate flow and salinity with laboratory measurements. The report discussed the reduction in permeate flow with increasing feed concentration and discrepancies between predictions and measurements.

## Deliverables and limitations

The submitted PDF contains the calculations, simulation plots, assumptions and references. The gPROMS executable model files are **not included**, so this page documents modelling work rather than offering a fully reproducible software package.

The original report also incorporates cited third-party literature figures, whose public redistribution rights need to be checked before posting the complete PDF.

---

**Suggested CV link:** This project page may be linked as `gPROMS — MSF Desalination Modelling` while the complete PDF is being uploaded.
