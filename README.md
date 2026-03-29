# SUPERVISED-vs-UNSUPERVISED-LEARNING
# Student Dropout Synthetic Dataset

This repository contains a synthetic dataset designed to simulate a real-world student dropout prediction problem for Data Mining / Machine Learning.

## Dataset File
- `student_dropout_synthetic.csv`

## Number of Records
- 600 student records

---

## Variables Description

### Demographic Variables
| Variable | Type | Description | Range / Categories |
|---------|------|-------------|------------------|
| Age | Numeric | Student age | Normally 16–35, includes outliers |
| Gender | Categorical | Student gender | Male, Female, Other |
| Origin | Categorical | Place of origin | Barranquilla, Cartagena, Santa Marta, Bogotá, Medellín, Other |

### Academic Variables
| Variable | Type | Description | Range |
|---------|------|-------------|------|
| HighSchool_Avg | Numeric | High school grade average | 0.0 – 5.0 |
| Admission_Test_Score | Numeric | Admission test score | 0 – 100 (includes outliers) |
| FirstSemester_GPA | Numeric | GPA of first semester | 0.0 – 5.0 (includes outliers) |

### Financial Variables
| Variable | Type | Description | Range / Categories |
|---------|------|-------------|------------------|
| Socioeconomic_Level | Numeric | Socioeconomic level | 1 – 6 |
| Scholarship | Categorical | Scholarship status | Yes, No |
| Loan | Categorical | Loan status | Yes, No |
| Financial_Aid | Categorical | Financial aid status | Yes, No |

### Output Variable
| Variable | Type | Description | Categories |
|---------|------|-------------|------------|
| Dropout | Categorical | Whether student dropped out | Yes, No |

---

## How Dropout Was Generated
Dropout probability was generated based on academic and financial performance:

- Lower first semester GPA increases dropout probability.
- Lower high school average increases dropout probability.
- Lower admission test score increases dropout probability.
- Lower socioeconomic level increases dropout probability.
- Scholarship and financial aid decrease dropout probability.

A probability score was computed and then used to randomly assign Dropout = Yes/No.

---

## Introduction of Null Values
Null values were introduced randomly in the following columns:

- Age
- HighSchool_Avg
- Admission_Test_Score
- FirstSemester_GPA
- Origin

Approximately 7% of the values in each of these columns were replaced with `NaN`.

---

## Introduction of Outliers
Outliers were artificially inserted to simulate real-world data issues:

- Age outliers: values such as 10, 50, 60
- Admission test score outliers: values such as 150, 200, -20
- GPA outliers: values such as 6.5, -1.0

A small number of rows were randomly selected and modified to include these extreme values.

---

## Author
Universidad de la Costa - Data Mining  
Daniel Jose Buelvas Donado 
Department of Computer Science and Electronics
