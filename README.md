# Iris Classification using Linear SVM (OvO)

## Objective
Build and evaluate a **Linear Support Vector Machine (SVM)** classifier using the **One-vs-One (OvO)** strategy on the Iris dataset.

---

## Dataset
- **Source:** Seaborn Iris dataset  
- **Samples:** 150  
- **Features:** Sepal length, sepal width, petal length, petal width  
- **Classes:** Setosa, Versicolor, Virginica  

---

## Workflow

### 1. Data Loading & Inspection
- Loaded dataset using Pandas
- Verified shape, sample rows, and class balance

### 2. Train/Test Split
- **85% training / 15% testing**
- Stratified split to preserve class distribution
- `random_state = 42` for reproducibility

### 3. Label Encoding
- Converted species labels to numeric form using `LabelEncoder`
- Required for SVM compatibility

### 4. Model Training
- Used **Linear SVM (SVC)**
- **One-vs-One (OvO)** multiclass strategy
- Hyperparameter tuning with **GridSearchCV (5-fold CV)**
- Tuned parameter: `C`

### 5. Model Evaluation
- Predictions made on test set
- Metrics used:
  - Accuracy
  - Confusion Matrix
  - Precision, Recall, F1-Score

---

## Results
- **Best C:** 1  
- **Cross-Validation Accuracy:** ~98.46%  
- **Test Accuracy:** **100%**
- Perfect classification across all three classes

---

## Tools & Libraries
- Python
- NumPy, Pandas
- Matplotlib, Seaborn
- Scikit-learn

---

## Conclusion
The Linear SVM with OvO strategy achieved **excellent performance** on the Iris dataset, demonstrating strong class separability and effective generalization.
