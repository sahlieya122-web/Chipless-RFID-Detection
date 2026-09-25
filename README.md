# Chipless RFID Detection & Decoding in an Embedded RF Environment

## Overview

This research project focuses on the **detection and decoding of chipless RFID tags in realistic RF environments**.

Unlike conventional RFID systems, chipless RFID tags do not contain an integrated electronic chip. Instead, the information is encoded through the electromagnetic resonances of the tag structure.

The main objective of this work was to improve the robustness of tag detection and decoding in the presence of:

- noise,
- environmental reflections,
- multipath effects,
- and quasi-optical interference.

The project compares a **classical energy-based detection method** with a new **spectral entropy-based approach** for the adaptive estimation of the useful signal extraction instant `Tstart`.

---

## Research Context

This project was carried out during 2024–2025 in collaboration with:

- **LCIS Laboratory**
- **Grenoble INP**
- **Université Grenoble Alpes**
- **IDYLICC Technology**

Supervisors:

- Louis Morge-Rollet
- Étienne Perret

The work is related to:

- RF and microwave systems
- Chipless RFID
- Signal processing
- Embedded systems
- RF characterization
- Robust detection in complex environments

---

## Chipless RFID Principle

A chipless RFID reader emits a radio-frequency signal toward the tag.

The physical structure of the tag modifies and backscatters the incident RF signal. The returned signal contains a characteristic spectral signature that can be used to identify the tag.

In the studied decoding method:

- the frequency range is approximately **3.1 GHz to 6 GHz**,
- the spectrum is divided into **150 MHz bands**,
- each band represents one bit,
- presence of a resonance peak corresponds to `1`,
- absence of a resonance peak corresponds to `0`.

The final binary sequence represents the identifier of the tag.

---

## Main Problem

In an ideal environment, the resonant frequencies of the tag are clearly visible.

However, in real environments, the RF signal interacts with surrounding objects and reflective surfaces.

This creates additional echoes and interference that can overlap with the useful tag response.

The received signal may therefore contain:

- quasi-optical interference,
- environmental reflections,
- additive noise,
- useful resonances from the RFID tag.

These effects can significantly reduce decoding accuracy.

The main research question was:

> How can the useful starting instant `Tstart` be determined automatically while removing irrelevant interference and preserving the RFID tag information?

---

## Classical Method: Energy-Based Detection

The classical approach detects the maximum-energy region of the received signal.

A temporal window is then selected in order to isolate the useful part of the RFID response.

### Advantages

- Simple implementation
- Effective in low-noise environments
- Low computational complexity

### Limitations

The main limitation is that `Tstart` is fixed.

In real environments, RF conditions are dynamic and can vary because of:

- reflections,
- interference,
- noise,
- propagation changes.

As a result, a fixed `Tstart` can reduce the robustness of the detection process.

---

## Proposed Method: Spectral Entropy Detection

To improve robustness, a new approach based on **spectral entropy** was investigated.

The received signal is divided into temporal segments.

For each segment, the normalized spectral distribution is calculated and the spectral entropy is evaluated.

The spectral entropy is defined as:

\[
H_m = -\sum_k P_m[k]\log_2(P_m[k])
\]

where:

- `P_m[k]` is the normalized spectral density,
- `H_m` represents the spectral complexity of the current segment.

A concentrated frequency distribution produces lower entropy, while a more uniform spectrum produces higher entropy.

By analyzing the evolution of spectral entropy over time, it becomes possible to identify the transition between interference and the useful resonant response of the tag.

---

## Adaptive Tstart Detection

In the studied example, the spectral entropy reaches a minimum at approximately **12 ns**.

This minimum corresponds to the end of the dominant quasi-optical interference.

The detected instant can therefore be used as an adaptive value of `Tstart`.

After extracting the signal from this instant:

- the useful tag response becomes more visible,
- resonant frequencies are easier to identify,
- decoding becomes more robust.

---

## Robustness Evaluation

The proposed method was evaluated under several RF scenarios.

### Case 1

Quasi-optical interference + noise

### Case 2

Quasi-optical interference + 1 reflection + noise

### Case 3

Quasi-optical interference + 2 reflections + noise

### Case 4

Quasi-optical interference + 3 reflections + noise

For each case, the workflow included:

1. generation of the received signal,
2. addition of noise and reflections,
3. spectral entropy calculation,
4. adaptive `Tstart` detection,
5. extraction of the useful signal,
6. frequency-domain analysis,
7. RFID tag decoding.

---

## Large-Scale Validation

To evaluate the generalization capability of the proposed approach, the method was tested using **1,000 randomly generated RFID identifiers**.

The analysis investigated:

- minimum spectral entropy,
- time position of the entropy minimum,
- influence of SNR,
- influence of reflections,
- decoding performance.

---

## Results

The comparison between the classical energy-based detection method and the spectral entropy method showed that the spectral entropy approach provides better robustness in noisy and reflective environments.

The proposed method:

- automatically adapts the value of `Tstart`,
- isolates the useful RFID response more effectively,
- preserves the tag resonance information,
- improves decoding performance,
- performs better in environments affected by multiple reflections.

The results demonstrate that spectral entropy is a promising method for chipless RFID detection in complex and dynamic RF environments.

---

## Tools and Technologies

- MATLAB
- Python
- Ansys HFSS
- CST Studio Suite
- Vector Network Analyzer (VNA)
- FPGA
- VHDL
- Verilog
- RF and microwave simulation
- Signal processing
- Spectral analysis
- Spectral entropy
- Experimental RF characterization

---

## Skills Demonstrated

- RF Engineering
- Microwave Engineering
- Signal Processing
- Chipless RFID
- Electromagnetic Simulation
- RF Measurements
- VNA Characterization
- Algorithm Development
- Experimental Validation
- MATLAB
- Python
- FPGA
- Embedded Systems

---

## Future Work

A possible continuation of this work is the development of a **hybrid energy–entropy detection method**.

This approach could combine:

- energy detection,
- spectral entropy,
- adaptive environmental analysis,
- embedded real-time implementation,
- FPGA acceleration.

---

## Repository Note

This repository is intended as a public presentation of the research project.

The source code is not publicly available.

Only the methodology, results, technical description and selected figures are presented for portfolio and documentation purposes.

---

## Author

**Eya Sahli**

RF, Microwave & Signal Processing Engineer

Portfolio:  
https://eya-sahli-portfolio.vercel.app
