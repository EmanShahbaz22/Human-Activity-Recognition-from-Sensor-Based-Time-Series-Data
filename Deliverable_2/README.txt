===========================================
README — Assignment 5.2  
Human Activity Recognition (HAR)  
===========================================

Student: Eman Shahbaz and Dua Sarwar 
Course: Machine Learning  
Assignment: 5.2 – Classical ML on Time-Series Data  
Dataset: UCI HAR Dataset  
Programming Environment: Google Colab (Python 3)
-------------------------------------------


1. PROJECT OVERVIEW
-------------------------------------------
This project focuses on Human Activity Recognition (HAR) using data from
smartphone accelerometer and gyroscope sensors. The goal is to classify 
six human activities using classical machine learning models.

The dataset contains pre-extracted features for each time-windowed signal.
We further engineered additional statistical features and trained four ML
models:

1) Logistic Regression  
2) Support Vector Machine (RBF Kernel)  
3) Random Forest  
4) XGBoost  

Model performance was evaluated using Accuracy, Precision, Recall,
F1-score, Confusion Matrix, and ROC-AUC.


2. DATASET DESCRIPTION
-------------------------------------------
Dataset: UCI Human Activity Recognition Using Smartphones  
Link: https://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones

Activities (labels 0–5):
0 = Walking  
1 = Walking Upstairs  
2 = Walking Downstairs  
3 = Sitting  
4 = Standing  
5 = Lying  

Dataset Size:
- Training: 7352 samples  
- Testing: 2947 samples  
- Features: 561 per sample  


3. PREPROCESSING AND FEATURE ENGINEERING
-------------------------------------------
The dataset contains pre-extracted time-domain and frequency-domain features.  
Additional engineered features were created from each sample:

- Mean  
- Standard Deviation  
- Minimum  
- Maximum  
- Median  
- Skewness  
- Kurtosis  
- Energy  
- Zero-Crossing Rate  

These 9 new features were used as input for the machine learning models.

StandardScaler was applied for normalization.  
Labels were shifted from 1–6 to 0–5 for compatibility with XGBoost.


4. MODELS TRAINED
-------------------------------------------
The following models were implemented:

1) Logistic Regression  
   - multi_class = multinomial  
   - solver = lbfgs  

2) SVM (RBF Kernel)  
   - kernel = rbf  
   - probability = True  

3) Random Forest  
   - n_estimators = 200  

4) XGBoost  
   - n_estimators = 200  
   - learning_rate = 0.1  
   - max_depth = 4  
   - objective = multi:softprob  

Evaluation metrics included:
- Accuracy  
- Precision  
- Recall  
- F1-score  
- ROC-AUC  
- Confusion Matrix  
- Classification Report  


5. RESULTS SUMMARY
-------------------------------------------
Final performance scores (extracted from output):

Model                  | Accuracy | Precision | Recall | F1-score | ROC-AUC
---------------------- | -------- | --------- | ------ | -------- | --------
Logistic Regression    | 0.5541   | 0.5535    | 0.5541 | 0.5492   | 0.8837
SVM (RBF Kernel)       | 0.5507   | 0.5516    | 0.5507 | 0.5408   | 0.8864
Random Forest          | 0.5467   | 0.5463    | 0.5467 | 0.5442   | 0.8901
XGBoost (Best Model)   | 0.5632   | 0.5623    | 0.5632 | 0.5585   | 0.8965

Best Overall Model: **XGBoost**  
Reason: Highest accuracy, F1-score, and ROC-AUC.


6. FILE STRUCTURE
-------------------------------------------
Your Colab Notebook contains the following:

- Data loading
- ZIP upload and extraction
- Feature engineering
- Scaling
- Model training
- Evaluation (metrics + confusion matrices)
- Final comparison table


7. HOW TO RUN THE CODE
-------------------------------------------
1. Upload the "UCI HAR Dataset.zip" to Google Colab when prompted.
2. Run the notebook from top to bottom.
3. All models will train automatically.
4. Final comparison table will be printed at the end.


8. CONCLUSION
-------------------------------------------
This assignment demonstrates how classical machine learning techniques 
perform on time-series activity recognition tasks. Although deep learning 
can achieve higher accuracy, classical models with engineered features 
provide solid performance and valuable learning experience.

XGBoost was the best-performing model in this project, achieving:
- Highest accuracy: 0.5632  
- Highest F1-score: 0.5585  
- Highest ROC-AUC: 0.8965  

-------------------------------------------
END OF README
-------------------------------------------
