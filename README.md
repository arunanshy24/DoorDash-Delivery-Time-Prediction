# ⏱️ DoorDash Delivery Time Prediction

> A comparative machine learning study to build and evaluate regression models for accurately predicting the total duration of food delivery orders.

---

## 📝 Table of Contents
- [About the Project](#about-the-project)
- [Key Findings & Best Model](#key-findings--best-model)
- [Methodology & Models](#methodology--models)
- [Data Source](#data-source)

---

## 💡 About the Project

This project focuses on **predicting the total delivery time** for DoorDash orders, a critical task for logistics optimization, customer satisfaction, and efficient fleet management. Accurate time prediction helps set realistic expectations for customers and optimize route planning for drivers.

The core of the project involves training and comparing various **regression models** on historical delivery data, using **Root Mean Squared Error (RMSE)** as the primary evaluation metric. The goal is to minimize the prediction error (RMSE) to achieve the most reliable time estimates.

---

## 🏆 Key Findings & Best Model

Seven different regression models were tested and benchmarked against the test dataset's actual delivery times.

### Model Performance (Root Mean Squared Error - RMSE)

| Model | RMSE (Lower is Better) | Performance Category |
| :--- | :---: | :--- |
| **MLPRegressor (Recommended)** | **1007.80** | **Deep Learning (Best)** |
| LGBMRegressor | 1079.29 | Gradient Boosting (Excellent) |
| RandomForestRegressor | 2549.97 | Ensemble (Good Baseline) |
| DecisionTreeRegressor | 2577.26 | Simple Tree |
| XGBRegressor | 2869.17 | Gradient Boosting |
| Ridge | 2901.59 | Regularized Linear |
| LinearRegression | 2901.69 | Linear (Worst) |

### Conclusion Summary

The **Multi-layer Perceptron (MLPRegressor)**, a type of Artificial Neural Network, achieved the best performance with the lowest RMSE of **1007.80**, demonstrating its superior ability to capture non-linear relationships in the delivery data. The **LGBMRegressor** also provided excellent results, confirming that advanced ensemble and deep learning methods are best suited for this prediction task.

---

## 🔬 Methodology & Models

The analysis compares seven models from different families of regression algorithms:

* **Linear:** `LinearRegression`, `Ridge`
* **Tree/Ensemble:** `DecisionTreeRegressor`, `RandomForestRegressor`
* **Gradient Boosting:** `XGBRegressor`, `LGBMRegressor`
