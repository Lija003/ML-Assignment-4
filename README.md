```{=html}
<p align="center">
```
`<img
    width="100%"
    src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=250&section=header&text=Feature%20Engineering%20%26%20Regression%20Modeling&fontSize=48&fontAlignY=38&animation=fadeIn&desc=Data%20Preparation%20and%20Machine%20Learning%20Pipeline&descAlignY=60"
    alt="Feature Engineering Banner"
  />`{=html}
```{=html}
</p>
```
```{=html}
<p align="center">
```
`<img src="https://readme-typing-svg.herokuapp.com?font=Orbitron&size=22&duration=3000&color=22C55E&center=true&vCenter=true&width=900&lines=Clean+Reliable+Machine+Learning+Dataset;Feature+Engineering+and+Regression+Models;Built+with+Python+Pandas+Scikit-Learn+and+Jupyter" />`{=html}
```{=html}
</p>
```
```{=html}
<p align="center">
```
`<img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white"/>`{=html}
`<img src="https://img.shields.io/badge/Pandas-Data%20Processing-150458?style=for-the-badge&logo=pandas&logoColor=white"/>`{=html}
`<img src="https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white"/>`{=html}
`<img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white"/>`{=html}
```{=html}
</p>
```

------------------------------------------------------------------------

# 🧠 Project Overview (Assignment 05)

**Feature Engineering, Data Preparation & Regression Modeling** is a
complete machine-learning preprocessing project built using Python and
Scikit-Learn.

The project converts a noisy student performance dataset into a
structured dataset suitable for regression and classification modeling.

The workflow includes:

-   Data quality inspection
-   Data cleaning
-   Missing value analysis
-   Duplicate removal
-   Categorical standardization
-   Feature engineering
-   Feature encoding
-   Feature scaling
-   Linear Regression
-   Logistic Regression
-   Model evaluation

------------------------------------------------------------------------

# 🎯 Assignment Objective

The objective is to clean:

``` text
student_dataset_dirty.csv
```

and build:

``` text
student_dataset_cleaned.csv
```

along with regression models for:

-   Predicting `Total_Score`
-   Predicting `Result` (Pass/Fail)

------------------------------------------------------------------------

# 📊 Dataset Overview

  Property                                         Value
  ------------------------ -----------------------------
  Dataset                    `student_dataset_dirty.csv`
  Original rows                                   10,000
  Original columns                                    15
  Cleaned rows                                     9,850
  Cleaned columns                                     16
  Removed duplicate rows                             150
  Environment                           Jupyter Notebook
  Language                                    Python 3.x

------------------------------------------------------------------------

# 📂 Project Files

  -------------------------------------------------------------------------------
  File                                        Description
  ------------------------------------------- -----------------------------------
  `Assignment_05_Regression_Complete.ipynb`   Complete notebook containing
                                              cleaning, feature engineering,
                                              Linear Regression and Logistic
                                              Regression

  `student_dataset_dirty.csv`                 Original raw dataset

  `student_dataset_cleaned.csv`               Structurally cleaned dataset

  `README.md`                                 Project documentation
  -------------------------------------------------------------------------------

------------------------------------------------------------------------

# 🧹 Data Cleaning Process

## Duplicate Removal

-   Identified duplicate records.
-   Removed 150 duplicate rows.

## Data Type Correction

Converted:

-   Age
-   Math Score
-   Science Score
-   English Score

into proper numeric formats.

Invalid text values were converted into missing values.

## Categorical Cleaning

Standardized:

-   Gender
-   City
-   Class
-   Parent Education
-   Internet Access
-   Result

Example:

``` text
male
MALE
Male

↓

Male
```

## Invalid Value Handling

Applied validation rules:

-   Age: 5--25 years
-   Attendance: 0--100%
-   Study hours: 0--16 hours/day
-   Subject scores: 0--100

Invalid values were replaced with missing values.

------------------------------------------------------------------------

# 🧬 Feature Engineering

Created additional features:

## Average_Score

Mean score calculated from:

-   Math Score
-   Science Score
-   English Score

## Study_Efficiency

Represents relationship between study time and attendance.

## Attendance_Category

Attendance converted into categories:

  Category   Range
  ---------- --------
  Low        \<60
  Medium     60--80
  High       \>80

------------------------------------------------------------------------

# 🔢 Feature Preparation

## Encoding

Categorical variables were encoded using:

``` text
One-Hot Encoding
```

Reason:

Categorical variables have no natural ranking, therefore label encoding
may create false relationships.

## Scaling

Numerical features were standardized using:

``` text
StandardScaler
```

Scaling was applied after train-test splitting to prevent data leakage.

------------------------------------------------------------------------

# 📈 Linear Regression Model

## Target

``` text
Total_Score
```

## Data Split

``` text
80% Training
20% Testing
```

## Leakage Prevention

The following features were excluded:

-   Math_Score
-   Science_Score
-   English_Score

Reason:

`Total_Score` is directly calculated from these variables.

Including them would create target leakage.

## Evaluation

Metrics:

-   R² Score
-   MAE
-   RMSE

Result:

``` text
R² ≈ -0.005
```

Interpretation:

Available demographic and behavioral features show no meaningful linear
relationship with total score.

------------------------------------------------------------------------

# 🤖 Logistic Regression Model

## Target

``` text
Result (Pass/Fail)
```

Binary conversion:

``` text
Pass = 1
Fail = 0
```

## Evaluation Metrics

-   Accuracy
-   Precision
-   Recall
-   F1-score
-   ROC-AUC

Result:

``` text
Accuracy ≈ 49%
ROC-AUC ≈ 0.49
```

Interpretation:

The model performs close to random guessing because predictors have weak
relationship with the target.

------------------------------------------------------------------------

# 🔄 Machine Learning Pipeline

``` mermaid
flowchart TD
A[Raw Dataset] --> B[Data Inspection]
B --> C[Cleaning]
C --> D[Feature Engineering]
D --> E[Encoding]
E --> F[Train Test Split]
F --> G[Scaling and Imputation]
G --> H[Linear Regression]
G --> I[Logistic Regression]
H --> J[Evaluation]
I --> J
```

------------------------------------------------------------------------

# 🏗 Technology Stack

-   Python
-   Pandas
-   NumPy
-   Scikit-Learn
-   Matplotlib
-   Seaborn
-   Jupyter Notebook

------------------------------------------------------------------------

# 📁 Final Project Structure

``` text
Assignment_05/
│
├── README.md
├── Assignment_05_Regression_Complete.ipynb
├── student_dataset_dirty.csv
├── student_dataset_cleaned.csv
└── requirements.txt
```

------------------------------------------------------------------------

# ▶️ How to Run

1.  Open the notebook:

``` text
Assignment_05_Regression_Complete.ipynb
```

2.  Keep dataset files in the same directory.

3.  Restart kernel.

4.  Run all cells.

5.  Export notebook as PDF.

------------------------------------------------------------------------

# 👨‍💻 Author

Student Assignment Submission

```{=html}
<p align="center">
```
`<b>`{=html}⭐ Data Preparation • Feature Engineering • Regression
Modeling ⭐`</b>`{=html}
```{=html}
</p>
```
