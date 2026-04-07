# MLP-SEV1D-Denoiser

This repository contains a complete workflow for generating synthetic 1D vertical electrical sounding (VES) data, polluting it with Gaussian noise, and training a multilayer perceptron (MLP) to remove noise from apparent resistivity curves.

The workflow is organized into three notebooks:

1. **`CLEAN_DATASET.ipynb`**: Generates synthetic models of stratified earth and their clean Schlumberger-type apparent resistivity curves.

2. **`CORRUPT_DATASET.ipynb`**: Constructs a dataset for noise removal by adding Gaussian noise at different noise levels to the clean curves.

3. **`DENOISING_TRAINING.ipynb`**: Trains and evaluates an MLP that learns to map noisy curves to clean curves.

The datasets in `.npz` format are stored in a folder called **`DATASETS/`**.

---

## Repository structure

```bash
.
├── CLEAN_DATASET.ipynb
├── CORRUPT_DATASET.ipynb
├── DENOISING_TRAINING.ipynb
├── DATASETS/
│ ├── dataset_1d_variable_models_variable_ab2.npz
│ └── dataset_denoising_gaussian.npz
└── README.md
