# Co2-emission-on-vehical
# Vehicle CO₂ Emissions Using Support Vector Regression (SVR)

Author: Md Athar Shihab Biplob  
Module: Machine Learning and Neural Networks  
Student ID: 24082155  

This repository contains the code and report for my assignment on **Support Vector Regression (SVR)** applied to the prediction of **vehicle CO₂ emissions**. The focus is on **how different kernels and hyper-parameters (C, ε, γ) affect SVR behaviour and performance**, compared with a simpler **linear regression** baseline. :contentReference[oaicite:0]{index=0}

---

## 1. Project overview

The project addresses the following questions:

- How well can we predict **CO₂ emissions (g/km)** from engine and fuel-consumption data?
- How does **SVR** compare to **linear regression** on this task?
- How do **kernel choice** and **hyper-parameters** such as **C** and **ε** influence:
  - the shape of the fitted regression function,
  - generalisation performance on unseen data?

The work is implemented in **Python** using **scikit-learn**, **pandas**, **NumPy** and **matplotlib**, and demonstrated in a single Jupyter notebook.

---

## 2. Repository contents

- `Machine_Learning_.ipynb` (or similarly named notebook)  
  Main notebook containing:
  - Data loading and preprocessing  
  - Exploratory Data Analysis (EDA)  
  - 1D experiments: `ENGINESIZE → CO2EMISSIONS`  
  - SVR kernel comparison (linear / poly / RBF)  
  - Hyper-parameter sweeps for **C** and **ε**  
  - Final model evaluation and residual analysis  
  - (Optional) multi-feature pipeline with `ColumnTransformer` + `Pipeline` :contentReference[oaicite:1]{index=1}  

- `Predicting Vehicle CO₂ Emissions Using Support Vector Regres.pdf`  
  <2000-word written tutorial/report that explains the method, the figures and the results in a narrative format. :contentReference[oaicite:2]{index=2}  

- `data/` (optional, if licence allows including the CSV)
  - `FuelConsumptionCo2.csv` – raw dataset from the original source (see Dataset section).

- `README.md` (this file)

- `LICENSE`  
  Licence under which this code and report may be used (e.g. MIT or CC BY-NC; to be chosen).

---

## 3. Technique and focus

The central technique is **Support Vector Regression (SVR)** with a focus on:

- Understanding the role of:
  - **Kernels** (`linear`, `poly`, `rbf`)
  - **Regularisation parameter C**
  - **Epsilon (ε)** for the epsilon-insensitive loss
  - **Gamma (γ)** for the RBF kernel
- Comparing SVR to a **linear regression** baseline
- Interpreting **validation/test metrics** and **residual plots** to judge model quality

The experiments are mainly done in a **1D setting** using only `ENGINESIZE` as the input feature so that the fitted functions can be visualised and directly compared. A multi-feature pipeline is also included in the notebook to illustrate a more realistic workflow. :contentReference[oaicite:3]{index=3}  

---

## 4. Dataset

The project uses the public **FuelConsumptionCO2** dataset (2014) which contains measurements for **1,067** vehicles. Each row corresponds to a vehicle model and includes: :contentReference[oaicite:4]{index=4}  

- `MODELYEAR`  
- `MAKE`, `MODEL`  
- `VEHICLECLASS`  
- `ENGINESIZE`  
- `CYLINDERS`  
- `TRANSMISSION`  
- `FUELTYPE`  
- `FUELCONSUMPTION_CITY`, `FUELCONSUMPTION_HWY`, `FUELCONSUMPTION_COMB`  
- `CO2EMISSIONS` (target, g/km)

If the CSV cannot be distributed in this repo, please download it directly from the official source (e.g. Government of Canada fuel consumption data) and place it in the `data/` folder, then update the path in the notebook.

---

## 5. Getting started

### 5.1. Requirements

- Python 3.9+ (earlier 3.x should also work)
- Packages:
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `seaborn`
  - `scikit-learn`
  - `jupyter` or `jupyterlab` (for running the notebook)

Install dependencies (for example):

```bash
pip install -r requirements.txt
