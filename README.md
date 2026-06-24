# CPSC481 Introduction to Machine Learning Final Project - Predicting Students' Dropout and Academic Success using Machine Learning

## Project Overview
Higher education institutions often face challenges in identifying students who are at risk of dropping out before completing their degree programs. Detecting and identifying which students are at risk of dropping out can help institutions provide timely support and improve student retention and academic success.

This project aims to address this problem by building a multiclass classification model that predicts student academic outcomes based on their academic path, demographics, social-economic factors, and the students' academic performance at the end of the first and second semesters. 

## Team Members
| Name             | 
|------------------|
| Wen Fan    |
| Hai Sieu Cao   |
|  Monte Bradford   |

## Layout of the Code
project/ <br>
| <br>
├── test.py <br>
├── data.csv <br>
├── test.ipynb </br>

## What Each File Does
### 1. test.py and test.ipynb (Main File)
Both files contains the same content. test.py is a Python file and test.ipynb is a Python notebook file. These files contains the entire project.
#### a) Load data
- Load the UCI "Predict Students' Dropout" dataset (697) via ucimlrepo — 4,424 students, 36 features, target = Dropout/Enrolled/Graduate.

#### b) Class distribution
- Check how many students per class. Shows imbalance (Graduate ≫ Enrolled), which guides our metric choice later.

#### c) Preprocessing
- Encode text labels to numbers, split 80/20 with stratify to keep class ratios, and scale features so models train properly.
- The original data has already performed a rigorous data preprocessing to handle data from anomalies, unexplainable outliers, and missing values.

#### d) Train Models
- Train three classifiers — Logistic Regression, Decision Tree, Random Forest. class_weight="balanced" makes them handle the imbalance.

#### e) Evaluation
- Score each model on the test set with accuracy, precision, recall, F1 (macro average so every class counts equally). Compare in one table.

#### f) Best Model Detail
- Take the top-F1 model and view its per-class report and confusion matrix to see where it predicts well and where it confuses classes.

#### g) Feature Importance
- Rank which features the Random Forest relied on most — the strongest predictors of student outcome.

### 2. data.csv
This is the data.csv file used for training and testing.  
From: [UCI Dataset](https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success)

## Dataset Used for this Project
[UCI Dataset](https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success)
