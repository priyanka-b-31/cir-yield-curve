# CIR Yield Curve Modelling

Stochastic interest rate modelling using the Cox-Ingersoll-Ross (CIR) model and CIR++ extension on real bond yield data.


---

## Overview

This project implements, calibrates, and extends the CIR short-rate model to reconstruct a full yield curve using only the 3-Month yield as input. The model achieves an out-of-sample R² of 0.8928, exceeding the 0.85 target threshold.

## Structure

| Phase | Description |
|-------|-------------|
| A | Data engineering and preprocessing |
| B | CIR model implementation and MLE/curve-fit calibration |
| C | Yield curve prediction from 3M rate alone |
| D | CIR++ extension (Brigo-Mercurio) |
| E | Critical analysis and limitations |

## Results

| Model | Overall R² | Status |
|-------|-----------|--------|
| Base CIR | 0.8928 | ✅ PASSED |
| CIR++ | 0.8769 | ✅ PASSED |

## Dataset

- Training: 2016-05-19 → 2024-04-26 (1976 days, 9 maturities)
- Testing: 2024-04-29 → 2026-04-29 (495 days, 5 maturities)
- Maturities: 3M, 6M, 9M, 1Y, 2Y, 5Y, 10Y, 20Y, 30Y

## Tech Stack

- Python, NumPy, Pandas, SciPy, Scikit-learn, Matplotlib
- Google Colab
