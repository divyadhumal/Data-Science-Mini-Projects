# Diabetes Prediction using Artificial Neural Network (ANN)

## Overview

This project uses an Artificial Neural Network (ANN) built with TensorFlow and Keras to predict whether a patient is diabetic or not based on medical attributes.

The model is trained on the Diabetes dataset and includes:

* Data preprocessing
* Feature scaling
* ANN model building
* Model evaluation
* Loss and accuracy visualization
* Basic regularization using Dropout

---

# Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* TensorFlow / Keras

---

# Dataset

The dataset contains medical information such as:

* Pregnancies
* Glucose
* Blood Pressure
* Skin Thickness
* Insulin
* BMI
* Diabetes Pedigree Function
* Age

Target Column:

* `Outcome`

  * `0` → Non-Diabetic
  * `1` → Diabetic

---

# Project Workflow

## 1. Import Required Libraries

Imported important libraries for:

* Data handling
* Visualization
* Preprocessing
* Model creation
* Model evaluation

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import confusion_matrix, accuracy_score
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense, Dropout
```

---

## 2. Load Dataset

The dataset is loaded using Pandas.

```python
data = pd.read_csv("diabetes.csv")
```

---

## 3. Data Preprocessing

Separated input features and output labels.

```python
X = data.drop("Outcome", axis=1)
y = data["Outcome"]
```

### Train-Test Split

```python
X_train, X_test, y_train, y_test = train_test_split(
    X, y,
    test_size=0.2,
    random_state=42
)
```

### Feature Scaling

StandardScaler is used to normalize the data.

```python
scaler = StandardScaler()

X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)
```

---

# 4. Building the ANN Model

The neural network contains:

* Input Layer
* Hidden Layers with ReLU activation
* Dropout layer for regularization
* Output Layer with Sigmoid activation

```python
from tensorflow.keras import Input

model = Sequential()

model.add(Input(shape=(X_train.shape[1],)))

model.add(Dense(32, activation='relu'))
model.add(Dropout(0.2))

model.add(Dense(8, activation='relu'))

model.add(Dense(1, activation='sigmoid'))
```

---

# 5. Compile the Model

The model uses:

* Adam optimizer
* Binary Crossentropy loss
* Accuracy metric

```python
model.compile(
    loss='binary_crossentropy',
    optimizer='adam',
    metrics=['accuracy']
)
```

---

# 6. Train the Model

The model is trained using:

* 150 epochs
* Batch size of 32
* Validation split of 20%

```python
history = model.fit(
    X_train,
    y_train,
    epochs=150,
    batch_size=32,
    validation_split=0.2,
    verbose=1
)
```

---

# 7. Model Evaluation

Predictions are made on test data.

```python
y_pred_prob = model.predict(X_test)

y_pred = (y_pred_prob > 0.5).astype(int)
```

### Confusion Matrix and Accuracy

```python
cm = confusion_matrix(y_test, y_pred)
acc = accuracy_score(y_test, y_pred)

print("Confusion Matrix:\n", cm)
print("Test Accuracy:", acc)
```

---

# 8. Loss Curve Visualization

Training loss and validation loss are plotted to analyze learning behavior.

```python
plt.plot(history.history['loss'], label='Training Loss')
plt.plot(history.history['val_loss'], label='Validation Loss')
```

### Insights

* Decreasing loss indicates learning
* Validation loss helps detect overfitting

---

# 9. Accuracy Curve Visualization

Training accuracy and validation accuracy are plotted.

```python
plt.plot(history.history['accuracy'], label='Training Accuracy')
plt.plot(history.history['val_accuracy'], label='Validation Accuracy')
```

### Insights

* Higher validation accuracy indicates better generalization
* Gap between train and validation accuracy may indicate overfitting

---

# Concepts Learned

During this project, the following concepts were explored:

* Artificial Neural Networks (ANN)
* Dense Layers
* Activation Functions
* Feature Scaling
* Binary Classification
* Overfitting
* Dropout Regularization
* Loss Curves
* Accuracy Curves
* Hyperparameter Tuning

---

# Results

* Successfully built a binary classification ANN model
* Achieved good validation accuracy on the diabetes dataset
* Visualized model learning using graphs
* Understood model performance and overfitting behavior

---

# Future Improvements

Possible improvements for better performance:

* Hyperparameter tuning
* EarlyStopping
* More hidden layers
* Learning rate optimization
* Cross-validation
* Feature engineering


 
