# Dry Bean Classification Project

## Project Overview
This project aims to classify different varieties of dry beans based on their physical characteristics. The dataset contains 13,611 records with 16 numeric shape features extracted from bean images and a target label indicating the bean variety (7 classes).

The following models were implemented and evaluated for this classification task:

- Logistic Regression  
- k-Nearest Neighbors (k-NN)  
- Decision Tree Classifier  

Each model was trained using robust preprocessing pipelines and evaluated using comprehensive classification metrics.

---

## Key Features
- Implemented in Python using scikit-learn  
- Standardized preprocessing with `ColumnTransformer` and `StandardScaler`  
- Target variable encoded with `LabelEncoder` for multiclass classification  
- Performance evaluation with `classification_report` (Accuracy, Precision, Recall, F1-score)  

---

## Dataset Summary
- **Total Records:** 13,611  
- **Features:** 16 numeric shape descriptors (Area, Perimeter, Eccentricity, etc.)  
- **Target Classes:** 7 bean varieties (e.g., SEKER, BARBUNYA, BOMBAY, etc.)  

---

## Data Preprocessing
- Data loading performed using `pandas.read_excel()`  
- Target labels transformed from strings to integers via `LabelEncoder`  
- Features standardized using `StandardScaler` for improved model training  
- Dataset split into 80% training and 20% testing sets with stratification to maintain class distribution  

---

## Models and Evaluation
Each classification model was wrapped in a scikit-learn Pipeline that combined preprocessing and the classifier itself. The models were evaluated on the test set with the following metrics:

| Model               | Accuracy | Precision (Macro) | Recall (Macro) | F1 Score (Macro) |
|---------------------|----------|-------------------|----------------|------------------|
| Logistic Regression  | 0.9265   | 0.9393            | 0.9369         | 0.9379           |
| k-Nearest Neighbors  | 0.9232   | 0.9395            | 0.9344         | 0.9367           |
| Decision Tree       | 0.8928   | 0.9069            | 0.9072         | 0.9070           |

---

## Insights
- Logistic Regression and k-NN showed the best overall performance, achieving over 92% accuracy and strong macro-averaged F1 scores.  
- Decision Tree achieved slightly lower accuracy, possibly due to overfitting in certain classes.  
- Feature standardization was critical in improving model convergence and accuracy.  
- Macro-averaged metrics effectively accounted for class imbalance, providing a balanced evaluation across all classes.  

---

## Methodology Summary
- **Preprocessing Pipeline:** StandardScaler applied to all features  
- **Model Integration:** Each classifier integrated into a pipeline for seamless preprocessing and prediction  
- **Evaluation:** Utilized `classification_report()` for detailed metrics and model comparison  
- **Reproducibility:** Random state fixed during train-test split and model training to ensure consistent results  

---

## Citation
Özguven, M. M., & Ege University, Department of Computer Engineering. (2015). *Dry Bean Dataset*. UCI Machine Learning Repository. https://archive.ics.uci.edu/ml/datasets/Dry+Bean+Dataset

---

