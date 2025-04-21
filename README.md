# dns-exfiltration-tabtransformer
A deep learning based approach to detect DNS exfiltration using a simple TabTransformer

# DNS Exfiltration Detection using TabTransformer

This project aims to detect malicious DNS traffic using a lightweight TabTransformer model. It focuses on **offline detection** (not real time) of DNS based data exfiltration — a covert technique where attackers use DNS queries to sneak out sensitive information from a network.

The model leverages deep learning (transformer based architecture) . It was trained and tested on labeled DNS traffic logs, achieving **98% accuracy** with **no false negatives**.

---

## Problem Statement

DNS is a core part of internet communication, but it's often exploited by attackers for stealthy data theft. Traditional rule based detection methods fail to detect these modern attacks due to their dynamic behavior.

This project aims to solve:
- Detection of malicious DNS exfiltration traffic
- Using a transformer model that adapts to patterns in tabular DNS data
- Reducing false positives while increasing detection accuracy

---

## Dataset

The dataset used for this project is publicly available on GitHub:

 [DNS Exfiltration Dataset on Github](https://github.com/Daumel/dns-exfiltration-dataset)

It contains both benign and malicious DNS flows, with 45 features such as:
- Packet sizes
- Domain name structure
- TTL values
- Entropy metrics
- Query timing

---

##  Model

- **TabTransformer**: Designed for tabular data with categorical and numerical features
- **Frameworks**: TensorFlow, Keras, Scikit-learn

The model uses:
- Attention layers to capture feature importance
- Dense + dropout layers for classification
- Adam optimizer with sparse categorical cross-entropy

---

##  Results

- **Accuracy**: 98%
- **Precision**: 96–100%
- **Recall**: 96–100%
- **No False Negatives**
- **AUC Score**: ~1.0


