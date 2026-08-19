# UAQRF - IJASE Article Reproducibility Package

**Manuscript:** *Uncertainty-Adaptive Quantum Residual Fusion for Imbalanced Steel Surface Fault Classification: A State-Vector Simulation Study*

## Problem and novelty
UAQRF addresses imbalanced seven-class steel surface-fault classification with a leakage-safe uncertainty router. LightGBM and ExtraTrees provide out-of-fold probabilities; entropy plus inter-model disagreement selects a 1-, 2-, or 3-layer six-qubit feature circuit. A validation-only residual gate decides when quantum-derived features are blended with the classical ensemble.

## Dataset
UCI Machine Learning Repository, **Steel Plates Faults** (id 198), 1,941 samples, 27 features, 7 classes. DOI: 10.24432/C5J88N. License: CC BY 4.0.

## Quantum evidence boundary
The quantum branch is an **exact classical NumPy state-vector simulation**. No quantum hardware, shot sampling, device noise, transpilation, queue latency, or quantum-advantage claim is used.

## Reproduction
1. Open `UAQRF_Steel_Faults_IJASE_Colab.ipynb` in Google Colab.
2. Run all cells. The notebook installs `lightgbm` and `ucimlrepo`.
3. `FAST_MODE=False` reproduces the ten fixed manuscript seeds: 7, 19, 31, 43, 59, 71, 83, 97, 109, 127.
4. Generated outputs include seed-level metrics, routing statistics, the main results figure, and an input-output example.

## Verified manuscript run (10 seeds)
- UAQRF macro-F1: **0.835 ± 0.025**
- UAQRF balanced accuracy: **0.843 ± 0.029**
- UAQRF accuracy: **0.803 ± 0.029**
- Classical ensemble macro-F1: **0.833 ± 0.026**
- Static-depth quantum fusion macro-F1: **0.828 ± 0.033**
- Mean adaptive depth: **1.67**
- Residual quantum route fraction: **39.9%** (about 60.1% can bypass it)

The strongest-baseline gains are modest and are not presented as proof of quantum advantage.
