# 📊  Telco Customer Churn Prediction using Decision Tree

## 📌 Project Overview 
This project predicts whether a customer will leave (churn) or not using a **Decision Tree Classifier**.

I worked on data cleaning, preprocessing, and model building to understand how machine learning models handle real-world data.

---

## 📂 Dataset
- Telco Customer Churn Dataset
- Contains customer details like:
  - Gender
  - Contract type
  - Monthly charges
  - Internet services
  - Payment method

---

## ⚙️ Steps Performed

### 1. Data Cleaning
- Converted `TotalCharges` to numeric
- Handled missing values
- Removed unnecessary rows

### 2. Data Preprocessing
- Used **Label Encoding** for categorical columns
- Converted text data into numerical format

### 3. Feature & Target Split
- Features (X): All columns except `Churn`
- Target (y): `Churn` column

### 4. Model Building
- Used `DecisionTreeClassifier`
- Trained model on dataset

### 5. Model Visualization
- Visualized tree using `plot_tree`
- Also created a simpler tree using `max_depth=3`

### 6. Model Evaluation
- Accuracy
- Precision
- Recall

### 7. Prediction
- Tested model on a new customer
- Predicted churn probability

---

## 📈 Results
- Model Accuracy: 77.77%
- Model can predict whether a customer will churn or not

---

## 🛠️ Technologies Used
- Python
- Pandas
- Matplotlib
- Scikit-learn

---

## 💡 What I Learned
- How to clean real-world data
- Handling categorical vs numerical data
- How Decision Trees make decisions
- Importance of model evaluation

---

## 🚀 Future Improvements
- Use Random Forest for better accuracy
- Perform feature selection
- Hyperparameter tuning

---

## 📌 Conclusion
This project helped me understand how machine learning models work step by step from data cleaning to prediction.

