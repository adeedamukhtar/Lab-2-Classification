# Dry Bean Classification using Machine Learning

##  Project Overview

This project focuses on the classification of **Dry Bean types** using supervised machine learning algorithms. The dataset contains **17 numerical features** extracted from bean images and is used to train and evaluate classification models like **Logistic Regression**, **k-Nearest Neighbors (k-NN)**, and **Decision Trees**.

---

##  Key Features

- Multiclass classification with 7 dry bean types
- Comprehensive data preprocessing
- Model performance comparison using multiple metrics
- Scikit-learn pipelines for clean, reusable ML workflows

---

## Dataset Information

- Source: UCI Machine Learning Repository  
- Samples: `13,611` dry bean samples  
- Features: `16` numerical attributes related to shape, geometry, and texture  
- Target: `Class` — one of the following:
  - **SEKER**
  - **BARBUNYA**
  - **BOMBAY**
  - **CALI**
  - **DERMASON**
  - **HOROZ**
  - **SIRA**

### Sample Features:
- `Area`, `Perimeter`, `MajorAxisLength`, `MinorAxisLength`
- `Eccentricity`, `Solidity`, `Extent`, `Compactness`
- Shape Factors (`ShapeFactor1` to `ShapeFactor4`)

---

##  Methodology Highlights

###  Data Loading & Cleaning
- Loaded dataset from `Dry_Bean_Dataset.xlsx`
- Verified class distribution
- Ensured data integrity and correct data types

###  Exploratory Data Analysis
- Visualized class distribution and feature relationships
- Identified potential feature importance and separability

### Feature & Target Preparation
- Input features `X`: All 16 numerical columns
- Target variable `y`: Bean `Class` (converted to categorical labels)

### Data Splitting
- Split into **80% training** and **20% testing** sets using `train_test_split` with `stratify=y` to preserve class balance

---

## Model Building & Evaluation

Three classification models were evaluated:

### 1️  Logistic Regression
- Linear classifier with regularization
- Good baseline with solid performance

### 2️  k-Nearest Neighbors (k-NN)
- Distance-based algorithm
- Performed well but slower for large datasets

### 3️  Decision Tree Classifier
- Tree-based model that handles non-linear boundaries
- Tended to overfit slightly without pruning

---

## Performance Evaluation

Evaluated using Accuracy, Precision, Recall, and F1 Score:

| Model               | Accuracy | Precision | Recall | F1 Score |
|---------------------|----------|-----------|--------|----------|
| Logistic Regression | 0.9266   | 0.9393    | 0.9369 | 0.9379   |
| k-NN                | 0.9232   | 0.9395    | 0.9344 | 0.9367   |
| Decision Tree       | 0.8928   | 0.9069    | 0.9072 | 0.9070   |

---

##  Key Takeaways

- **Logistic Regression** and **k-NN** performed best with accuracy above 92%
- **Decision Tree** showed decent performance but was slightly less reliable due to possible overfitting
- Proper scaling (e.g., StandardScaler) improved model performance, especially for distance-based methods like k-NN


