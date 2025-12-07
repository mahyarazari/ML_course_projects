# Naive Bayes Spam Classifier Implementation

This repository contains a Jupyter Notebook that implements a Naive Bayes classifier from scratch for the task of email spam (`spam`) and non-spam (`ham`) classification. The model uses token counts (word frequencies) extracted from a pre-processed dataset.

## Project Structure

* `Naive_Bayes_Spam_Classifier.ipynb`: The main notebook containing all the code for data loading, model training, prediction, and evaluation.
* `requirements.txt`: Lists the necessary Python packages.
* `train` / `test` (assumed): Input data files containing email ID, label, and word counts (not included here).

## Key Concepts and Methodology

The notebook covers the following steps and concepts:

1.  **Data Loading and Parsing:** Custom functions (`parse_line`, `load_dataset`) are used to read and process the raw text data format, converting it into a structured list of emails with their associated labels and token frequency dictionaries.
2.  **Prior Probability Calculation:** Calculating the base probabilities of a message being spam or ham: $P(\text{spam})$ and $P(\text{ham})$.
3.  **Conditional Probability Estimation:** Calculating $P(\text{word} | \text{class})$ for every word in the vocabulary, which is the core of the Naive Bayes model.
4.  **Add-m Smoothing (Laplace/Add-alpha):** The conditional probabilities are computed using the **Add-m Smoothing** technique to handle Out-Of-Vocabulary (OOV) words and prevent zero probabilities.
    $$P(word|class) = \frac{\text{count}_{word, class} + \alpha}{\text{Total Words}_{class} + \alpha \times V}$$
    (where $\alpha$ is the smoothing coefficient and $V$ is the vocabulary size)
5.  **Log-Probability Scoring:** Classification is performed by calculating the log-probability scores for each class ($\log P(\text{class} | \text{document})$) to avoid underflow errors.
6.  **Evaluation and Analysis of Smoothing Coefficient ($\alpha$):** The notebook analyzes the impact of different values for the smoothing coefficient $\alpha$ on model accuracy, demonstrating the concepts of Overfitting (small $\alpha$) and Underfitting (large $\alpha$).

## Dependencies

The following dependencies are required to run the notebook:

* Python 3.x
* `pandas`

You can install the required packages using pip:
```bash
pip install -r requirements.txt
