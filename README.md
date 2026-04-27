# Banknote Counterfeit Detection

## Project Overview

This project aims to detect counterfeit banknotes using geometric measurements and machine learning techniques.

The analysis compares an unsupervised clustering approach with a supervised classification model in order to identify the most reliable method for counterfeit detection.

## Business Context

A public security organization wants to automate the detection of counterfeit banknotes based on physical measurements.  
The goal is to build a reliable model that can classify a banknote as genuine or counterfeit.

## Dataset

The dataset contains 170 banknotes:

- 100 genuine banknotes
- 70 counterfeit banknotes
- 6 numerical features describing banknote dimensions
- 1 target variable: `is_genuine`

Features include:

- diagonal
- height_left
- height_right
- margin_low
- margin_up
- length

## Methodology

The project follows these steps:

1. Exploratory Data Analysis
2. Statistical tests on feature relevance
3. Principal Component Analysis
4. KMeans clustering
5. Logistic Regression modeling
6. Model comparison and final recommendation

## Key Findings

- Some geometric features show strong differences between genuine and counterfeit banknotes.
- PCA shows a clear separation between genuine and counterfeit banknotes.
- KMeans clustering achieves around 95% accuracy.
- Logistic Regression achieves stronger performance and is better suited for the final detection task.

## Model Performance

| Model | Approach | Accuracy |
|---|---:|---:|
| KMeans | Unsupervised learning | 95.29% |
| Logistic Regression | Supervised learning | 100% on test set |

## Final Recommendation

Logistic Regression is the preferred model because it provides better classification performance and is easier to interpret.

The most influential variables are:

- margin_low
- margin_up
- length

## Repository Structure

```text
.
├── data/
│   ├── notes.csv
│   └── example.csv
├── notebooks/
│   └── banknote_counterfeit_detection.ipynb
├── reports/
│   └── banknote_counterfeit_detection.pdf
├── README.md
└── requirements.txt
