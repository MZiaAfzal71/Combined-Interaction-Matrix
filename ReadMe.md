# Molecular Solubility Prediction on ESOL

This repository contains a comprehensive experimental study on **aqueous solubility prediction**
using the **ESOL (Delaney) dataset**, covering **graph neural networks**, **descriptor-based
machine learning models**, and **Chemprop message-passing neural networks**.

The project is designed to ensure:
- Rigorous and reproducible evaluation
- Fair comparison across modeling paradigms
- Chemically realistic generalization assessment using scaffold splits

---

## 📁 Repository Structure


### 🔹 `ESOL_Dataset/`
This folder contains:
- The ESOL (Delaney) dataset
- Preprocessed versions used in experiments
- Files equipped with **Bemis–Murcko scaffold information**  
  (Train / Validation / Test labels)

The dataset includes **1,128 molecules** with experimentally measured
aqueous solubility values.

---

### 🔹 `Models/`
This folder contains **all Colab-runnable notebooks** used in the study.

Each notebook is **self-contained** and includes:
- Model description and experimental setup
- Data loading and preprocessing
- Training and evaluation procedures
- Cross-validation and/or scaffold-based evaluation
- Result aggregation and reporting

The models covered include:
- **Edge-Aware Graph Neural Networks**
- **Descriptor-Augmented Edge-Aware GNNs**
- **Random Forest**
- **XGBoost**
- **Chemprop (with and without RDKit descriptors)**

Both **repeated cross-validation (5×5)** and **scaffold-based ensemble evaluations**
are implemented where applicable.

---

### 🔹 `Results/`
This folder contains:
- Aggregated performance metrics (RMSE, MAE, R²)
- Cross-validation statistics (mean ± standard deviation)
- Scaffold split ensemble results
- Tables and figures used for analysis and reporting

All results correspond directly to the notebooks in the `Models/` directory.

---

## 🔁 Evaluation Protocols

The following evaluation strategies are used consistently across models:

- **Repeated Cross-Validation (5×5)**
  - Robust performance estimation
  - Reduced variance due to data splitting

- **Bemis–Murcko Scaffold Split**
  - Chemically realistic generalization assessment
  - Ensemble evaluation using multiple random seeds

---

## ⚙️ Running the Notebooks

All notebooks are designed to run in **Google Colab**.

To speed up training (especially for GNNs and Chemprop models):
1. Open a notebook in Colab
2. Go to **Runtime → Change runtime type**
3. Select **GPU** (T4 recommended)

---

## 🎯 Objective

The goal of this repository is to:
- Compare structure-based, descriptor-based, and hybrid modeling approaches
- Evaluate the impact of edge-aware message passing and descriptor fusion
- Provide reproducible baselines for molecular solubility prediction
- Support research and benchmarking in molecular machine learning

---

## 📄 Notes

- All experiments are conducted with careful prevention of data leakage
- Descriptor normalization is performed using training data only
- Ensemble and aggregation strategies are explicitly documented in each notebook

---

## 📬 Citation

If you use this repository or its results in your work, please cite the
corresponding publication (to be added).
