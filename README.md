# ✍️ Handwritten Digit Recognition | LeNet-5 & MNIST

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=flat-square&logo=keras&logoColor=white)
![MNIST](https://img.shields.io/badge/Dataset-MNIST-blue?style=flat-square)
[![Kaggle](https://img.shields.io/badge/Kaggle-Notebook-20BEFF?style=flat-square&logo=kaggle&logoColor=white)](https://www.kaggle.com/code/mostafaelsayed7/handwritten-digit-recognition-lenet-5-mnist)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1OBag6SbVs7QuJGCVGi7fqhRytIKawKrY?usp=sharing)

> LeNet-5 implemented from scratch achieving **97.7% accuracy** on MNIST —
> one of the most iconic benchmarks in deep learning history.

---

## 📌 Project Overview

This project reproduces the classic **LeNet-5 architecture** (LeCun et al., 1998)
from scratch using TensorFlow & Keras, trained and evaluated on the MNIST dataset
of 70,000 handwritten digit images. Directly applicable in:

- 📬 Postal automation & ZIP code recognition
- 🏦 Bank check processing & amount reading
- 📋 Form digitization & document processing
- 🔢 Any system requiring handwritten numeral recognition

---

## 🏗️ Architecture

```
Input (32×32×1)
    ↓
C1 — Conv2D(6 filters, 5×5, tanh)        → 28×28×6
    ↓
S2 — AveragePooling2D(2×2)               → 14×14×6
    ↓
C3 — Conv2D(16 filters, 5×5, tanh)       → 10×10×16
    ↓
S4 — AveragePooling2D(2×2)               → 5×5×16
    ↓
Flatten                                   → 400
    ↓
FC5 — Dense(120, tanh)
    ↓
FC6 — Dense(84, tanh)
    ↓
Output — Dense(10, softmax)              → 10 classes (0–9)
```

---

## 📊 Results

| Metric | Value |
|---|---|
| Dataset | MNIST (60,000 train / 10,000 test) |
| Test Accuracy | **97.7%** |
| Optimizer | Adam |
| Loss Function | Categorical Crossentropy |
| Epochs | 2 |
| Batch Size | 32 |

---

## 🔧 Preprocessing Pipeline

| Step | Detail |
|---|---|
| Padding | 28×28 → 32×32 (LeNet-5 requirement) |
| Normalization | Pixel values scaled to [0, 1] |
| One-Hot Encoding | Labels encoded to 10-class vectors |
| Channel Expansion | Shape expanded to (32, 32, 1) |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| `tensorflow` / `keras` | Model building & training |
| `numpy` | Array operations & padding |
| `matplotlib` | Training curves & sample visualization |
| `visualkeras` | Architecture layer visualization |

---

## ▶️ How to Run

1. Open in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1OBag6SbVs7QuJGCVGi7fqhRytIKawKrY?usp=sharing)

2. Or view on Kaggle:

[![Kaggle](https://img.shields.io/badge/View%20on-Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/code/mostafaelsayed7/handwritten-digit-recognition-lenet-5-mnist)

3. Install dependencies:
```bash
pip install tensorflow numpy matplotlib visualkeras
```

4. Run all cells — training takes ~2 minutes on CPU, under 30 seconds on GPU.

---

## 📁 Project Structure

```
handwritten-digit-recognition/
│
├── notebook.ipynb     # Full LeNet-5 implementation
└── README.md          # Project documentation
```

---

## 👤 Author

**Mostafa El-Sayed** — Data Scientist | Computer Vision Engineer

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/mostafa-nfc)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:m.e.2172000@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/MostafaELsayed-217)
