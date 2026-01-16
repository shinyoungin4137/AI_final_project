# 🎬 Optimizing BERT for Sentiment Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-1.12%2B-ee4c2c)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626)
![Accuracy](https://img.shields.io/badge/Accuracy-94.70%25-brightgreen)

## 📌 Project Overview
This project focuses on **optimizing BERT fine-tuning** for sentiment analysis using the IMDB dataset. 
By implementing advanced training strategies such as **Layer-wise Learning Rate Decay (LLRD)** and **Stochastic Weight Averaging (SWA)** within a single Jupyter Notebook, we achieved a **state-of-the-art accuracy of 94.70%**, significantly outperforming standard baselines.

> **📄 [Read Full Report (PDF)](./Report%20file.pdf)**
> *Click the link above to view the detailed academic report, including theoretical background and ablation studies.*

---

## 📂 Repository Contents
This repository consists of the following key files:

- **`final-project_finetuning _w_BERT.ipynb`** - The **complete source code** in a single Jupyter Notebook.
  - Includes: Data Preprocessing, Model Architecture, Training Loop (with optimizations), and Inference.
- **`Report file.pdf`**
  - The final project report documenting the methodology, experiments, and results.

---

## 🚀 Key Methodologies
To address **catastrophic forgetting** and **overfitting**, the following techniques were applied:

1.  **Layer-wise Learning Rate Decay (LLRD)**
    -   Applied differential learning rates ($\xi=0.95$) to preserve linguistic features in lower layers.
2.  **Stochastic Weight Averaging (SWA)**
    -   Averaged weights from the final epochs to find a flatter minimum and enhance generalization.
3.  **Label Smoothing**
    -   Softened target labels ($\alpha=0.1$) to prevent model overconfidence.
4.  **Mixed Precision (FP16)**
    -   Optimized for GPU memory efficiency and faster training.

---

## 📊 Experimental Results
We compared our optimized model against a standard baseline (Seq=128).

| Configuration | Accuracy | Improvement |
| :--- | :---: | :---: |
| Baseline | 92.11% | - |
| **Final Optimized Model** | **94.70%** | **+2.59%** |

---

## 💻 How to Run
Since the code is a self-contained Jupyter Notebook, you can run it easily on Google Colab.

1.  Download `final-project_finetuning _w_BERT.ipynb`.
2.  Upload the file to **[Google Colab](https://colab.research.google.com/)**.
3.  Set the runtime type to **GPU** (Runtime > Change runtime type > T4 GPU).
4.  Run all cells to reproduce the results.

---

## 👨‍💻 Author
**Young-In Shin**
- **Affiliation:** Dept. of Computer Science & Engineering, Soongsil University
- **Contact:** shinyoungin4137@naver.com
