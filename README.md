# Chipless RFID Detection & Decoding in an Embedded RF Environment

## Overview

This research project focuses on improving the **detection and decoding of chipless RFID tags in realistic RF environments**.

Chipless RFID systems encode information through electromagnetic resonances. In practical environments, reflections, interference and noise can overlap with the useful tag response and reduce decoding reliability.

The work investigates signal-processing techniques for identifying and extracting the useful RFID response in complex propagation environments.

---

## Research Context

This work was carried out during the 2024–2025 academic year in collaboration with:

- LCIS – Laboratoire de Conception et d'Intégration des Systèmes
- Grenoble INP / Université Grenoble Alpes
- IDYLICC Technology

### Academic Supervision

- Louis Morge-Rollet
- Étienne Perret

---

## Research Problem

In realistic RF environments, the received signal may contain:

- environmental reflections,
- multipath propagation,
- interference,
- noise,
- and the useful electromagnetic response of the RFID tag.

These effects can make the identification of the useful tag response more difficult.

The project therefore investigated adaptive signal-processing approaches for improving detection and decoding robustness.

---

## Methods

Two detection strategies were investigated:

### Energy-Based Detection

A classical method based on the energy distribution of the received signal was used as a reference approach.

### Spectral-Entropy-Based Detection

An adaptive detection strategy based on **spectral entropy** was investigated to better identify the useful portion of the RFID response under changing environmental conditions.

The objective was to improve robustness compared with a fixed detection strategy.

---

## Experimental Evaluation

The proposed approach was evaluated under different simulated and experimental RF conditions involving:

- noise,
- environmental interference,
- multipath reflections,
- and varying propagation conditions.

The analysis included:

- time-domain signal analysis,
- frequency-domain analysis,
- spectral analysis,
- RF measurements,
- comparison between simulated and measured behavior,
- and decoding performance evaluation.

---

## Main Results

The spectral-entropy-based approach demonstrated improved robustness compared with the classical energy-based method under the evaluated noisy and reflective RF conditions.

The method provided a more adaptive way of isolating the useful RFID response while preserving the information required for decoding.

Selected figures are provided only to illustrate the general methodology and experimental behavior.

---

## Engineering Work

The project involved:

- RF and microwave modelling
- Electromagnetic simulation
- VNA measurements and RF characterization
- MATLAB signal processing
- Python-based validation
- Time- and frequency-domain analysis
- Experimental validation
- FPGA-oriented implementation studies

---

## Tools & Technologies

| Area | Tools / Methods |
|---|---|
| RF & Microwave | RF characterization, VNA measurements |
| EM Simulation | Ansys HFSS, CST Studio Suite |
| Signal Processing | MATLAB, spectral analysis, filtering |
| Validation | MATLAB, Python |
| Embedded Hardware | FPGA, VHDL / Verilog |
| Application | Chipless RFID |

---

## Skills Demonstrated

- RF & Microwave Engineering
- Signal Processing
- Chipless RFID
- Electromagnetic Simulation
- RF Measurements
- Experimental Validation
- MATLAB
- Python
- FPGA
- Research Methodology
- Scientific Communication

---

## Confidentiality & Intellectual Property

This repository provides a high-level presentation of the research work for academic and professional portfolio purposes.

Detailed implementation, source code, experimental datasets, internal software, proprietary parameters and confidential technical information are not publicly disclosed.

Some aspects of the work were developed within an academic and industrial research environment and may be subject to institutional or intellectual-property restrictions.

---

## Author

**Eya Sahli**  
RF, Microwave & Signal Processing Engineer

## Academic Supervision

**Louis Morge-Rollet**  
**Étienne Perret**
