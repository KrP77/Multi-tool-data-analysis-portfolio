# 🧾 Booking Completion Prediction – Classification with EDA

This project explores customer booking behavior using a structured dataset of flight bookings. The goal is to understand patterns using exploratory data analysis and train machine learning models to predict whether a booking is completed.

---

## 📄 Dataset Overview

The dataset (`customer_booking.csv`) includes various customer and booking features such as:

- `num_passengers`: Number of passengers
- `trip_type`: Type of trip (One Way, Round Trip, etc.)
- `sales_channel`: How the booking was made
- `flight_day` / `flight_hour`: Time and day of departure
- `route`, `booking_origin`: Travel and booking location info
- Binary indicators: Wants extra baggage, preferred seat, meals
- `flight_duration`: Length of flight
- `booking_complete`: Target variable (0 or 1)

> Note: Please update the data path (`your_path/Dataset/customer_booking.csv`) in the notebook as needed.

---

## 🧪 Steps & Techniques

### 🧹 Data Preprocessing
- Cleaned and converted `flight_day` to numeric values
- Encoded categorical variables using `LabelEncoder`
- Checked nulls and data types using `.info()` and `.describe()`

### 📊 Exploratory Data Analysis (EDA)
- Histograms, box plots, and countplots for key variables
- Correlation heatmap and pair plots
- Examined class imbalance and feature distributions

### 🤖 Model Building
- **Random Forest Classifier** (baseline & balanced)
- **Support Vector Machine (SVM)**
- Train-test split (80/20)
- Evaluated with:
  - Accuracy
  - Confusion matrix
  - Classification report

### 📈 Model Comparison
- Tested performance with and without class weighting
- Compared Random Forest vs. SVM classifiers
- Visualized confusion matrices for both

---

## 🧠 Key Learnings

- Class imbalance slightly affects prediction; balancing improves results
- Booking behavior can be reasonably predicted using ML classifiers
- `flight_duration`, `route`, and `trip_type` were among the important features

---

## ▶️ How to Use

1. Open the notebook in Google Colab or Jupyter.
2. Update the data path in `pd.read_csv()` to your local dataset.
3. Run through the cells for EDA and model training.
4. Try experimenting with different models or hyperparameters.

---

## 🔧 Dependencies

- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `sklearn` – preprocessing, model building, evaluation

---

This project is part of a learning portfolio and was completed using Google Colab notebooks.
