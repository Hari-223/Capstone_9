Customer Retention Using Predictive Customer Lifetime Value (CLTV) Modeling

📌 **Project Overview**
This project focuses on identifying customers who are likely to churn and quantifying their value to the business using predictive Customer Lifetime Value (CLTV) modeling. The goal is to help businesses reduce unnecessary marketing costs and prioritize retention of high-value customers.

📊 **Key Objectives**
Clean and preprocess customer data.
Calculate Customer Lifetime Value (CLTV).
Segment customers using K-Means clustering.
Reduce feature complexity with PCA.
Predict customer churn using ML models.
Understand reasons for churn using a separate model.

📁 **Dataset**
We used two datasets:

Telco-Customer-Churn.csv: Demographics, usage, and churn labels.
Customer_Churn.csv: Behavioral and service-related data.

🧪 **Methodology**
🔹 Data Preprocessing
Handled missing values: Mode for categorical, mean for numerical.
Converted tenure to years.
Computed total revenue per customer.

🔹 CLTV Calculation
CLTV was calculated using the following formula: CLTV = customer_value × average_tenure customer_value = avg_order_value × purchase_frequency avg_order_value = total_charges / total_transactions purchase_frequency = transactions / total_customers

🔹 Customer Segmentation
Used K-Means clustering to categorize customers as:
High-value
Medium-value
Low-value

🔹 Feature Reduction
Applied PCA on highly correlated features like streaming services and billing to reduce noise and improve model performance.

🔹 Model Building
Used the following models to predict churn:
Logistic Regression
Decision Tree
Random Forest (including GridSearchCV tuning)

🔹 Churn Reason Prediction
Used a separate Random Forest model to identify why customers churn (e.g., better offers from competitors, poor service).

🏆 **Results**
Model	Accuracy	Recall
Decision Tree	77.71%	62.47%
Logistic Regression	84.74%	71.31%
Random Forest	84.32%	64.08%
Tuned RF (GridSearch)	84.46%	59.79%
Logistic Regression achieved the best recall, making it the most effective model for identifying potential churners.

📈 **Business Insights**
Focus retention efforts on 135 high-value customers predicted to churn.
Main reasons for churn: better competitor offers and poor support experience.
Strategic recommendations: improve pricing, and invest in employee training.

💡 **Future Scope**
Integrate real-time churn monitoring into CRM tools.
Expand model to other industries (e-commerce, banking, insurance).
Add deep learning models and SHAP for interpretability.

👥 **Team Members**
Hari Pavan Siva Phani Bhuti
Varun Aditya Madala

📦 Customer-Churn-CLTV/ ├── data/ │ ├── Telco-Customer-Churn.csv │ └── Customer_Churn.csv ├── Customer Churn Prediction.ipynb ├── README.md
