## 1. Project Overview

This project focuses on **Human Activity Recognition (HAR)** using smartphone sensor data.
The goal is to classify **six human activities** based on signals recorded by a smartphone worn on the waist.

Activities:

1. Walking
2. Walking Upstairs
3. Walking Downstairs
4. Sitting
5. Standing
6. Lying
7. 
## 2. Dataset Description

* **Subjects:** 30 volunteers
* **Sensors Used:**

  * 3-axis Accelerometer
  * 3-axis Gyroscope
* **Sampling Rate:** 50 Hz
* **Window Size:** 2.56 seconds (128 readings per window)

Dataset Split:

* Training samples: 7,352
* Testing samples: 2,947
* Total samples: 10,299

Each sample contains **561 pre-extracted time and frequency domain features**.

---

## 3. Data Understanding & Preprocessing

Key steps:

* Studied dataset structure and activities
* Understood raw signals vs windowed features
* Checked missing values (none found)
* Explained timestamps and segmentation
* Prepared data for machine learning models

---

## 4. Classical Machine Learning Models

### Feature Engineering

Although the dataset already contains 561 features, we performed **additional feature engineering** by computing:

* Mean
* Standard Deviation
* Minimum
* Maximum
* Median
* Skewness
* Kurtosis
* Energy
* Zero-Crossing Rate

These **9 engineered features** were used as model input.

### Models Trained:

1. Logistic Regression
2. SVM (RBF Kernel)
3. Random Forest
4. XGBoost

### Best Classical Model:

* **XGBoost**
* Accuracy: **0.5632**
* ROC-AUC: **0.8965**

---

## 5. Fully Connected Neural Network (FCNN)

### Model Description:

* Input layer: 561 neurons
* Hidden layers: Fully connected (ReLU)
* Output layer: 6 neurons (Softmax)

### Training Details:

* Optimizer: Adam
* Loss Function: Categorical Cross-Entropy
* Epochs: Multiple passes over training data

### Results:

* **Accuracy:** 0.9437
* **Weighted F1-score:** 0.9436

### Observation:

FCNN significantly outperformed classical models by learning **complex non-linear relationships**.

---

## 6.  Recurrent Neural Networks (RNNs)

### Models Implemented:

1. Simple RNN
2. LSTM (Long Short-Term Memory)
3. GRU (Gated Recurrent Unit)

### Evaluation Metrics:

* Accuracy
* F1-score
* Confusion Matrix
* Training vs Validation Loss Curves

### Results Summary:

| Model      | Accuracy | Weighted F1 |
| ---------- | -------- | ----------- |
| Simple RNN | 0.4404   | 0.3866      |
| LSTM       | 0.6339   | 0.5590      |
| GRU        | 0.6624   | 0.6179      |

### Best Recurrent Model:

* **GRU** (highest accuracy among RNN-based models)

### Comparison with FCNN:

* FCNN Accuracy: **0.9437**
* Best RNN Accuracy (GRU): **0.6624**

---

## 7. Key Observations

* Classical ML models struggle with complex temporal patterns
* FCNN performs best when using full feature vectors
* RNN-based models perform better than Simple RNN but still below FCNN
* LSTM and GRU handle long-term dependencies better
* GRU is faster and more efficient than LSTM

---

## 8. How to Run the Code

1. Open Google Colab
2. Upload the notebook
3. Upload `UCI HAR Dataset.zip` when prompted
4. Run cells from top to bottom
5. Results and plots will be generated automatically

---

## 9. Conclusion

This project demonstrates the progression from classical machine learning to deep learning and recurrent models for time-series classification.

* **Best Overall Model:** FCNN
* **Best Recurrent Model:** GRU
* Deep learning methods clearly outperform classical approaches for HAR tasks

---

