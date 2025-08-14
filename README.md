# SVM Binary Classification on Breast Cancer Dataset

## 📌 Overview
This project demonstrates **Support Vector Machine (SVM)** classification on the Breast Cancer dataset.  
We train models using both **Linear** and **RBF kernels**, visualize decision boundaries for 2D feature space, and perform **hyperparameter tuning** with cross-validation.

---

## 📂 Dataset
- **Source**: Provided CSV file (`Breast Cancer.csv`)
- **Target Variable**: `diagnosis` (`M` = Malignant, `B` = Benign)
- **Features Used for Visualization**:  
  - `radius_mean`  
  - `texture_mean`

---

## ⚙️ Steps Performed

1. **Data Loading & Cleaning**
   - Removed unnecessary columns: `id`, `Unnamed: 32`
   - Encoded target variable: `M=1`, `B=0`

2. **Feature Scaling**
   - Applied `StandardScaler` for normalization.

3. **Model Training**
   - **SVM with Linear Kernel**
   - **SVM with RBF Kernel**

4. **Decision Boundary Visualization**
   - Plotted decision boundaries in 2D space using selected features.

5. **Hyperparameter Tuning**
   - Used `GridSearchCV` to optimize:
     - `C` → Regularization parameter
     - `gamma` → Kernel coefficient
   - Best parameters found:  
     ```
     C = 10
     gamma = 0.1
     kernel = rbf
     ```

6. **Evaluation**
   - **Best CV Accuracy** (GridSearch): ~90.11%
   - **Mean CV Accuracy** (Final Model): ~89.63%

---

## 📊 Results

| Kernel   | CV Accuracy | Notes |
|----------|------------|-------|
| Linear   | ~89%       | Simpler decision boundary |
| RBF      | ~90%       | Captures nonlinear patterns |

---

## 🖼 Decision Boundary Visualizations
- **Linear Kernel** – Straight separation line.
- **RBF Kernel** – Flexible curves fitting complex data patterns.

---

## 🛠 Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

---

## 🚀 How to Run
```bash
pip install pandas numpy matplotlib scikit-learn
python svm_classification.py
