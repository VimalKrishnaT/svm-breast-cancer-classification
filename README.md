# SVM Breast Cancer Classification

This project applies **Support Vector Machine (SVM)** models to classify tumor samples as **Malignant** or **Benign** using the Breast Cancer dataset.

## 📌 Features
- Load and preprocess the dataset (removing IDs, encoding target labels, scaling features).
- Train **Linear** and **RBF** SVM models.
- Visualize decision boundaries using **PCA** (2D projection).
- Tune hyperparameters **C** and **gamma** using **GridSearchCV**.
- Evaluate performance with **cross-validation** and hold-out test sets.

## 📂 Dataset
The dataset contains:
- **Features:** 30 numeric measurements of cell nuclei (radius, texture, perimeter, etc.).
- **Target:** 
  - `M` → Malignant (mapped to 1)
  - `B` → Benign (mapped to 0)
- **Source:** [UCI Machine Learning Repository - Breast Cancer Wisconsin Dataset](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29)

## ⚙️ Steps Implemented
1. **Load & Prepare Dataset**
   - Read CSV file
   - Drop `id` column
   - Encode target (`M` → 1, `B` → 0)
   - Train-test split with stratification
   - Standard scaling

2. **Train Models**
   - Linear kernel SVM
   - RBF kernel SVM

3. **Visualize Decision Boundaries**
   - Use **PCA** to project data into 2D
   - Plot decision regions for both kernels

4. **Hyperparameter Tuning**
   - `C` (margin penalty)
   - `gamma` (RBF kernel influence)
   - `GridSearchCV` with 5-fold cross-validation

5. **Model Evaluation**
   - Accuracy
   - Confusion matrix
   - Classification report
   - Cross-validation results

## 📊 Example Output
- **Linear SVM Test Accuracy:** ~96%
- **RBF SVM Test Accuracy:** ~98%
- Decision boundary plots in PCA space
