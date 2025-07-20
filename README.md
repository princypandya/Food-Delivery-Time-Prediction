# 🍱 Food Delivery Time Prediction

This project uses real-world food delivery logistics data to predict the time taken for food delivery and classify delivery speed as Fast or Slow. Both regression and classification models are applied for comprehensive predictive analysis.

---

## 📌 Objective

- Predict the time taken (in minutes) to deliver food orders.
- Classify deliveries as **Fast** or **Slow** based on time thresholds.
- Analyze how distance, traffic, weather, and vehicle conditions impact delivery.

---

## 📊 Dataset Overview

The dataset contains features like:

- Delivery person age, ratings, and vehicle condition
- Restaurant and delivery location coordinates
- Weather conditions and traffic density
- Order date, time, and type of vehicle/order
- **Time Taken** (target variable)

📁 **File**: `food_delivery.csv`

---

## 📂 Project Structure

### 🔹 Phase 1: Data Preprocessing

- ✅ Handled null/missing values
- ✅ Encoded categorical features
- ✅ Converted "Time taken" to numerical format
- ✅ Extracted and cleaned datetime features
- ✅ Calculated **distance** using the **Haversine formula**

### 🔹 Phase 2: Exploratory Data Analysis (EDA)

- Distribution of delivery time
- Distance vs. delivery time trend
- Impact of weather, traffic, and vehicle condition
- Correlation heatmap
- Feature importance analysis

---

## 🔮 Model Building

### 🔸 Linear Regression (for time prediction)

- **Target**: Time Taken (in minutes)
- **Key Features**: Distance, vehicle condition, weather, traffic, delivery type, etc.
- **Performance**:
  - R² Score: ~0.20 (low explanatory power)
  - MSE: High (model underfits)

### 🔸 Logistic Regression (for speed classification)

- **Target**: Delivery Speed (Fast = 0, Slow = 1)
- **Labeling Logic**: Threshold = Mean time taken (35.5 minutes)
- **Performance**:
  - Accuracy: 83.3%
  - Precision: 83%
  - Recall: 83%
  - F1 Score: 0.833

📌 **Conclusion**: Logistic Regression works **significantly better** than Linear Regression in classifying deliveries into meaningful speed categories.

---

## 📈 Visualizations

- 📊 Histograms for time, ratings, and distances
- 📉 Scatter plots: Distance vs. Time Taken
- 📌 Bar charts: Traffic, Weather, and their effects
- 🧮 Correlation heatmap for all numerical features
- 📍 Pie charts for traffic and weather distribution

---

## ⚙️ Technologies Used

- **Python Libraries**:
  - `pandas`, `numpy`
  - `scikit-learn`
  - `matplotlib`, `seaborn`
- **Distance Calculation**:
  - Haversine Formula (from coordinates)
- **Jupyter Notebook** for development and visualization

---

## 🔍 Key Insights

- 🚗 Distance is the most important predictor of delivery time.
- 🌧️ Poor weather and 🛑 high traffic conditions significantly delay deliveries.
- 🚙 Vehicle condition plays a noticeable role in delays.
- 👤 Delivery person age and ratings have minimal impact.

---

## 📢 Recommendations

- Assign high-condition vehicles for long or high-traffic deliveries.
- Monitor weather and traffic conditions for real-time adjustments.
- Implement a classification-based system to flag potential late deliveries.
- Future work: Use advanced models like Random Forest or XGBoost for better predictions.

---

## 📁 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/princypandya/Food-Delivery-Time-Prediction.git
   cd Food-Delivery-Time-Prediction
