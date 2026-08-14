# Common-Source Amplifier

## Objective

Design and simulate a CMOS Common-Source amplifier using Cadence Virtuoso and Spectre.

## Technology

- PDK: GPDK090
- Simulator: Spectre
- Environment: Cadence Virtuoso

## Analyses

- [x] DC Analysis
- [x] AC Analysis
- [x] Transient Analysis
- [ ] Phase Response
- [ ] -3 dB Bandwidth
- [ ] Post-layout Simulation

## Current Results

### DC Analysis

The output voltage decreases as the input voltage increases, showing the inverting characteristic of the Common-Source amplifier.

### AC Analysis

Approximate midband voltage gain:

\[
|A_v| \approx 2.05
\]

High-frequency roll-off begins at approximately:

\[
f_H \approx 4\,GHz
\]

### Transient Analysis

The output signal is approximately 180° out of phase with the input signal.

The transient input amplitude was reduced to approximately 10 mV to observe small-signal behavior.

## Tools

- Cadence Virtuoso
- Spectre
- ViVA
- GPDK090

## Project Status

In progress.
