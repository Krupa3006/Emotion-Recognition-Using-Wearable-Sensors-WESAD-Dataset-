# Emotion Recognition Using Wearable Sensors (WESAD Dataset)

## Overview
This project implements an end-to-end emotion recognition system using wrist-worn wearable sensor data. The goal is to classify human emotional states based on physiological and motion signals using machine learning and deep learning techniques.

The system identifies four emotional states:
- Baseline / Neutral  
- Stress  
- Amusement  
- Relaxed / Meditation  

A hybrid approach combining time-series deep learning and feature-based modeling is used to achieve robust and generalizable performance.

---

## Dataset
- Dataset: WESAD (Wearable Stress and Affect Detection)
- Sensors (Wrist-based):
  - Accelerometer (ACC)
  - Blood Volume Pulse (BVP / PPG)
  - Electrodermal Activity (EDA)
  - Skin Temperature (TEMP)
- Subjects: 17 participants  
- Evaluation: Subject-independent testing on unseen users

---

## Methodology

### Data Preprocessing
- Noise reduction using band-pass and low-pass filtering
- Signal detrending and normalization
- Label alignment across different sensor sampling rates

### Window Segmentation
- 5-second sliding windows with 50% overlap
- Majority-vote labeling with purity threshold
- Ensures consistent emotional representation per window

### Feature Engineering
- Statistical features (mean, standard deviation, skewness, kurtosis)
- Frequency-domain features
- Physiological features derived from EDA, BVP, and temperature signals

### Model Architecture
- LSTM branch for temporal modeling of accelerometer data
- Dense neural network for handcrafted physiological features
- Feature fusion followed by Softmax classification

---

## Results
- Test Accuracy (Unseen Subject): ~97%
- Cross-Validation Accuracy: ~98.6%
- Evaluation Metrics:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Confusion Matrix

The model demonstrates strong generalization and stability across subjects, making it suitable for real-world wearable applications.

---

## Technologies Used
- Programming Language: Python
- Libraries: NumPy, Pandas, SciPy, Scikit-learn
- Deep Learning: TensorFlow, Keras
- Visualization: Matplotlib
- Techniques: Machine Learning, Time Series Analysis, Feature Engineering

---

## Applications
- Stress monitoring systems
- Mental health assessment tools
- Wearable-based health analytics
- Human-centered AI applications

---

## Author Contribution
- Model development and experimentation
- Feature engineering and evaluation
- Performance analysis and documentation

---

## License
This project is intended for academic and research purposes.
