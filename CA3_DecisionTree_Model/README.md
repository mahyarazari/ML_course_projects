# Decision Tree Classifier Implementation (ID3)

## 🚀 Project Overview
This project provides an implementation of the **ID3 Decision Tree Algorithm** for classification tasks. The core of the project involves custom functions to calculate **Entropy** and **Information Gain** to recursively build the tree. The model is applied to the classic 'PlayTennis' dataset.

## ✨ Features

The notebook and code cover the following key machine learning and implementation concepts:

* **Custom ID3 Implementation:** Building the Decision Tree from scratch using a recursive approach, defining custom `Node` and `DecisionTreeID3` classes.
* **Continuous Feature Handling:** Implementing a binary split method to find the optimal threshold for continuous features (like `Temperature`).
* **High Cardinality Trap Analysis:** Discussing and handling features with high cardinality (e.g., dropping `Day_ID`) to prevent the **High Cardinality Trap** and avoid overfitting.
* **Model Evaluation and Pruning:** Utilizing `scikit-learn` to conduct an experiment on the **Cost Complexity Pruning (CCP)** technique, analyzing the trade-off between tree size and test accuracy on the Iris dataset.
* **Evaluation Metrics:** Calculating standard metrics like **Accuracy**, **Precision**, and **Recall**.

## 🛠 Prerequisites

To run this project, you need Python and the packages listed in the `requirements.txt` file.

## 🏃 How to Run

1.  **Dependencies:** Ensure all libraries are installed:
    ```bash
    pip install -r requirements.txt
    ```
2.  **Data:** Ensure the data file (`jeeves_tennis.csv`) is accessible.

