#  Sepsis Prediction - End-to-End ML Project

This project focuses on building an end-to-end machine learning pipeline for predicting **Sepsis** using patient vital signs and lab measurements. The solution is developed with real-time clinical applications in mind, leveraging the power of machine learning to detect sepsis early and assist in critical care decision-making.

---

##  Problem Statement

Sepsis is a life-threatening condition caused by the body's extreme response to infection. Early detection is crucial to reduce mortality. This project predicts the onset of sepsis using patient clinical data collected over time in the ICU.

---

##  Project Pipeline

### 1.  Data Ingestion
- Raw data is collected from hospital records.
- The data is loaded into the pipeline for further processing.

### 2.  Data Validation
- Checks for:
  - Missing values
  - Duplicates
  - Invalid column types
  - Statistical summaries for sanity checks

### 3.  Data Transformation
- Time-based filling (`backfill`, `forward-fill`)
- Feature engineering (e.g., combining `Unit1` and `Unit2` into a `Unit` feature)
- Label encoding, scaling
- Feature selection
- Dropping redundant and noisy columns

### 4.  Model Training
- Model used: `Random Forest Classifier`
- Trained using:
  - K-fold cross-validation
  - Precision, Recall, F1-score metrics
  - - `MLflow` used to track experiments

### 5.  Model Evaluation
- Evaluation on a test dataset from a different hospital
- Classification report and confusion matrix
- ROC AUC and other performance metrics

### 6.  MLOps Integration
- Trained model saved using `joblib`
- `MLflow` for model tracking
- `Docker` used to containerize the entire project
- `Flask` app for user interaction with the model
- API endpoint created to accept patient data and return sepsis predictions

---
## 🧑‍💻 Tech Stack

| Purpose             | Tools Used                                  |
|---------------------|----------------------------------------------|
| Data Handling       | Pandas, NumPy                                |
| Modeling            | Scikit-learn, RandomForest                   |
| Tracking            | MLflow                                       |
| Deployment          | Flask, Docker                                |
| Evaluation          | Scikit-learn Metrics, Matplotlib, Seaborn    |

---


