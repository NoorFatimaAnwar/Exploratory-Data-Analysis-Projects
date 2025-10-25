# 🧠 Student Academic Score Prediction -> EDA Edition

## 📘 Project Overview

This project explores how lifestyle factors such as **sleep**, **exercise**, **social media use**, and **study habits** influence students’ academic performance.

Using a **synthetic dataset of 5,000 students generated with ChatGPT**, the analysis includes data cleaning, missing value handling, outlier detection, and **Exploratory Data Analysis (EDA)** to uncover relationships between lifestyle behaviors and academic outcomes.

> The dataset was intentionally designed to contain imperfections similar to real-world data, allowing practice in realistic data preprocessing and analysis workflows.

---

## 🎯 Problem Statement

Analyze how different lifestyle factors (sleep, exercise, social media use, and study habits) influence students’ academic performance.

**Goal:** Identify which lifestyle behaviors most strongly affect academic success and understand their correlations and patterns through visual and statistical methods.

---

## 🧩 Dataset Details

**File name:** `students_lifestyle_5000.csv`  
**Source:** Generated using ChatGPT for educational and analytical purposes

### Overview

| Property | Details |
|-----------|----------|
| **Rows** | 5,000 |
| **Columns** | Mixed numerical and categorical variables |
| **Imperfections** | Missing values (~6%), typos, inconsistent labels, outliers, invalid values, duplicates |

**Intentional Data Imperfections:**
- Missing values (~6% across several columns)
- Typos and inconsistent categorical labels (e.g., `femmale`, `fmale`)
- Lowercase/variant entries in `Stress_Level`
- Duplicate `Student_ID`s
- Outliers in study/sleep/screen time
- Invalid values (e.g., attendance > 100%)

### Column Descriptions

| Column Name | Type | Description |
|--------------|------|-------------|
| Age | Numeric | Age of the student |
| Gender | Categorical | Student gender |
| Study_Hours_Per_Day | Numeric | Average hours spent studying daily |
| Sleep_Hours | Numeric | Average sleep hours per day |
| Physical_Activity_Hours | Numeric | Daily exercise hours |
| Screen_Time_Hours | Numeric | Daily screen/social media time |
| Social_Activity_Score | Numeric | Social interaction frequency score |
| Mental_Wellbeing_Score | Numeric | Overall mental wellness score |
| Attendance_Rate | Numeric | Class attendance percentage |
| Stress_Level | Categorical | Low / Medium / High |
| Academic_Score | Numeric | Final academic performance score |

---

## 🧹 Data Cleaning Steps

- Removed unnecessary columns (e.g., `Student_ID`)
- Handled missing values:
  - **KNN Imputer** for numeric data  
  - **Mode imputation** for categorical data
- Fixed inconsistent categorical entries (e.g., `femmale → Female`)
- Standardized `Stress_Level` categories
- Removed duplicates based on `Student_ID`
- Detected and treated outliers using **IQR (Interquartile Range)** method
- Capped invalid values (e.g., attendance > 100%)
- Verified data distributions after cleaning

---

## 📊 Exploratory Data Analysis (EDA)

### 🔹 Univariate Analysis
- Examined individual feature distributions using **histograms** and **countplots**
- Checked data balance and detected skewed variables

### 🔹 Bivariate Analysis
Explored pairwise relationships using **scatterplots**, **violin plots**, and **boxplots**.

**Key Findings:**
- 📈 Study hours show a strong positive correlation with academic performance  
- 😴 Sleep hours and screen time have weaker relationships  
- 💆 Lower stress levels correspond to higher academic scores  
- 🚻 Gender differences were statistically insignificant  

### 🔹 Multivariate Analysis
- Correlation heatmap revealed:  
  - **Strongest positive correlation:** `Study_Hours_Per_Day ↔ Academic_Score` (~0.78)  
  - **Strongest negative correlation:** `Screen_Time_Hours ↔ Mental_Wellbeing_Score` (~−0.20)
- 3D scatterplots illustrated combined effects of study hours, sleep, and stress.

---

## ⚙️ Feature Engineering

- **One-Hot Encoding** for categorical features (`Gender`, `Stress_Level`)
- **Feature Scaling** using `StandardScaler`
- **Feature correlation** and **variance analysis** for feature selection

---

## 🧠 Key Insights

- 📚 Study hours per day is the most influential predictor of academic performance  
- 📵 High screen time is linked with lower mental well-being  
- 😌 Stress level inversely impacts performance — lower stress = higher scores  
- 🚻 Gender and age show minimal impact  
- ⚖️ Balanced lifestyle habits lead to better academic outcomes  

---

## 🛠️ Technologies Used

| Category | Tools & Libraries |
|-----------|------------------|
| **Language** | Python |
| **Libraries** | pandas, numpy, matplotlib, seaborn, scikit-learn, scipy |
| **Environment** | Google Colab / Jupyter Notebook |
| **Techniques** | Data Cleaning, Outlier Detection, Visualization, Correlation Analysis, Feature Engineering |

---

## 📈 Future Improvements

- Develop a **machine learning model** to predict academic performance  
- Create **interactive dashboards** using Plotly or Power BI  
- Apply **statistical inference** or **regression analysis** for causal insights  

---

## 📦 How to Run the Project

```bash
# Clone the repository
https://github.com/NoorFatimaAnwar/Exploratory-Data-Analysis-Projects.git
cd Exploratory-Data-Analysis-Projects.git
```


# Run the Jupyter/Colab notebook
Academic_Score_EDA.ipynb

---
## 👩‍💻 Author

**Noor Fatima**  
🎓 *Computer Science Student* | 💡 *Data Science Enthusiast*  
📍 *Pakistan*  

---

## ⭐ Project Highlights

- ✅ **End-to-end realistic EDA workflow** — from messy data to insights  
- ✅ **Dataset generated with ChatGPT** to simulate real-world imperfections  
- ✅ **Comprehensive data cleaning** — imputation, outlier handling, and correlation analysis  
- ✅ **Ready for predictive modeling and academic research**

---
