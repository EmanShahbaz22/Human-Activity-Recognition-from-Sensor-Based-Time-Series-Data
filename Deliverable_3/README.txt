===========================================
README — Assignment 5.3
Human Activity Recognition (Deep Learning)
===========================================

Students:
Eman Shahbaz
Dua Sarwar

Course: Machine Learning
Assignment: 5.3
Dataset: UCI HAR Dataset
Programming Environment: Google Colab (Python 3)

-------------------------------------------
1. PROJECT OVERVIEW
-------------------------------------------
This project implements a Fully Connected Neural Network (FCNN)
for Human Activity Recognition using smartphone sensor data.

The goal is to classify six human activities using deep learning
and compare performance with classical ML models from Assignment 5.2.

-------------------------------------------
2. DATASET
-------------------------------------------
Dataset: UCI Human Activity Recognition Using Smartphones

Activities:
1 = Walking
2 = Walking Upstairs
3 = Walking Downstairs
4 = Sitting
5 = Standing
6 = Lying

Samples:
- Training: 7352
- Testing: 2947
- Features: 561 per sample

-------------------------------------------
3. MODEL USED
-------------------------------------------
- Fully Connected Neural Network (FCNN)
- Optimizer: Adam
- Loss: Categorical Cross-Entropy
- Output: Softmax (6 classes)

-------------------------------------------
4. RESULTS
-------------------------------------------
Test Accuracy: 0.9437
Weighted F1-score: 0.9436

The FCNN significantly outperforms classical ML models.

-------------------------------------------
5. COMPARISON WITH 5.2
-------------------------------------------
Best Classical ML (XGBoost) Accuracy: 0.5632
FCNN Accuracy: 0.9437

-------------------------------------------
6. HOW TO RUN
-------------------------------------------
1. Upload the UCI HAR Dataset ZIP file.
2. Run the notebook from top to bottom.
3. Model will train and evaluate automatically.
4. Results and confusion matrix will be displayed.

-------------------------------------------
END OF README
-------------------------------------------
