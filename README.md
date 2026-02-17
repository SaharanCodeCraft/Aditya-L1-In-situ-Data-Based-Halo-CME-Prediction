# 🌌 Real-Time Halo CME Prediction using SWIS-ASPEX (Aditya-L1)

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Machine Learning](https://img.shields.io/badge/Model-Random%20Forest-green.svg)
![Event](https://img.shields.io/badge/Event-Bharatiya%20Antariksh%20Hackathon%202025-orange.svg)
![Status](https://img.shields.io/badge/Status-Research%20Prototype-yellow.svg)

---

## 📖 Overview

This project was developed as part of the **Bharatiya Antariksh Hackathon 2025 (ISRO)**.

The objective is to predict **Halo Coronal Mass Ejections (CMEs)** in real time using *in-situ* particle and plasma measurements from the **SWIS-ASPEX payload onboard Aditya-L1**.

Unlike traditional CME detection approaches that rely on remote solar imaging, this system leverages time-series solar wind parameters to identify precursor signatures of Halo CMEs — enabling earlier and more reliable space weather alerts.

### Key Solar Wind Parameters Modeled

- Proton Density  
- Bulk Speed  
- Temperature  
- Dynamic Pressure  
- Plasma Gradients  
- Rolling-window statistical features  

This approach demonstrates potential for **30–60 minute early warning capability** for Earth-directed CMEs.

---

## 🎯 Problem Statement

Traditional CME detection systems:

- Depend on remote solar imaging  
- Detect events after propagation delay  
- Offer limited early-warning lead time  

### Proposed Approach

- Utilize time-aligned *in-situ* plasma measurements  
- Apply machine learning on engineered temporal features  
- Identify precursor signatures prior to CME impact  
- Improve operational space weather preparedness  

---

## 🧠 System Architecture

### Data Engineering Pipeline

- Unified multi-source datasets into **HDF5 format**
- Time-aligned solar wind parameter streams
- Rolling-window feature engineering:
  - Moving averages
  - Gradients
  - Dynamic pressure computation
- Anomaly handling
- Time-series continuity correction

### Machine Learning Framework

- Model: **Random Forest Classifier**
- Dataset Size: **1M+ labeled samples**
- Task: Binary classification (CME vs Non-CME)
- Optimization Focus: High-confidence quiet-period detection

---

## 🚀 Key Features

- End-to-end ML research pipeline
- Large-scale time-series handling using HDF5
- Rolling-window temporal feature extraction
- Robust anomaly detection and correction
- Modular and extensible architecture
- Research-driven experimental workflow

---

## 🛠 Tech Stack

### Programming Language
- Python

### Core Libraries
- NumPy
- pandas
- Scikit-learn
- h5py

### Model
- Random Forest Classifier

### Data Engineering
- HDF5 time-aligned storage
- Rolling-window statistical features
- Continuity and anomaly handling mechanisms

---

## 📊 Results

| Metric                  | Score |
|--------------------------|--------|
| Accuracy                 | ~80%  |
| Non-CME Recall           | 0.96  |
| CME Detection Recall     | 0.04  |
| Weighted F1 Score        | 0.72  |

---

## 📈 Performance Analysis

### Strengths

- High reliability in identifying quiet solar periods
- Strong filtering capability for non-CME conditions
- Stable overall classification performance

### Limitations

- Low CME sensitivity due to:
  - Severe class imbalance
  - Absence of deep temporal sequence modeling
  - Static classification threshold

This model serves as a robust baseline for improving real-time CME detection sensitivity.

---

## 🔬 Future Enhancements

- Address class imbalance (SMOTE / class weights / focal loss)
- Implement sequence-based models (LSTM / Temporal CNN / Transformers)
- Threshold optimization for improved CME recall
- Probabilistic confidence scoring
- Real-time streaming inference system
- Deployment as a space-weather early-warning API

---

## 🌍 Impact & Applications

Early detection of Halo CMEs can:

- Protect satellites from radiation damage  
- Safeguard electrical power grids  
- Improve global space weather forecasting systems  
- Enhance mission safety for space agencies  

This project establishes a data-driven foundation toward operational real-time CME prediction using in-situ plasma measurements.

---

## 👥 Contributors

- Jatin Khiyani  
- Samriddhi (SaharanCodeCraft)

---

## 📜 License

Developed for academic and hackathon purposes.
