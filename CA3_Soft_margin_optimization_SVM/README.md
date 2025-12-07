# 🏆 Primal QP-Based Soft-Margin SVM

This project implements a **Primal Quadratic Programming (QP)**
formulation to train a **Soft-Margin Support Vector Machine (SVM)** for
binary classification. The model predicts which users are likely to
purchase a product based on the **Social_Network_Ads** dataset.

## 🚀 Project Overview

**`soft_margin_optimization.ipynb`** contains the complete workflow:

-   Data loading and preprocessing (`Social_Network_Ads.csv`)
-   Primal SVM formulation using `cvxpy`
-   Optimization to obtain the weight vector **w** and bias **b**
-   Model evaluation (accuracy)
-   Visualization of the decision boundary and support vectors

## 🛠️ Setup

Install dependencies:

    pip install -r requirements.txt

Python 3.7+ is recommended.

## 🏃 Running the Notebook

1.  Place `Social_Network_Ads.csv` in the working directory (or update
    its path in the notebook).\
2.  Open `soft_margin_optimization.ipynb` in Jupyter Notebook or Google Colab.\
3.  Run all cells sequentially.

> **Note:** QP solving requires `cvxpy` and a compatible solver (e.g.,
> **ECOS**, **OSQP**).

## 📊 Dataset

-   **File:** `Social_Network_Ads.csv`\
-   **Download:** Google Drive
-   **Key Features:**
    -   Age
    -   EstimatedSalary
    -   Purchased (target)
