# Implementations of BLS, PIELM, and BPIELM

This repository provides Python implementations of three advanced, non-deep machine learning frameworks:

1.  **Broad Learning System (BLS)**
2.  **Physics-Informed Extreme Learning Machine (PIELM)**
3.  **Bayesian Physics-Informed Extreme Learning Machine (BPIELM)**

These models offer efficient and powerful alternatives to traditional deep learning architectures for various tasks, including classification, regression, and solving partial differential equations (PDEs). The code in this repository is based on the findings from a literature review on these models.

---

## Table of Contents
- [Models Implemented](#models-implemented)
- [Repository Structure](#repository-structure)
- [Getting Started](#getting-started)
- [Acknowledgments](#acknowledgments)
- [References](#references)

---

## Models Implemented

### Broad Learning System (BLS)
The Broad Learning System is a flat, single-layer neural network architecture designed for high efficiency and effectiveness. Unlike deep models that increase complexity through depth, BLS expands horizontally by adding feature and enhancement nodes.

**Key Features:**
* **No Backpropagation:** Output weights are calculated analytically using a closed-form ridge regression solution, eliminating the need for iterative gradient-based optimization.
* **Fast Training:** The one-shot learning process is extremely fast and computationally inexpensive.
* **Incremental Learning:** New data samples or network nodes can be added incrementally without requiring a full retraining of the model from scratch.

### Physics-Informed Extreme Learning Machine (PIELM)
PIELM is a mesh-free and training-free framework for solving linear partial differential equations. It merges the rapid computation of Extreme Learning Machines (ELMs) with the physical consistency of Physics-Informed Neural Networks (PINNs).

**Key Features:**
* **Training-Free:** Solves for the solution of a PDE by constructing and solving a single linear system, completely avoiding iterative training.
* **Physics-Consistent:** The governing physical laws (PDEs) and boundary conditions are embedded directly into the model's formulation.
* **Mesh-Free:** Operates on collocation points and does not require a computational mesh, making it well-suited for problems with complex geometries.

### Bayesian Physics-Informed Extreme Learning Machine (BPIELM)
BPIELM extends PIELM by incorporating a Bayesian probabilistic framework. This allows it not only to solve PDEs but also to quantify the uncertainty in its predictions, which is crucial for applications involving noisy or sparse data.

**Key Features:**
* **Uncertainty Quantification:** By treating the model's output weights as random variables, BPIELM computes a full posterior distribution over the solution space, providing both a mean prediction and a measure of confidence (variance).
* **Robustness to Noise:** The Bayesian approach provides natural regularization, making the model more robust to noisy measurements and preventing overfitting.
* **Forward and Inverse Problems:** The framework is capable of solving both forward problems (finding the solution given parameters) and inverse problems (finding system parameters given solution data).

---

## Repository Structure
The repository contains the following Jupyter Notebooks:
```
/
|-- BLS_CODES.ipynb              # Jupyter Notebook with the implementation and examples for BLS.
|-- PIELM_Codes.ipynb            # Jupyter Notebook with the implementation and examples for PIELM.
|-- BPIELM_Python_code.ipynb     # Jupyter Notebook with the implementation and examples for BPIELM.
`-- README.md                    # This README file.
```

---

## Getting Started

### Usage

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/MEGHAPANKAJ/Literature-Review-On-BLS-PIELM-and-BPIELM.git](https://github.com/MEGHAPANKAJ/Literature-Review-On-BLS-PIELM-and-BPIELM.git)
    cd Literature-Review-On-BLS-PIELM-and-BPIELM
    ```
    
2.  **Open the Jupyter Notebooks:**
    You will need a Jupyter environment to run the code. You can use Google Colab, the classic Jupyter Notebook, or an editor like VS Code with the Python extension.

3.  **Run the code:**
    Open one of the `.ipynb` files (e.g., `BPIELM_Python_code.ipynb`) and run the cells sequentially to see the implementation and results.

---

## Acknowledgments
This work is based on a literature review internship conducted by  **Ananya J R** and **Megha P** under the supervision of **Prof. M. Tanveer**. The implementations are based on the methods described in the following key papers.

---

## References
1.  **Broad Learning System:**
    * Chen, C. and Zhulin Liu. "Broad Learning System: An Effective and Efficient Incremental Learning System Without the Need for Deep Architecture". In: *IEEE Transactions on Neural Networks and Learning Systems* PP (July 2017), pp. 1-15. DOI: `10.1109/TNNLS.2017.2716952`.

2.  **Physics-Informed Extreme Learning Machine:**
    * Dwivedi, Vikas and Balaji Srinivasan. *Physics Informed Extreme Learning Machine (PIELM) A rapid method for the numerical solution of partial differential equations*. July 2019. DOI: `10.48550/arXiv.1907.03507`.

3.  **Bayesian Physics-Informed Extreme Learning Machine:**
    * Liu, Xu et al. "Bayesian Physics-Informed Extreme Learning Machine for Forward and Inverse PDE Problems with Noisy Data". In: *Neurocomputing* 549 (June 2023), p. 126425. DOI: `10.1016/j.neucom.2023.126425`.
