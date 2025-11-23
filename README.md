# 🏋️‍♂️ Fitness Tracker — Time-Series Activity Classification & Rep Counting

A machine learning project that classifies exercise movements using raw accelerometer and gyroscope data — and automatically counts repetitions with high accuracy.  
Built from scratch using signal processing, feature engineering, and multiple ML models.

---

## 📌 Project Overview

This project analyzes wearable-sensor time-series data (accelerometer + gyroscope) to:

1. **Classify 6 different exercise movements**
2. **Count the number of repetitions performed**
3. **Visualize raw and processed sensor signals**
4. **Evaluate multiple ML models and feature-engineering approaches**

It was designed as an independent exploration into time-series modeling, classical ML, and algorithmic signal analysis.

---

## 🚀 Key Features

### **🔧 1. Feature Engineering**
Implemented a full preprocessing and feature-engineering pipeline:
- Low-pass filtering to smooth noisy sensor readings  
- Fourier Transform for frequency-domain features  
- PCA for dimensionality reduction  
- Clustering to reveal patterns across movements  
- Custom signal features (peaks, magnitude, smoothness, periodicity)

---

### **📈 2. Machine Learning Models**
Evaluated and compared:
- Random Forest  
- Support Vector Machine  
- Neural Network  
- KNN  
- Naive Bayes  

Performed:
- Grid search  
- Feature-set experiments  
- Train/test evaluation  

**Best model:** Random Forest  
**Accuracy:** **99.46%**

---

### **🔁 3. Rep Counting Algorithm**
Designed a custom algorithm combining:
- Smoothed peak detection  
- Axis-wise signal thresholds  
- Movement-specific rules  
- Temporal consistency checks  

**Performance:**  
**MAE = 0.88 reps** (on average, <1 rep off from ground truth)

---

### **📊 4. Visualization Pipeline**
Automatically generates:
- Time-series plots for every participant × movement  
- Side-by-side accelerometer & gyroscope comparisons  
- Signal smoothness and peak patterns  
- PCA scatter plots for cluster inspection

This made the ML pipeline interpretable and helped validate that the model learned meaningful structure.

---

## 🗂️ Project Structure
```
📁 fitness-tracker/
│
├── data/
│ ├── raw/ # Unprocessed sensor data
│ └── processed/ # Filtered + engineered features
│
├── notebooks/
│ ├── 01_data_processed.ipynb
│ ├── 02_outliers_removed_chauvenets.ipynb
│ └── 03_data_features.ipynb
│
├── src/
│ ├── LearningAlgorithms.py
│ ├── visualize.py
│ ├── remove_outliers.py
│ ├── build_features.py
│ └── rep_counter.py
│
└── README.md
```

---

## 🛠️ Tech Stack

- **Python**
- numpy, pandas  
- scikit-learn  
- scipy  
- matplotlib, seaborn  
- statsmodels  
- peakutils / custom peak detection functions  

---

## 📚 What I Learned

- How to extract meaningful structure from noisy time-series data  
- Why filtering + frequency analysis matter in wearable-sensor modeling  
- How different ML models behave with correlated multiaxis data  
- How to design a practical algorithm (rep counting) beyond just classification  
- How to validate model decisions using visualization  

This project pushed me to think like both a data scientist *and* an engineer building a real product.

---

## 🎯 Potential Real-World Applications

- Smart fitness tracking apps  
- Gym analytics for form/rep detection  
- Wearable health monitoring  
- Personalized exercise recommendations  

This project was more than a class assignment — it’s a foundational prototype for something that could become a **real-world product**.

---

## ✨ Acknowledgements

Special thanks to the open-source community for the tools and libraries that made this project possible.

---

