# 🎓 Student Performance Prediction using Random Forest

This project predicts student final grades based on various features like demographic information, family background, and school support. It utilizes the Random Forest Regression algorithm from scikit-learn to train and evaluate the model.

---

## 📁 Dataset

The dataset used is `studentPerformance.csv`, containing student information and their grades (G1, G2, G3).

### Sample Features:
- `sex`, `age`, `Pstatus`, `Medu`, `Fedu`, `Mjob`, `Fjob`
- `studytime`, `failures`, `schoolsup`, `famsup`, `internet`, etc.
- `G1`, `G2`, `G3`: First, second, and final period grades

---

## 🧪 Workflow

### 1. **Data Preprocessing**
- Loaded data with pandas
- Removed missing values
- Created a new target column `G`: average of `G1`, `G2`, `G3`
- Encoded categorical variables (e.g., `sex`, `Mjob`, `internet`) using numerical mappings

### 2. **Feature Selection**
- Selected relevant features into `X`
- Target variable: `G` (average grade)

### 3. **Model Training**
- Split data into train/test (80/20)
- Used `RandomForestRegressor` with 175 estimators
- Trained the model on training data

### 4. **Evaluation**
- Metrics:
  - **Mean Squared Error (MSE)**
  - **Mean Absolute Error (MAE)**
- Compared predictions to actual grades

---

## 📈 Results

Example output:
```
Mean Squared Error: [your_MSE_value]
Mean Absolute Error: [your_MAE_value]
```

These values represent the average squared and absolute difference between the predicted and actual grades, respectively.

---

## 📦 Requirements

Install dependencies using pip:

```bash
pip install pandas scikit-learn
```

---

## 🚀 Run the Notebook

1. Ensure `studentPerformance.csv` is in the same directory.
2. Open the `.ipynb` file with Jupyter Notebook or JupyterLab.
3. Run all cells sequentially.

---

## 📚 Future Improvements

- Hyperparameter tuning with `GridSearchCV`
- Feature engineering (interaction terms, binning)
- Support for additional models (e.g., XGBoost, SVR)

---

