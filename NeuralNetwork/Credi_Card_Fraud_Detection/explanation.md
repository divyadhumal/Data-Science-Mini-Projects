## Project Explanation

In this project, I built a Credit Card Fraud Detection system using Machine Learning and Neural Networks.

The main goal of the project was to identify fraudulent credit card transactions from a highly imbalanced dataset where normal transactions were much higher than fraud transactions.

### What I Did

- Imported and analyzed the dataset using Pandas and NumPy
- Performed data preprocessing and train-test splitting
- Handled class imbalance using SMOTE (Synthetic Minority Oversampling Technique)
- Built an Artificial Neural Network (ANN) using TensorFlow/Keras
- Trained the model on the balanced dataset
- Evaluated the model using:
  - Accuracy Score
  - Confusion Matrix
  - Precision and Recall
- Predicted whether a transaction was fraudulent or genuine

### Why SMOTE Was Used

The dataset was highly imbalanced, which could make the model biased toward normal transactions.  
SMOTE helped balance the dataset by generating synthetic samples for the minority class (fraud transactions).

### Outcome

The project helped improve understanding of:
- Imbalanced datasets
- Neural Networks
- Fraud detection systems
- Model evaluation techniques
- Deep learning workflow using TensorFlow/Keras
