# NRNN: Non-linear Analytical Rock Neural Network

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Framework](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?logo=PyTorch&logoColor=white)](https://pytorch.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**NRNN (Non-linear Analytical Rock Neural Network)** is a novel physics-informed deep learning framework designed for modeling the highly non-linear deformation of rocks and rapidly assessing deep tunnel excavations. By explicitly embedding mathematical constitutive laws into a forward fusion network architecture, NRNN acts as a rigorous structural regularizer, eliminating physically inadmissible predictions and ensuring exceptional stability.

Developed by a collaborative research team from **The University of Sydney**, **Monash University**, and **Wuhan University**.

---

## 🚀 Overview

Traditional purely data-driven neural networks often act as unconstrained "black boxes" when modeling geomaterials, leading to physical inconsistencies (e.g., violating yield surfaces) and spatial error accumulation in iterative simulations. 

To bridge the gap between data-driven intelligence and physics-based engineering simulation, **NRNN** introduces:
1. An **Equally-Weighted Physics-Guided Forward Fusion Architecture** that integrates the Non-linear Analytical Rock (NAR) constitutive formulation directly into the network.
2. An **Autoregressive Spatial Deduction Engine** that mitigates spatial error accumulation during recursive predictions for deep tunnel Boundary Value Problems (BVPs).

---

## ✨ Key Features

* **Physics-Guided Forward Fusion:** Embeds the NAR constitutive laws (strength evolution $f=0$ and lateral deformation compatibility $g=0$) directly into the forward pass, forcing the network into a strict residual learning paradigm.
* **Elimination of Non-Physical Artifacts:** Effectively eliminates physically inadmissible predictions observed in standard ANNs, reducing principal stress prediction errors (MSE) by up to 75%.
* **Autoregressive Tunnel Engine:** Seamlessly integrated with a semi-analytical solver for deeply buried circular tunnels, enabling millisecond-level reconstruction of full-field stress–strain distributions without spatial error snowballing.
* **Sequential Hybrid Optimizer:** Utilizes a custom two-stage optimization strategy (Adam for global exploration + L-BFGS-B for high-precision fine-tuning) to overcome gradient flow pathologies in highly non-convex solid mechanics.
* **Broad Lithological Generalization:** Rigorously verified against comprehensive independent experimental datasets encompassing conventional quasi-brittle rocks (limestone, sandstone) and highly non-linear geomaterials (marble, shale).

---

## 🛠️ Installation & Usage

### Prerequisites
* Python 3.8+
* PyTorch 1.12+
* NumPy, SciPy, Matplotlib, Pandas
---
## 📊 Datasets

The high-fidelity synthetic datasets and independent experimental datasets used in this study rigorously evaluate the model across varying degrees of geomechanical complexity. They cover four distinct rock types:

* **Limestone**
* **Marble**
* **Sandstone**
* **Shale**

> **Data Availability:** The datasets are available from the corresponding author upon reasonable request.
---


## 📢 Notice
The full source code will be officially released and made publicly available in this repository upon the publication of the related paper.
---


## 📜 Citation

If you use this software in your research, please cite our corresponding work:

```bibtex
@article{li2026nrnn,
  title={NRNN: A Physics-Informed Neural Framework for Non-linear Rock Modelling and Deep Tunnel Analysis},
  author={Li, Zhihang and Shen, Luming and Zhang, Chunshun and Tang, Yaolan and Zhao, Jian},
  journal={Preprint},
  year={2024}
}
