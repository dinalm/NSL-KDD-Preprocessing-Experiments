# NSL-KDD Data Preprocessing Experiments

This repository contains the experimental implementation for the bachelor's thesis **"Effect of Data Preprocessing Techniques on Machine Learning Model Accuracy in Network Intrusion Detection."**

The study investigates how different data preprocessing techniques affect the performance of machine learning-based Intrusion Detection Systems (IDS) using the NSL-KDD dataset.

## 1. Research Overview

The experiments evaluate three machine learning classifiers:

- Random Forest
- XGBoost
- k-Nearest Neighbor (kNN)

Five preprocessing categories are investigated:

1. **Feature Scaling:** No Scaling, MinMax, Standard, Robust, and Normalizer.
2. **Categorical Encoding:** Label Encoding and One-Hot Encoding.
3. **Feature Selection:** All Features, PCA, SelectKBest, and Correlation-Based Selection.
4. **Class Imbalance Handling:** No Handling, SMOTE, Random Undersampling, and Class Weights.
5. **Outlier Removal:** No Removal, IQR-Based Filtering, and Z-Score Filtering.

A sixth experiment evaluates an optimized combined preprocessing pipeline.

A total of **120 model evaluations** are conducted across 20 experimental settings, three classifiers, and two classification scenarios (binary and multiclass).

## 2. Dataset

The study uses the NSL-KDD benchmark dataset:

- `KDDTrain+.txt` — 125,973 training records
- `KDDTest+.txt` — 22,544 testing records

The dataset files are not included in this repository.

Dataset download: [NSL-KDD on Zenodo](https://zenodo.org/records/17424143)

## 3. Installation and Execution

Install the required Python libraries:

`pip install -r requirements.txt`

**Google Colab:**

1. Create a folder named `NSL_KDD_Experiments` in Google Drive.
2. Place `KDDTrain+.txt`, `KDDTest+.txt`, and `NSL_KDD_Experiments.ipynb` inside the folder.
3. Open the notebook in Google Colab.
4. Run all cells in sequence.

**Local Jupyter Notebook:**

1. Install the required dependencies.
2. Place the two dataset files in the notebook's working directory.
3. Open `NSL_KDD_Experiments.ipynb` in Jupyter.
4. Restart the kernel and run all cells.

The complete experiments may require substantial execution time.

## 4. Evaluation Metrics

Model performance is evaluated using accuracy, precision, recall, F1-score, and ROC-AUC where applicable. The false alarm rate (FAR) is also calculated for binary classification.

## 5. Experimental Results

The repository includes:

- `NSL_KDD_Experiments.ipynb` — Complete experimental implementation.
- `results_summary.xlsx` — Results of all 120 model evaluations, including experiment-level worksheets and an F1-score pivot summary.
- `confusion_matrices_baseline.png` — Baseline confusion matrices for binary classification.
- `requirements.txt` — Required Python libraries.

## 6. Reproducibility

The experiments use the predefined NSL-KDD training and test sets, with a fixed random state of 42 where applicable.

Preprocessing transformations are fitted using training data, and the test dataset is used for evaluation.

Running the notebook generates `results_summary.xlsx` and `confusion_matrices_baseline.png`.

## 7. Research Purpose

This repository accompanies an academic thesis conducted at Metropolia University of Applied Sciences, Finland.
