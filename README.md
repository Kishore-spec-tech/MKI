# Credit Card Fraud Detection with Machine Learning
 
MSc Cybersecurity · HDBW · Methods of AI (MKI) · SS26
 
## Project Overview
 
This project compares three machine learning approaches for detecting credit card fraud in a highly imbalanced dataset (0.17% fraud rate): a supervised Random Forest classifier, and two unsupervised anomaly detection methods, Isolation Forest and One-Class SVM. Three resampling strategies (no resampling, SMOTE, and random undersampling) were also evaluated. All models are assessed primarily using AUC-PR rather than accuracy, due to the severe class imbalance.
 
## Team
 
- Priyanka Das

- Gauri Shubham Jadhav

- Hari Kishore Sankar
 
## Dataset
 
**Credit Card Fraud Detection** — published by the ULB Machine Learning Group

- Source: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

- 284,807 transactions, 492 fraudulent (0.17%)

- 28 PCA-anonymised features (V1–V28) plus Amount and Time
 
The dataset is not included in this repository due to its size. Download it from the Kaggle link above before running the notebook.
 
## How to Run
 
1. Download `creditcard.csv` from the Kaggle link above

2. Open `CreditCardProject.ipynb` in Google Colab

3. Run the upload cell and select `creditcard.csv` when prompted, or place the file in the same directory if running locally

4. Run all cells in order from top to bottom
 
## Requirements
 
Most libraries are pre-installed in Google Colab. If running locally, install:
Credit Card Fraud Detection | Kaggle
Anonymized credit card transactions labeled as fraudulent or genuine
Most libraries are pre-installed in Google Colab. The only one not included by default is `imbalanced-learn`. Run this in your first notebook cell if needed:
 
```
pip install imbalanced-learn
 
## Project Structure
 
| File | Description |

|---|---|

| `CreditCardProject.ipynb` | Full notebook: data loading, preprocessing, EDA, model training, evaluation |

| `README.md` | This file |
 
## Methods Summary
 
| Model | Type | Best AUC-PR |

|---|---|---|

| Random Forest (SMOTE) | Supervised | 0.8675 |

| Isolation Forest | Unsupervised | 0.1916 |

| One-Class SVM | Unsupervised | 0.1625 |
 
## Notes
 
- GridSearchCV was attempted for hyperparameter tuning but was computationally infeasible on Google Colab's free tier. A manual comparison of four configurations was used instead.

- One-Class SVM was trained on a 10,000 row sample of the training set due to the algorithm's quadratic time complexity.
 
