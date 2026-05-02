# 📩 SMS Spam Detection using Naive Bayes

## 🚀 Overview
This project is a **Machine Learning-based SMS Spam Classifier** that predicts whether a message is **Spam or Not Spam (Ham)** using Natural Language Processing (NLP) techniques.

It uses **text preprocessing, TF-IDF vectorization, and Naive Bayes classification** to build an efficient spam detection system.

---

## 🎯 Problem Statement
Spam messages are a common issue in communication systems.  
The goal of this project is to build a model that can automatically classify SMS messages and help filter unwanted spam.

---

## 🛠️ Tech Stack
- Python  
- Pandas, NumPy  
- NLTK (Natural Language Processing)  
- Scikit-learn  
- Streamlit (for deployment)

---

## ⚙️ Features
- Text preprocessing (lowercasing, tokenization, stopword removal, stemming)  
- TF-IDF vectorization  
- Multinomial Naive Bayes model  
- Real-time prediction using Streamlit UI  

---

## 🔄 Workflow
1. Data Cleaning & Preprocessing  
2. Text Transformation using TF-IDF  
3. Model Training using Naive Bayes  
4. Model Evaluation  
5. Deployment using Streamlit  

---

## 🧠 Model Used
- **Multinomial Naive Bayes**
  - Suitable for text classification problems  
  - Performs well with discrete features like word counts  

---

## 📊 Evaluation Metrics
- Accuracy  
- Precision  
- Recall  
- F1-Score  

---

## 💻 How to Run the Project

### 1. Clone the repository
```bash
git clone https://github.com/divyadhumal/Data-Science-Mini-Projects.git
cd Data-Science-Mini-Projects/Naive_Bayes_Algo/SMS_Spam_detection

pip install -r requirements.txt
streamlit run app.py

