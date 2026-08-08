# Student Performance Prediction Using Machine Learning

## 📌 Project Overview

**Student Performance Prediction** is a Machine Learning project that predicts students' final grades based on their academic performance and attendance.

The project uses **Linear Regression** and **Ridge Regression** to analyze factors such as Quiz scores, Midterm performance, Project scores, Quiz 2 scores, Attendance, and performance trends. It can predict the expected final grade, assign a letter grade, and identify whether a student is **"On Track"** or **"At Risk"**.

The project also supports **individual student prediction** as well as **batch prediction for multiple students**.

---

## 🎯 Objectives

* Predict a student's final grade using Machine Learning.
* Analyze the relationship between academic performance and final grades.
* Identify important factors influencing student performance.
* Compare Linear Regression and Ridge Regression.
* Identify students who may be academically at risk.
* Predict grades for individual students.
* Perform predictions for multiple students simultaneously.

---

## 🧠 Machine Learning Models

The project implements two regression algorithms:

### 1. Linear Regression

Used to predict the final numerical grade based on the selected input features.

### 2. Ridge Regression

A regularized version of Linear Regression that helps reduce the effect of potentially correlated features and overfitting.

---

## 📊 Features Used

The model uses the following features:

| Feature    | Description                                       |
| ---------- | ------------------------------------------------- |
| Quiz 1     | Student's first quiz score                        |
| Midterm    | Midterm examination score                         |
| Project    | Project score                                     |
| Quiz 2     | Student's second quiz score                       |
| Attendance | Student's attendance percentage                   |
| Trend      | Difference between recent and earlier performance |

The target variable is:

**Final Grade** – Predicted final numerical score from 0 to 100.

---

## 🔎 Exploratory Data Analysis

The project performs basic Exploratory Data Analysis (EDA), including:

* Dataset shape and preview
* Descriptive statistics
* Final grade distribution
* Correlation matrix
* Feature coefficient analysis
* Actual vs. predicted grade visualization

These visualizations help understand the dataset and the relationship between different academic factors.

---

## ⚙️ Data Preprocessing

Before training the models:

1. The dataset is generated using NumPy.
2. Academic scores are constrained between 0 and 100.
3. An **Assignment Average** feature is calculated.
4. A **Trend** feature is calculated to represent changes in performance.
5. Final grades are converted into letter grades:

   * **A:** 90–100
   * **B:** 80–89
   * **C:** 70–79
   * **D:** 60–69
   * **F:** Below 60
6. Students scoring below 70 are classified as **At Risk**.
7. Features are standardized using `StandardScaler`.
8. The data is divided into training and testing sets.

---

## 📈 Model Evaluation

The models are evaluated using:

* **R² Score**
* **RMSE (Root Mean Squared Error)**
* **5-Fold Cross-Validation**

These metrics are used to determine how accurately the models predict final grades.

---

## 👨‍🎓 Individual Student Prediction

The project provides a `predict_student()` function that allows users to enter a student's:

* Quiz 1 score
* Midterm score
* Project score
* Quiz 2 score
* Attendance

The system then calculates:

* Predicted final grade
* Letter grade
* Academic status

Example:

```python
predict_student(
    quiz1=78,
    midterm=82,
    project=91,
    quiz2=74,
    attendance=85
)
```

Example output:

```text
Student Prediction
----------------------
Predicted Grade : XX.XX
Letter Grade    : B
Status          : On Track
```

---

## 👥 Batch Prediction

The project also allows predictions for multiple students at once.

For each student, the system generates:

* Predicted Grade
* Letter Grade
* Status

A bar chart is also generated to visually compare predicted grades across the class.

---

## 🛠️ Technologies Used

* **Python**
* **NumPy**
* **Pandas**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **Google Colab**

### Machine Learning Libraries

```text
scikit-learn
```

Algorithms used:

```text
Linear Regression
Ridge Regression
```

---

## 📂 Project Structure

```text
Student-Performance-Prediction/
│
├── Student_Performance_Prediction.ipynb
├── README.md
└── requirements.txt
```

---

## 🚀 How to Run

### Option 1: Google Colab

1. Open the `.ipynb` notebook in Google Colab.
2. Run the cells sequentially.
3. The dataset will be generated automatically.
4. The models will be trained and evaluated.
5. Use the prediction functions to predict student performance.

### Option 2: Local Machine

Clone the repository:

```bash
git clone https://github.com/your-username/Student-Performance-Prediction.git
```

Install the required libraries:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

Open the notebook using Jupyter Notebook or VS Code and run the cells.

---

## 📌 Important Note

This project currently uses a **synthetically generated dataset** rather than real student records. The dataset is generated using NumPy with controlled random values for demonstration and educational purposes.

For a real-world application, the project could be extended by using an actual student performance dataset while maintaining appropriate privacy and data protection.

---

## 🔮 Future Improvements

Possible improvements include:

* Use a real-world student performance dataset.
* Add more academic and behavioral features.
* Implement additional Machine Learning algorithms such as Random Forest and Gradient Boosting.
* Build an interactive web application using Streamlit.
* Add early-warning notifications for at-risk students.
* Track student performance over multiple semesters.
* Improve prediction accuracy with hyperparameter tuning.
* Add dashboards for teachers and academic administrators.

---

## 📜 Conclusion

This project demonstrates how Machine Learning can be used to analyze academic performance and predict students' final grades.

By combining **academic scores, attendance, and performance trends**, the system provides both numerical grade predictions and simple academic risk identification.

It serves as an educational example of applying **Regression, Data Analysis, Data Visualization, Feature Engineering, and Model Evaluation** to a student performance prediction problem.
