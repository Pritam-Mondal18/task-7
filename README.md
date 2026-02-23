# Support Vector Machines (SVM) – Analysis

## Step 1: Dataset Preparation for Binary Classification
The Breast Cancer dataset was used for binary classification.

- The target variable (diagnosis) was converted into numeric form:
  - Malignant → 1
  - Benign → 0
- Feature scaling was applied using StandardScaler to normalize feature values.

**Observation:**
SVM is sensitive to feature scale, so normalization improves performance and convergence.

---

## Step 2: Training SVM with Linear and RBF Kernel

Two SVM models were trained:

### Linear Kernel
- Works well when data is linearly separable.
- Finds a straight decision boundary (hyperplane).

### RBF Kernel (Radial Basis Function)
- Handles non-linear relationships.
- Uses kernel trick to map data into higher-dimensional space.

**Observation:**
RBF kernel usually performs better when data is not linearly separable.

---

## Step 3: Decision Boundary Visualization (2D Data)

To visualize classification behavior, only two features were used.

**Observation:**
- Decision boundary shows how SVM separates classes.
- Linear SVM produces straight boundary.
- RBF SVM produces curved boundary.

Visualization helps understand margin and class separation.

---

## Step 4: Hyperparameter Tuning (C and Gamma)

### Parameter C
Controls trade-off between:
- Large margin
- Classification error

Small C → wider margin, more tolerance  
Large C → narrow margin, less tolerance

---

### Parameter Gamma (RBF only)
Controls influence of individual data points.

Small gamma → smoother boundary  
Large gamma → complex boundary (risk of overfitting)

GridSearchCV was used to find optimal values.

---

## Step 5: Cross-Validation Evaluation

Cross-validation was used to evaluate model performance across multiple splits.

**Benefits:**
- More reliable accuracy estimate
- Reduces bias from single train-test split
- Helps detect overfitting

---

## Final Conclusion

- SVM is a powerful classifier that maximizes margin between classes.
- Linear kernel works for simple separable data.
- RBF kernel handles complex patterns.
- Hyperparameter tuning significantly improves performance.
- Cross-validation ensures robust evaluation.

SVM is effective for high-dimensional datasets and provides strong generalization performance.
