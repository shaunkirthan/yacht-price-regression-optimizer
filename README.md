# 🚤 Yacht Price Prediction using Optimized Linear Regression

Welcome to this project on **Yacht Price Prediction** built using a custom implementation of Linear Regression from scratch in Python. This project is focused on optimizing the regression process with a detailed approach to scaling, training, bias handling, rank checking, and convergence diagnostics.

---

## 📌 Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Key Features](#key-features)
- [Model Architecture](#model-architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Results & Visualization](#results--visualization)
- [Project Structure](#project-structure)
- [License](#license)

---

## 🚀 Project Overview

This project explores a **robust and detailed implementation of Linear Regression** for predicting yacht hydrodynamic resistance (a proxy for price/value) based on multiple input features such as **longitudinal position, prismatic coefficient, length-displacement ratio**, and more.

Rather than relying on Scikit-learn's abstraction, this project implements:
- Manual **feature scaling**
- **Bias addition**
- **Gradient Descent with convergence tracking**
- **Rank checking** to switch between Normal Equation & GD

It is ideal for understanding the mechanics of linear regression under-the-hood.

---

## 📊 Dataset

The dataset used is `yachtData.csv` (attached in the repository), originally from the UCI Machine Learning Repository. It contains 6 input features and 1 target variable.

**Attributes:**
1. Longitudinal position of the center of buoyancy
2. Prismatic coefficient
3. Length-displacement ratio
4. Beam-draught ratio
5. Length-beam ratio
6. Froude number
7. **Resistance** (Target Variable)

---

## 🔍 Key Features

- ✅ Custom Linear Regression (no external ML libraries)
- ⚙️ Supports both **Gradient Descent** and **Normal Equation** based on data characteristics
- 📉 Convergence using **epsilon threshold** and cost function tracking
- 📊 Error plots (RMSE vs. iterations)
- 🔍 Automatic bias addition
- 📐 Rank check for determining solution method
- ✨ Easily configurable learning rate, epochs, epsilon

---

## 🧠 Model Architecture

The logic determines whether to use **Normal Equation** (when full rank and low sample size) or **Gradient Descent**, based on:
- Matrix rank (`SVD`)
- Row-column ratio
- Dataset size

### 🚦 Gradient Descent Parameters:
- `alpha`: Learning rate
- `epsilon`: Convergence threshold
- `epochs`: Maximum iterations

---

## 🛠 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/yacht-price-regression-optimizer.git
   cd yacht-price-regression-optimizer
   ```

2. Install dependencies (if using a virtual environment):
   ```bash
   pip install -r requirements.txt
   ```

> **Note**: The code only uses `numpy`, `pandas`, `matplotlib`, and `sklearn` for data handling.

---

## ▶️ Usage

You can run the entire training and prediction pipeline using the provided script:

```python
python lab1_linear_regression.py
```

---

## 📈 Results & Visualization

The model plots the cost/error over training iterations when Gradient Descent is used, helping visualize convergence:

| Plot | Description |
|------|-------------|
| 📉 RMSE vs Epochs | Shows model learning and convergence |

![Example Plot](https://raw.githubusercontent.com/your-username/yacht-price-regression-optimizer/main/images/rmse_plot.png) *(Placeholder)*

---

## 🗂 Project Structure

```
yacht-price-regression-optimizer/
│
├── yachtData.csv                 # Dataset
├── lab1_linear_regression.py     # Main script (contains the model)
├── README.md                     # This file
├── images/
│   └── rmse_plot.png             # Optional plot to visualize learning
└── requirements.txt              # Python dependencies
```

---

## 📄 License

This project is licensed under the MIT License. Feel free to use, share, and contribute!

---

## 🙌 Acknowledgements

- UCI Machine Learning Repository
- Inspired by Andrew Ng’s ML lectures (Gradient Descent intuition)

