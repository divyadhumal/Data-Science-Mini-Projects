
# 🎓 Student Performance Prediction using Linear Regression

## 🧩 Project Overview
This project predicts students' **exam scores** using different study and lifestyle factors such as study hours, sleep hours, gaming time, focus index, and burnout level.  

The main goal is to find **what habits affect student performance** the most.

---

## 📊 Dataset
- **Source:** Kaggle – Student Performance Dataset  
- **Features include:**
  - Study hours  
  - Sleep hours  
  - Gaming hours  
  - Focus index  
  - Burnout level  
  - Exam score (target)

---

## ⚙️ Steps in the Project

1. **Data Understanding**
   - Loaded and explored the dataset.
   - Checked for missing values and data types.

2. **Data Cleaning**
   - Removed unnecessary columns like `student_id`.
   - Confirmed dataset has no missing values.

3. **Data Preprocessing**
   - Converted text columns into numeric format using `pd.get_dummies()`.

4. **Exploratory Data Analysis (EDA)**
   - Used a **correlation heatmap** to see how each feature relates to exam scores.

5. **Train-Test Split**
   - Split data into 80% for training and 20% for testing.

6. **Model Training**
   - Used **Linear Regression** from `sklearn` to train the model.

7. **Model Evaluation**
   - R² Score: **0.8163**  
   - MAE: **3.96**  
   - MSE: **25.01**  
   The model predicts exam scores with about **81% accuracy** and only **±4 marks error** on average.

8. **Visualization**
   - Created a scatter plot for **Actual vs Predicted Scores**.
   - Plotted a bar chart to show **Feature Importance**.

---

## 📈 Key Insights
- **Positive Impact:** Study hours, focus index, and sleep hours.  
- **Negative Impact:** Gaming hours and burnout level.  
- The model shows that **better focus and rest lead to higher scores**.

---

## 🚀 Future Improvements
- Try advanced models like **Random Forest** or **Gradient Boosting**.
- Apply **feature scaling** and **cross-validation** for better results.
- Build a small **web app using Streamlit** to make predictions interactively.

---

## 🧠 Skills Used
- Python 🐍  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- Data Cleaning, EDA, Model Training

---

## 💡 Conclusion
This project helped me understand the complete workflow of a machine learning project — from data cleaning to building and evaluating a model.  

It was great to see how simple data can reveal real-life insights like how study habits and lifestyle affect student performance.

---
 
**Divya Dhumal**  
Machine Learning Enthusiast
