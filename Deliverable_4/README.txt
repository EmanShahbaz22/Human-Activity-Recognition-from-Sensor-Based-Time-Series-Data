===========================================
README — Assignment 5.4
Human Activity Recognition (RNN / LSTM / GRU)
===========================================

Team Members:
Eman Shahbaz (BITF22M516)
Dua Sarwar (BITF22M530)

Course: Machine Learning
Assignment: 5.4
Dataset: UCI Human Activity Recognition Using Smartphones
Programming Environment: Google Colab (Python 3)

-------------------------------------------
1. OBJECTIVE
-------------------------------------------
To implement recurrent neural network based classification
for time-series sensor data and evaluate Simple RNN,
LSTM, and GRU models.

-------------------------------------------
2. DATASET & INPUT FORMAT
-------------------------------------------
Raw inertial sensor signals were used from the
"Inertial Signals" folder of the UCI HAR dataset.

Each sample is represented as:
(samples, timesteps, features) = (N, 128, 6)

Features:
- Accelerometer X, Y, Z
- Gyroscope X, Y, Z

-------------------------------------------
3. PREPROCESSING
-------------------------------------------
- Conversion of data to 3D format for sequential learning
- Per-channel normalization using training statistics
- Labels converted from 1–6 to 0–5

-------------------------------------------
4. MODELS IMPLEMENTED
-------------------------------------------
1) Simple RNN
2) LSTM
3) GRU

All models use:
- Adam optimizer
- Sparse categorical cross-entropy loss
- Softmax output layer

-------------------------------------------
5. EVALUATION METRICS
-------------------------------------------
For each model:
- Accuracy
- Weighted F1-score
- Confusion Matrix
- Training vs Validation loss curves

-------------------------------------------
6. RESULTS SUMMARY
-------------------------------------------
Simple RNN: Accuracy = 0.44
LSTM:       Accuracy = 0.63
GRU:        Accuracy = 0.66 (Best RNN)

-------------------------------------------
7. COMPARISON WITH ASSIGNMENT 5.3
-------------------------------------------
The best recurrent model (GRU) was compared with
the Fully Connected Neural Network (FCNN) from
Assignment 5.3.

FCNN achieved higher accuracy due to the use of
engineered features.

-------------------------------------------
8. HOW TO RUN
-------------------------------------------
1. Upload "UCI HAR Dataset.zip" when prompted.
2. Run the notebook from top to bottom.
3. Metrics, plots, and comparison tables will be displayed.

-------------------------------------------
END OF README
-------------------------------------------
