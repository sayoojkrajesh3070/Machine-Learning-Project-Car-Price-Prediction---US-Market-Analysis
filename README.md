# 🏎️ Car Price Prediction - US Market Analysis

### **Project Overview**
This project was developed to help a Chinese automobile manufacturer understand the competitive landscape of the US auto market. By building and evaluating multiple regression models, we identify the key technical and physical attributes that drive car prices.

---

### **1. Data Preprocessing & Cleaning**
A robust preprocessing pipeline was implemented to ensure data quality:
* **Brand Normalization**: Fixed inconsistent naming (e.g., corrected 'maxda' to 'mazda', 'vw' to 'volkswagen', and 'toyouta' to 'toyota').
* **Feature Selection**: Extracted brand names from the `CarName` column and removed unique identifiers.
* **Pipeline Integration**: Used `StandardScaler` for numerical scaling and `OneHotEncoder` for categorical feature transformation to prevent data leakage.

---

### **2. Model Implementation & Evaluation**
We implemented five regression algorithms to find the most accurate pricing tool.



#### **Performance Comparison**
| Model | R-squared ($R^2$) | Mean Absolute Error (MAE) |
| :--- | :--- | :--- |
| **Random Forest Regressor** | **0.9567** | **$1,309** |
| Gradient Boosting Regressor | 0.9279 | $1,666 |
| Decision Tree Regressor | 0.9063 | $1,785 |
| Support Vector Regressor (SVR) | 0.0956 | $4,893 |
| Linear Regression | -1.50e+22 | N/A |

**Key Finding**: The **Random Forest Regressor** is the best performing model, explaining **95.6%** of the price variance.

---

### **3. Significant Variables (Feature Importance)**
The analysis revealed that the following features have the most significant impact on a car's market value:



1. **Engine Size**: The primary driver of cost and market positioning.
2. **Curb Weight**: Highly correlated with vehicle size and segment.
3. **Highway MPG**: A critical factor for the economy and mid-range segments.
4. **Horsepower**: A key indicator of performance and luxury.

---

### **4. Hyperparameter Tuning**
We performed a `GridSearchCV` on the top-performing models. While the default Random Forest configuration was highly accurate, the tuning process ensured the model is generalized and robust against overfitting for future data entries.

---

### **5. Technologies Used**
* **Python** (Pandas, NumPy)
* **Scikit-Learn** (Pipelines, GridSearchCV, Metrics)
* **Matplotlib & Seaborn** (Data Visualization)
* **Jupyter Notebook**

---
