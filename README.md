# 🧮 Customer Lifetime Value (LTV) Prediction Project

## 📌 Objective
Predict the **Customer Lifetime Value (LTV)** using customer purchase behavior data to support targeted marketing strategies.


## What We Have Done

### 1. Data Collection & Loading
- Collected two main datasets:
  - **Transactions data** containing customer purchase records with order dates and order values.
  - **Customers data** containing customer registration dates.
- Loaded these datasets into a Python environment for analysis.

### 2. Data Preprocessing
- Converted date fields into proper datetime formats for easy time-based calculations.
- Merged the transaction and customer datasets on `customer_id` to combine purchase and registration information.

### 3. Feature Engineering
- Created key features to represent customer purchase behavior:
  - **Frequency:** Number of purchases made by a customer.
  - **Recency:** Number of days since the customer’s last purchase.
  - **Average Order Value (AOV):** Average amount spent per order.
- Calculated the **Total Value** of purchases per customer, which acts as the target variable for model training.

### 4. Model Development
- Split the data into training and testing sets.
- Trained a **XGBoost regression model** using Frequency, Recency, and AOV as input features to predict customer lifetime value.
- Evaluated the model’s performance using:
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)

### 5. Prediction and Customer Segmentation
- Generated predicted LTV values for all customers.
- Segmented customers into four groups (quartiles) based on their predicted LTV:
  - Low
  - Medium
  - High
  - Very High

### 6. Result Export & Visualization
- Exported the final dataset including predicted LTV and segments as a CSV file for further use.
- Saved the trained model for reuse or deployment.
- Created visualizations to illustrate the distribution of predicted LTV and customer segments, including:
  - Histogram of predicted LTV values.
  - Boxplot comparing LTV segments.

---

## Deliverables

- A Python notebook containing the complete data processing, model training, evaluation, and visualization pipeline.
- A serialized model file (`.pkl`) to load the trained model.
- A CSV file with final predicted LTV and customer segments.
- A project report detailing the methodology and results.

---

## Tools & Technologies Used

- Python (pandas, numpy, scikit-learn, xgboost)
- Data visualization libraries (matplotlib, seaborn)
- Model serialization with joblib

---

## How to Use

- Install the required Python libraries using the provided `requirements.txt`.
- Load the datasets (`transactions.csv` and `customers.csv`).
- Run the Python notebook to reproduce the preprocessing, modeling, and prediction steps.
- Use the saved model and prediction CSV for business insights or further analysis.

---

## Author

Ayush Katkar  
[GitHub](https://github.com/ayushkatkar) | [LinkedIn](https://linkedin.com/in/ayushkatkar)

---

## License

This project is licensed under the MIT License.

