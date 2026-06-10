# RegGNN: Explainable Heterogeneous Graph Neural Network for AML Detection via Regulatory Signal Integration

<p align="center">
  <img src="https://img.shields.io/badge/IEEE-Published-blue">
  <img src="https://img.shields.io/badge/Patent-Published-green">
  <img src="https://img.shields.io/badge/Python-3.10+-yellow">
  <img src="https://img.shields.io/badge/PyTorch-Geometric-red">
  <img src="https://img.shields.io/badge/Explainable%20AI-XAI-purple">
</p>

---

## Overview

RegGNN is a novel Explainable Heterogeneous Graph Neural Network (HGNN) framework designed for Anti-Money Laundering (AML) detection by integrating regulatory complaints directly into financial transaction networks.

Unlike traditional AML systems that rely solely on transaction patterns, RegGNN incorporates:

- Customer entities
- Accounts
- Transactions
- Regulatory Complaints

into a unified heterogeneous graph structure.

The model learns how risk propagates through financial ecosystems and provides interpretable explanations using relation-aware attention mechanisms.

---

## Research Contributions

### Novel Contributions

✅ Heterogeneous Financial Graph Construction

✅ Regulatory Complaint Integration

✅ Relation-Aware Attention Mechanism

✅ Curriculum Fidelity Training Strategy

✅ Explainable Risk Propagation Framework

✅ Attention-Based AML Interpretability

---

## Published Research

### IEEE Conference Publication

**Title**

RegGNN: An Explainable Heterogeneous Graph Neural Network for AML Detection via Regulatory Signal Integration

Published in:

**2026 International Conference on Recent Advancement in Electrical, Computer and Communication Technologies (IECCT)**

Publisher:

IEEE

### Research Outcomes

| Metric | Score |
|----------|----------|
| Accuracy | 94.8% |
| Precision | 93.1% |
| Recall | 95.5% |
| F1 Score | 94.3% |
| AUC | 0.93 |

---

## Patent Publication

### Patent Title

Explainable Heterogeneous Graph Neural Network System for Anti-Money Laundering Using Regulatory Complaint Integration

### Patent Application

Application No: 202641023896 A

Publication Date:
06 March 2026

### Innovation Highlights

- Regulatory complaint-driven AML detection
- Risk propagation across financial networks
- Explainable AI-based compliance framework
- Multi-relational graph learning architecture
- Financial crime intelligence integration

---

## Problem Statement

Traditional AML systems suffer from:

- High false positives
- Rule-based limitations
- Lack of explainability
- Inability to model network relationships
- Ignoring external regulatory intelligence

RegGNN addresses these challenges through graph-based reasoning and explainable AI.

---

## System Architecture

```text
Customer Nodes
      │
      ▼
Account Nodes
      │
      ▼
Transaction Nodes
      │
      ▼
Regulatory Complaint Nodes
      │
      ▼
Heterogeneous Graph Construction
      │
      ▼
Relation-Aware Attention
      │
      ▼
Curriculum Fidelity Training
      │
      ▼
AML Risk Prediction
      │
      ▼
Explainable Decision Output
```

---

## Dataset Characteristics

Synthetic AML Dataset

| Entity | Count |
|----------|----------|
| Customers | 50,000 |
| Accounts | 75,000 |
| Transactions | 500,000 |
| Regulatory Complaints | 2,500 |

Dataset Duration:
24 Months

Training Period:
18 Months

Testing Period:
6 Months

---

## Technology Stack

### Machine Learning

- PyTorch
- PyTorch Geometric
- Scikit-Learn

### Data Science

- NumPy
- Pandas
- SciPy

### Visualization

- Matplotlib
- Seaborn

### Graph Analytics

- NetworkX
- Graph Neural Networks

---

## Installation

Clone Repository

```bash
git clone https://github.com/yourusername/RegGNN.git

cd RegGNN
```

Install Dependencies

```bash
pip install -r requirements.txt
```

Run Training

```bash
python train.py
```

Run Evaluation

```bash
python evaluate.py
```

---

## Model Performance

| Model | Accuracy |
|---------|-----------|
| Feature-MLP | 76.4% |
| Topo-GCN | 84.2% |
| Hetero-GAT | 88.7% |
| RegGNN | 94.8% |

RegGNN significantly outperforms traditional machine learning and graph-based baselines.

---

## Explainability Features

### Attention Weight Analysis

The model identifies which relationships contribute most to risk prediction:

- Filed Against → Highest Impact
- Performs → Medium Impact
- Owns → Moderate Impact
- Involves → Lower Impact

### Risk Propagation

RegGNN can detect suspicious entities even when they have no direct fraudulent activity by analyzing indirect regulatory connections.

---

## Applications

### Banking

- Transaction Monitoring
- Customer Risk Scoring

### Financial Institutions

- Compliance Automation
- Suspicious Activity Detection

### Government Agencies

- Financial Crime Investigation
- Regulatory Intelligence Systems

### FinTech

- Real-Time AML Monitoring
- Explainable Risk Analytics

---

## Research Team

### Lead Student Researcher & Co-Inventor

**Sanjay R**

- Primary Implementation Engineer
- Graph Neural Network Development
- AML Modeling
- Explainable AI Research
- Experimental Evaluation

### Research Supervisor

**Theophilus F**

Assistant Professor

Department of Artificial Intelligence and Data Science

VSB College of Engineering Technical Campus

### Co-Researchers

- Sanjay Kumar R
- Sanju P G

---

## Intellectual Property

This project resulted in:

### IEEE Conference Publication

Published in IEEE IECCT 2026.

### Patent Publication

Published Indian Patent Application:

Explainable Heterogeneous Graph Neural Network System for Anti-Money Laundering Using Regulatory Complaint Integration

Application Number:
202641023896 A

---

## Citation

```bibtex
@inproceedings{reggnn2026,
  title={RegGNN: An Explainable Heterogeneous Graph Neural Network for AML Detection via Regulatory Signal Integration},
  author={Theophilus F and Sanjay R and Sanjay Kumar R and Sanju P G},
  booktitle={IEEE IECCT},
  year={2026}
}
```

---

## Acknowledgements

Department of Artificial Intelligence and Data Science

VSB College of Engineering Technical Campus

IEEE IECCT 2026

---

## Contact

Sanjay R

AI & Data Science Researcher

Email: sanjayrao0508@gmail.com

LinkedIn: www.linkedin.com/in/sanjayr0508

GitHub: https://github.com/sanjay-r-0508

---

⭐ If you find this research useful, please consider starring the repository.
