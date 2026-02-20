# 🧠 Image Classification with CNN — CIFAR-10

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow)
![Keras](https://img.shields.io/badge/Keras-Deep%20Learning-red?logo=keras)
![Dataset](https://img.shields.io/badge/Dataset-CIFAR--10-green)

## 📌 Project Overview

This project implements a **Convolutional Neural Network (CNN)** for automatic image classification using the **CIFAR-10** dataset. The model is capable of identifying 10 object categories with high accuracy, leveraging modern regularization techniques and data augmentation to optimize performance.

## 🎯 Objective

Design and train a computer vision model using a deep CNN architecture, evaluating its generalization capability on unseen images from the CIFAR-10 benchmark dataset.

## 🗂️ Dataset Classes

| ID | Class        |
|----|--------------|
| 0  | Airplane ✈️  |
| 1  | Automobile 🚗 |
| 2  | Bird 🐦      |
| 3  | Cat 🐱       |
| 4  | Deer 🦌      |
| 5  | Dog 🐶       |
| 6  | Frog 🐸      |
| 7  | Horse 🐴     |
| 8  | Ship 🚢      |
| 9  | Truck 🚚     |

## 🏗️ Model Architecture

The CNN is inspired by the **VGG-Net** architecture, featuring three convolutional blocks with progressively larger filters (64 → 128 → 256), followed by fully connected dense layers.

Each block includes:
- Two `Conv2D` layers with `ReLU` activation and `He Normal` initialization
- `L2` regularization to reduce overfitting
- A `MaxPooling` layer for dimensionality reduction
- `BatchNormalization` to stabilize training

The output layer uses `Softmax` for multi-class classification across the **10 CIFAR-10 categories**.

**Total parameters:** ~1.68 million

## ⚙️ Training Configuration

| Parameter        | Value                          |
|-----------------|-------------------------------|
| Optimizer        | Adam                           |
| Learning Rate    | 0.0001                         |
| Loss Function    | Sparse Categorical Crossentropy |
| Regularization   | L2 (0.001)                     |
| Initialization   | He Normal                      |
| Callbacks        | EarlyStopping                  |

## 🔧 Techniques Applied

- ✅ **Batch Normalization** — stabilizes and accelerates training
- ✅ **Dropout** — reduces overfitting (rates: 0.2 and 0.3)
- ✅ **L2 Regularization** — penalizes large weights
- ✅ **Data Augmentation** — rotation, horizontal flip, zoom, and shift
- ✅ **EarlyStopping** — halts training when validation loss stops improving

## 📁 Project Structure

```
📦 CNN-CIFAR10
 ┣ 📓 Vision por computador Cifar10.ipynb   ← Main notebook
 ┣ 📄 README.md                              ← This file
```

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
   ```

2. Install dependencies:
   ```bash
   pip install tensorflow numpy matplotlib
   ```

3. Open the notebook:
   ```bash
   jupyter notebook "Vision por computador Cifar10.ipynb"
   ```

4. Run cells in order.

## 📦 Requirements

```
tensorflow >= 2.0
numpy
matplotlib
```

## 👤 Author

**Gianpier Giandoni**
Project developed as part of the **Computer Vision** course at [Nuclio Digital School](https://nuclio.school).
