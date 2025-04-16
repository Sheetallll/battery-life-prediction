# 🔋 Battery Life Prediction using Machine Learning

A machine learning-based project to forecast the degradation and remaining useful life (RUL) of lithium-ion batteries using **Artificial Neural Networks (ANN)** and **Extreme Gradient Boosting (XGBoost)**. This project is built on a well-curated dataset from NASA and focuses on developing reliable models for real-time Battery Management Systems (BMS).

---

## 📄 Abstract

Accurate battery life prediction is essential in the modern energy landscape. This project compares the performance of ANN and XGBoost using key battery cycle data, such as voltage, current, temperature, and discharge capacity. Results show the potential of both models in predicting remaining capacity, with XGBoost slightly outperforming ANN in handling late-cycle degradation.

---

## 📚 Table of Contents

- [Introduction](#introduction)
- [Methodology](#methodology)
  - [Design](#design)
  - [Algorithms Used](#algorithms-used)
  - [Preprocessing](#preprocessing)
  - [Evaluation Metrics](#evaluation-metrics)
- [Case Study](#case-study)
- [Results](#results)
- [Conclusion](#conclusion)
- [Authors](#authors)

---

## 🧠 Introduction

Battery degradation forecasting is vital for electric vehicles, medical devices, and portable electronics. Traditional physics-based models often fail to generalize. This project explores data-driven approaches using machine learning to overcome such limitations.

---

## ⚙️ Methodology

### 📐 Design

The aim is to predict:
- Remaining capacity of a battery
- Number of cycles left before end-of-life

### 🧮 Algorithms Used

#### 1. Artificial Neural Network (ANN)
- Feedforward architecture with 5 layers (256 → 128 → 64 → 32 → 1)
- ReLU activations
- Dropout for regularization
- Trained with Adam optimizer and MSE loss

#### 2. Extreme Gradient Boosting (XGBoost)
- Ensemble of decision trees
- Tuned hyperparameters: `n_estimators=300`, `max_depth=6`, `learning_rate=0.05`
- Excellent at feature importance and structured data

### 🧹 Preprocessing

- Removed anomalous data and nulls
- Handled missing values with feature-wise means
- Label encoding for categorical features
- MinMax normalization
- Stratified split: 80% train / 20% test

### 📏 Evaluation Metrics

- **MAE (Mean Absolute Error)**
- **MSE (Mean Squared Error)**

---

## 🧪 Case Study

### 📊 Dataset

- NASA Battery Data Set
- Includes time-series measurements (voltage, current, temperature, etc.)
- End-of-life defined as capacity falling below threshold
- Feature engineering applied (e.g., delta capacity, temperature trends)

### 🤖 Models in Action

- **ANN:** Smooth capacity degradation predictions over time
- **XGBoost:** Captures sharp capacity drops and late-cycle trends

---

## 📈 Results

| Model     | MAE (%) | MSE    |
|-----------|---------|--------|
| XGBoost   | **6.13**  | **81.29** |
| ANN       | 6.31    | 83.91  |

- **XGBoost**: More accurate for sharp degradation patterns
- **ANN**: Better at modeling smooth and continuous decay

---

## ✅ Conclusion

This project validates the effectiveness of machine learning in battery life forecasting. While both models perform well, **XGBoost** slightly edges out **ANN** in accuracy. ANN, however, excels at producing smoother predictions. Future enhancements may include hybrid models like **LSTMs** for even better time-series learning and integration into real-time BMS platforms.

---

## 👥 Authors

- **Sheetal Lodhi**  
- **Aindrila Kundu**  
- **Vikash Kumar Vivek**  
- **Lakshya Pal**  


---
