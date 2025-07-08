# Bayesian PINN for MHD (Magnetohydrodynamics)

This repository contains a prototype implementation of a **Bayesian Physics-Informed Neural Network (B-PINN)** for solving the inverse problem of recovering primitive variables from conserved quantities in **special relativistic magnetohydrodynamics (SRMHD)**. The model is designed to be uncertainty-aware, allowing not only for predictions of physical variables but also for confidence estimation in high-risk inference settings.

## Overview

- **Forward Model**: The MHD system is governed by conservation laws that relate primitive variables (density, pressure, velocity, magnetic field) to conserved quantities.
- **Goal**: Recover primitive variables from simulated conserved quantities using a Bayesian neural network trained with physics-based constraints.
- **Uncertainty Quantification**: The model uses variational inference and Bayesian linear layers to produce distributions over predicted values.

## Key Features

- ✔️ **Bayesian neural architecture** with KL-divergence loss  
- ✔️ **Physics-informed loss function** that minimizes residuals on physical equations  
- ✔️ Predicts both **mean and variance** for each primitive variable  
- ✔️ Includes a warm-up scheduler for KL annealing  

## Usage

Clone the repository and run the notebook:

```
git clone https://github.com/your-username/bpinntest-prototype-987qz.git
cd bpinntest-prototype-987qz
jupyter notebook SRMHD.ipynb
```

## Dependencies

- `torch`  
- `torchbnn` or equivalent Bayesian layers implementation  
- `matplotlib`, `numpy`, `scipy`, `tqdm`  

Install with:

```
pip install -r requirements.txt
```

## Status

This is a **research prototype** under active development. Future plans include:

- Generalization to general relativity
- Extension to radiative MHD   
- Integration into hybrid simulation pipelines  

## Citation

If you use or build on this work, please cite:

**J. Davelaar**, *Bayesian Physics-Informed Neural Networks for SRMHD*, in prep.
