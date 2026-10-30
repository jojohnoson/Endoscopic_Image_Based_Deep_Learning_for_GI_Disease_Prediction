<div align="center">

# 🩺 Endoscopic Image-Based Deep Learning Approach for Predicting Gastrointestinal Diseases

**A deep learning framework for automated classification of gastrointestinal (GI) diseases from endoscopic images, built as a computer-aided diagnosis (CAD) system to give clinicians early, consistent, and reproducible diagnostic support.**

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-FF6F00?logo=tensorflow&logoColor=white)
![Dataset](https://img.shields.io/badge/Dataset-Kvasir-blue)
![Best Model](https://img.shields.io/badge/Best%20Model-ResNet50-success)
![Accuracy](https://img.shields.io/badge/Test%20Accuracy-84.5%25-brightgreen)
![IEEE](https://img.shields.io/badge/Published-IEEE-00629B?logo=ieee&logoColor=white)

[📄 Read the Paper](https://ieeexplore.ieee.org/abstract/document/11382902) · [🗂️ Kvasir Dataset](https://www.kaggle.com/datasets/meetnagadia/kvasir-dataset)

</div>

---

## 📑 Table of Contents

- [Publication](#-publication)
- [Overview](#-overview)
- [Models Compared](#-models-compared)
- [Methodology](#-methodology)
- [Results and Screenshots](#-results-and-screenshots)
- [Tech Stack](#-tech-stack)
- [Future Work](#-future-work)
- [Citation](#-citation)

---

## 📄 Publication

| | |
|---|---|
| **Title** | Endoscopic Image-Based Deep Learning Approach for Predicting Gastrointestinal Diseases |
| **Authors** | Joel Johnson BV, K Martin Victor |
| **Institution** | Karunya Institute of Technology and Sciences |
| **Venue** | IEEE |
| **Link** | [ieeexplore.ieee.org/abstract/document/11382902](https://ieeexplore.ieee.org/abstract/document/11382902) |

---

## 🔍 Overview

Endoscopy is the standard for diagnosing GI conditions such as polyps, ulcers, and colorectal cancer, but interpretation depends heavily on clinician experience and is prone to fatigue and subjective error.

This project uses **Convolutional Neural Networks (CNNs) with transfer learning** to classify endoscopic images automatically. It compares three architectures to find the best performer.

---

## 🏆 Models Compared

| Model | Test Accuracy |
|---|---|
| 🥇 **ResNet50** | **84.5%** |
| 🥈 MobileNetV2 | 80.5% |
| 🥉 VGG16 | 70.1% |

ResNet50 performed best thanks to its residual (skip) connections, which help it learn deeper, more detailed features. The proposed model also reached **87.6% recall** and an **F1-score of 85.8%**.

---

## ⚙️ Methodology

| Step | Stage | Details |
|:---:|---|---|
| 1 | **Dataset** | [Kvasir](https://www.kaggle.com/datasets/meetnagadia/kvasir-dataset), a multi-class endoscopic image dataset, split 70% train / 15% validation / 15% test |
| 2 | **Preprocessing** | Images resized to 224×224, denoised with Gaussian and median filters, and normalized |
| 3 | **Data augmentation** | Flips, rotation, zoom, brightness/contrast shifts, and CLAHE, expanding the dataset to about 40,000 images |
| 4 | **Model development** | Transfer learning with pre-trained ResNet50, VGG16, and MobileNetV2, with the final layer replaced by a softmax classifier |
| 5 | **Training and tuning** | GPU training with grid-search hyperparameter tuning (learning rate, batch size, epochs) |
| 6 | **Evaluation** | Accuracy, precision, recall, F1-score, and confusion matrix |

---

## 📊 Results and Screenshots

### Overall Workflow / Architecture

<div align="center">
  <img width="857" alt="Screenshot 1" src="https://github.com/user-attachments/assets/b8fd36a6-fba0-4427-86ad-5d94fe2475c5" />
</div>

### Training and Evaluation Outputs

<div align="center">
  <img width="527" alt="Screenshot 2" src="https://github.com/user-attachments/assets/1b600519-d6e1-4c04-8c76-fdee96da31f2" />
  <img width="573" alt="Screenshot 3" src="https://github.com/user-attachments/assets/b5e4427b-80e9-4ffa-8c9b-0de867131b89" />
</div>

### Sample Outputs

<div align="center">
  <img width="186" alt="Screenshot 4" src="https://github.com/user-attachments/assets/3c4d70a2-5fed-4a94-8d47-8fced46a1b41" />
  &nbsp;&nbsp;
  <img width="117" alt="Screenshot 5" src="https://github.com/user-attachments/assets/5419022d-7084-4ff7-b9f4-5c0d2e164d40" />
</div>

### Performance Summary

<div align="center">
  <img width="1000" alt="Screenshot 6" src="https://github.com/user-attachments/assets/f357b31d-5d56-4b6e-bb70-90c19c1e2022" />
</div>

---

## 🧰 Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?logo=keras&logoColor=white)

**Python · TensorFlow/Keras · CNNs (ResNet50, VGG16, MobileNetV2) · Kvasir Dataset**

---

## 🚀 Future Work

- [ ] Train on larger, multi-center clinical datasets for better generalization
- [ ] Add explainable AI (e.g., Grad-CAM) to highlight the image regions driving each prediction
- [ ] Explore hybrid ResNet + Transformer architectures
- [ ] Optimize for real-time deployment in clinical settings

---

## 📚 Citation

If you use this work, please cite:

```bibtex
@inproceedings{johnson2025endoscopic,
  title     = {Endoscopic Image-Based Deep Learning Approach for Predicting Gastrointestinal Diseases},
  author    = {Joel Johnson BV and K Martin Victor},
  booktitle = {IEEE Conference},
  year      = {2025},
  url       = {https://ieeexplore.ieee.org/abstract/document/11382902}
}
```

---

<div align="center">

⭐ If you find this project useful, please consider giving it a star!

</div>
