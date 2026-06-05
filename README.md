# Federated-Learning-IDS
Privacy-Preserving Intrusion Detection System using Federated Learning and Deep Learning Models
# Privacy-Preserving Intrusion Detection System using Federated Learning

## Overview

This project implements a Privacy-Preserving Intrusion Detection System (IDS) using Federated Learning and Deep Learning techniques. The goal is to detect network intrusions while preserving user privacy by ensuring that raw network traffic data remains on local clients.

A comparative analysis was performed between Centralized Learning and Federated Learning using multiple deep learning architectures on the NSL-KDD dataset.

---

## Problem Statement

Traditional Intrusion Detection Systems require centralized collection of network traffic data, which introduces:

- Privacy concerns
- Security risks
- Single point of failure
- Regulatory compliance challenges

Federated Learning addresses these issues by enabling collaborative model training without sharing raw data.

---

## Dataset

**NSL-KDD Dataset**

### Dataset Statistics

- Total Samples: 148,520
- Features: 41
- Classes:
  - Normal
  - DoS (Denial of Service)
  - Probe
  - R2L (Remote to Local)
  - U2R (User to Root)

---

## Data Preprocessing

The following preprocessing techniques were applied:

- Data Cleaning
- Label Mapping
- One-Hot Encoding
- Feature Scaling
- Feature Selection using Mutual Information
- Handling Class Imbalance using Class Weights
- Train-Test Splitting

---

## Models Evaluated

### Centralized Learning

- Multi-Layer Perceptron (MLP)
- Deep Neural Network (DNN)
- Convolutional Neural Network (CNN)
- Long Short-Term Memory (LSTM)
- CNN + LSTM

### Federated Learning

The same architectures were trained using Federated Learning with the FedProx aggregation algorithm.

---

## Federated Learning Configuration

- Number of Clients: 5
- Communication Rounds: 20
- Aggregation Method: FedProx
- Local Training at Each Client
- Privacy-Preserving Distributed Learning

---

## Results

| Model | Centralized Accuracy | Federated Accuracy |
|---------|---------|---------|
| MLP | 95.92% | 97.49% |
| LSTM | 96.72% | 97.55% |
| CNN | 96.73% | 97.00% |
| DNN | 97.14% | 97.16% |
| CNN + LSTM | 95.32% | 96.42% |

### Key Findings

- Federated Learning outperformed Centralized Learning across all architectures.
- Federated LSTM achieved the highest accuracy of **97.55%**.
- FedProx effectively handled heterogeneous client data.
- Privacy was preserved without sharing raw network traffic.
- Federated models demonstrated better generalization and lower error rates.

---

## Performance Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

---

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Scikit-Learn
- Matplotlib
- Federated Learning (FedProx)

---

## Repository Structure

```text
Federated-Learning-IDS/
│
├── README.md
├── FinalReport.pdf
│
├── notebooks/
│   ├── preprocessing.ipynb
│   ├── mlp.ipynb
│   ├── dnn.ipynb
│   ├── cnn.ipynb
│   ├── lstm.ipynb
│   ├── cnn_lstm.ipynb
│   └── federated_learning.ipynb
│
├── results/
│   ├── confusion_matrices/
│   ├── centralized_vs_federated.png
│   ├── performance_improvement.png
│   └── convergence_analysis.png
```

---

## Future Work

- Differential Privacy Integration
- Secure Aggregation Techniques
- Evaluation on CICIDS2017 and UNSW-NB15 datasets
- Improved detection of minority attack classes
- Asynchronous Federated Learning

---

## Project Type

Academic Mini Project completed as part of the B.Tech Computer Science and Engineering curriculum at SASTRA Deemed University.

---

## License

This project is intended for educational and research purposes.
