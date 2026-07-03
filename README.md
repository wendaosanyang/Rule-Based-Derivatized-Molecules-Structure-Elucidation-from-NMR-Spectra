# Rule-Based-Derivatized-Molecules-Structure-Elucidation-from-NMR-Spectra

This repository accompanies the manuscript:

> **Rule-Based Derivatized Molecules Structure Elucidation from NMR Spectra**
> (Submitted to Journal of Chemical Information and Modeling)

The repository contains the code used for molecular generation, data preprocessing, model training, and inference described in the manuscript.

---

# Repository Structure

```
.
├── checkpoints/                  # Example model files (model checkpoints are available on Zenodo)
├── SMILES_Expand/                  # Rule-based molecular generation and SMILES augmentation
├── nmr/                            # Original NMR2Struct implementation (MIT License)
├── training.ipynb                  # Model training example
├── jdx_to_pt.ipynb                 # Convert JCAMP-DX spectra to PyTorch format
├── single_jdx_infer_draw_top15.ipynb
│                                  # Inference for a single spectrum and visualization of Top-15 candidates
├── draw_success_fail_examples.ipynb
│                                  # Visualization of prediction examples
├── LICENSE
└── README.md
```

---

# Overview

This work proposes a rule-based molecular derivatization strategy for improving NMR-based molecular structure elucidation.

The repository mainly includes:

- Rule-based SMILES generation and molecular augmentation
- NMR spectrum preprocessing
- Model training workflow
- Molecular structure prediction
- Result visualization

The trained model checkpoints and processed datasets are provided separately via Zenodo due to GitHub file size limitations.

---

# Data and Model Availability

The processed datasets and trained model checkpoints are available on Zenodo:

**Dataset**

> [(Zenodo DOI)](https://doi.org/10.5281/zenodo.21126628)

**Model checkpoints**

> [(Zenodo DOI)](https://doi.org/10.5281/zenodo.21126628)

After downloading, place the files into

```
Model_Example/
```

or the corresponding directories specified in the notebooks.

---

# Usage

## 1. Molecular augmentation

The scripts under

```
SMILES_Expand/
```

generate rule-based derivatized molecules and expanded SMILES used in this work.

---

## 2. Spectrum preprocessing

Use

```
jdx_to_pt.ipynb
```

to convert JCAMP-DX spectra into PyTorch tensors for training and inference.

---

## 3. Model training

Open

```
training.ipynb
```

to reproduce the model training procedure.

---

## 4. Prediction

Use

```
single_jdx_infer_draw_top15.ipynb
```

to predict candidate molecular structures from an input NMR spectrum and visualize the Top-15 predictions.

---

## 5. Result visualization

```
draw_success_fail_examples.ipynb
```

provides examples for visualizing successful and failed predictions presented in the manuscript.

---

# Code Origin

This repository builds upon the publicly available **NMR2Struct** framework.

The original implementation is available at:

https://github.com/MarklandGroup/NMR2Struct

The source code under

```
nmr/
```

is directly reused from the original implementation without modification and remains distributed under the original MIT License.

The original copyright belongs to the Markland Group.

The remaining scripts and notebooks implement the data processing, molecular augmentation, experimental workflow, and evaluation pipeline developed for this work.

---

# Requirements

The implementation is developed using Python.

Major dependencies include

- PyTorch
- RDKit
- NumPy
- Pandas
- Matplotlib

Additional package versions can be found in the notebooks or environment configuration.

---

# Citation

If you use this repository in your research, please cite

(Your JCIM paper after publication)

and the original NMR2Struct paper.

---

# License

The original implementation in the `nmr/` directory follows the MIT License released by the Markland Group.

All newly developed code in this repository is released under the MIT License unless otherwise specified.
