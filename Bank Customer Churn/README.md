# Bank Customer Churn Prediction

This project explores the prediction of customer churn using machine learning classification models. 
The dataset is sourced from a banking context, and includes features such as geography, gender, credit score, balance, number of products, and more.
The goal is to accurately identify which customers are likely to churn.

## 📌 Project Highlights

- **Exploratory Data Analysis (EDA)** using pandas, matplotlib, seaborn
- **Data preprocessing**: encoding categorical variables, feature scaling
- **Class imbalance handling**:
  - Original (Imbalanced)
  - Random Under Sampling (RUS)
  - Random Over Sampling (ROS)
- **Modeling** using:
  - Support Vector Classifier (SVC)
  - GridSearchCV for hyperparameter tuning
- **Performance Evaluation**:
  - Confusion Matrix
  - Classification Report (Precision, Recall, F1-Score, Accuracy)

## 🧰 Tools & Libraries

- Python (Jupyter Notebook)
- pandas, NumPy
- matplotlib, seaborn
- scikit-learn
- imbalanced-learn (`imblearn`)

## 📊 Dataset

- **Source**: [Bank Churn Dataset](BankChurnModelling.csv)
- **Target variable**: `Churn` (binary: 1 if the customer left, 0 otherwise)

## ⚙️ Steps Performed

1. Loaded and cleaned dataset
2. Handled categorical variables (`Gender`, `Geography`)
3. Created new feature: `Zero Balance`
4. Visualized class imbalance and feature relationships
5. Split dataset into:
   - Original
   - Undersampled
   - Oversampled
6. Trained SVM classifiers on all three datasets
7. Tuned models using GridSearchCV
8. Compared model performances

## 🔍 Results

| Dataset        | Model            | Accuracy | Notes                          |
|----------------|------------------|----------|--------------------------------|
| Original       | SVC              | ~80%     | Baseline model                 |
| Original       | GridSearchCV     | ↑        | Improved with tuning           |
| Under Sampled  | SVC + GridSearch | ~74–78%  | Balanced classes, lower data   |
| Over Sampled   | SVC + GridSearch | ↑        | Better results with more data  |

> Detailed classification reports and confusion matrices are provided in the notebook.

