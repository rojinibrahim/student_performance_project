# Student Performance Prediction

This project predicts student academic performance in Math and Portuguese secondary school courses, analyzing features ranging from student background to behavioral habits.

## Motivation

I built this project to practice data cleaning, feature engineering, and binary classification while building practical machine learning experience.

## Dataset

* **Source:** [UCI Machine Learning Repository - Student Performance](https://archive.ics.uci.edu/dataset/320/student+performance)
* **Records:** 395 Math instances, 649 Portuguese instances (33 features each).

## Project Structure

```text
student-performance-project/
│
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_exploratory_analysis.ipynb
│   └── 04_modeling.ipynb
├── images/
├── .gitignore
├── README.md
└── requirements.txt

**Key Findings**
•  Data Quality: Zero missing (null) values and zero duplicate rows across both datasets.
•  Anomalies Identified: Multiple instances where final grade $G3 = 0$ (students who dropped out or missed final exams), requiring special handling during data cleaning.
•  Outliers: Significant right-skew in absences (e.g., $75\%$ quartile is $8$, but maximum reaches $75$).
•  Target Skew: Higher overall pass rate ($G3 \ge 10$) in Portuguese compared to Mathematics.
•  Data Types: Several ordinal features (e.g., Medu, Fedu, studytime, job scales) are stored as numerical types (int64), which need careful consideration during scaling and categorical encoding.
•  Sample Size Disparity: The Portuguese dataset ($649$ rows) is significantly larger than the Mathematics dataset ($395$ rows), providing more training instances for modeling Portuguese performance.
•  Demographic Consistency: Distributions for key demographic features (such as school, sex, and age) remain highly consistent across both datasets, ensuring structural alignment for merged or comparative analyses.
