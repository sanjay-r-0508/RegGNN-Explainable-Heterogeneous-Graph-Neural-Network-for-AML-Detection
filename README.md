# Explainable Heterogeneous Graph Neural Network (XAI-HGNN)

An end-to-end prototype for **explainable customer risk prediction** using a **heterogeneous graph neural network** built with PyTorch Geometric.

This project models multi-entity regulatory-style data (`customer`, `account`, `transaction`, `complaint`) and predicts whether a customer is **Compliant** or **Suspicious**.

---

## Project Highlights

- Heterogeneous graph modeling with multiple node and edge types
- Relation-aware attention using `HeteroConv + GATv2Conv`
- Robust training via noisy-to-clean curriculum-style feature fidelity
- Multi-level explainability:
  - confusion matrix + classification report
  - ROC curve
  - latent space visualization (t-SNE)
  - regulatory complaint impact analysis

---

## Problem Statement

Traditional tabular models often miss relational behavior (who interacts with whom).  
This project addresses that by learning over graph structure and relation types to improve risk signal extraction.

**Target task:** customer-level binary classification

- `0` -> Compliant
- `1` -> Suspicious

---

## Graph Schema

### Node Types
- `customer` (features + labels)
- `account`
- `transaction`
- `complaint`

### Edge Types
- `customer --owns--> account`
- `account --performs--> transaction`
- `complaint --filed_against--> customer`

The graph is converted to undirected for bidirectional message passing.

---

## Model Architecture

Model: `RegGNN`

- **Layer 1:** `HeteroConv` with per-relation `GATv2Conv` (4 heads)
- **Layer 2:** `HeteroConv` with per-relation `GATv2Conv` (2 heads)
- Activation: ELU
- Classification head: linear layer on `customer` embeddings

This provides relation-specific attention while aggregating signals across heterogeneous interactions.

---

## Training Strategy

- Train/Val/Test split: `70% / 15% / 15%` on customer nodes
- Optimizer: Adam
- Learning rate: `0.002`
- Weight decay: `1e-4`
- Loss: CrossEntropy
- Epochs: `100`

### Adaptive Fidelity (Robustness)

At each epoch:

- `fidelity = (epoch / EPOCHS) ** 0.8`
- `x_input = x * fidelity + noise * (1 - fidelity)`

Early training sees noisier features (regularization), later training sees cleaner features (refinement).

---

## Evaluation Snapshot

From the notebook's final test report:

- **Accuracy:** `0.92`
- **Compliant:** Precision `0.94`, Recall `0.96`, F1 `0.95`
- **Suspicious:** Precision `0.79`, Recall `0.69`, F1 `0.74`

Interpretation:
- strong overall discrimination
- suspicious-class recall is the primary improvement area

---

## Explainability Outputs

The notebook includes:

1. Training/validation convergence plots
2. Confusion matrix
3. Classification report
4. ROC curve and AUC
5. t-SNE latent space topology
6. Complaint-history vs no-history predicted risk comparison

---

## Repository Structure

- `Explainable_Heterogeneous_Graph_Neural_Network.ipynb` - main implementation and experiments
- `PROJECT_FULL_DETAILS.md` - deep project documentation
- `TECHNICAL_EXPERT_EXPLANATION_GUIDE.md` - expert-facing explanation strategy
- `MAJOR_INTERVIEW_QA.md` - interview Q&A bank
- `INTERVIEW_QUICK_REVISION.md` - 1-page quick revision sheet

---

## Setup

### 1) Create environment (recommended)

```bash
python -m venv .venv
```

Activate:

- Windows PowerShell:

```bash
.venv\Scripts\Activate.ps1
```

- Linux/macOS:

```bash
source .venv/bin/activate
```

### 2) Install dependencies

```bash
pip install torch torch-geometric networkx matplotlib seaborn scikit-learn pandas numpy
```

> Note: package compatibility may vary by CUDA/CPU and PyTorch version.

### 3) Run

Open and execute:

`Explainable_Heterogeneous_Graph_Neural_Network.ipynb`

---

## Future Improvements

- Temporal graph split to reduce leakage risk
- Class imbalance handling (weighted/focal loss, threshold tuning)
- Calibration metrics (ECE/Brier) for risk decision reliability
- Richer edge features (amount, timestamp, channel)
- Production monitoring and drift detection

---

## Disclaimer

This project currently uses synthetic regulatory-style data to demonstrate architecture and methodology.  
It is a strong prototype, not a production deployment benchmark.

---

## Author

If you use this repository for learning or interviews, feel free to adapt the included explanation guides and Q&A documents.

