# Telco Customer Churn Analysis

## Project Objective

This project aims to **analyze customer churn** in a telecommunications company and develop insights to identify customers at risk of leaving.
The ultimate goal is to help reduce churn and **improve customer retention** through data-driven strategies.

---

## Dataset Overview

The dataset contains detailed customer information including demographics, subscribed services, billing methods, and churn behavior.

### Dataset Column Descriptions

| Column               | Description                                                   |
| -------------------- | ------------------------------------------------------------- |
| **customerID**       | Unique ID assigned to each customer.                          |
| **gender**           | Whether the customer is male or female.                       |
| **SeniorCitizen**    | Indicates if the customer is a senior (1 = Yes, 0 = No).      |
| **Partner**          | Whether the customer has a partner (Yes/No).                  |
| **Dependents**       | Whether the customer has dependents (Yes/No).                 |
| **tenure**           | Number of months the customer has stayed with the company.    |
| **PhoneService**     | Whether the customer has a phone service (Yes/No).            |
| **MultipleLines**    | Indicates if the customer has multiple phone lines.           |
| **InternetService**  | Type of internet service: DSL, Fiber optic, or No.            |
| **OnlineSecurity**   | Whether the customer has online security service.             |
| **OnlineBackup**     | Whether the customer has online backup service.               |
| **DeviceProtection** | Whether the customer has a device protection plan.            |
| **TechSupport**      | Whether the customer has technical support service.           |
| **StreamingTV**      | Whether the customer has a streaming TV service.              |
| **StreamingMovies**  | Whether the customer has a streaming movies service.          |
| **Contract**         | Type of contract: Month-to-month, One year, or Two year.      |
| **PaperlessBilling** | Whether the customer uses paperless billing (Yes/No).         |
| **PaymentMethod**    | Customer’s payment method (e.g., Credit Card, Bank Transfer). |
| **MonthlyCharges**   | Amount charged to the customer each month.                    |
| **TotalCharges**     | Total amount charged to the customer over their tenure.       |
| **Churn**            | Indicates whether the customer left the company (Yes/No).     |

---

## Data Preparation

* Removed duplicates and handled missing values.
* Encoded categorical variables into numerical form.
* Scaled numerical features for consistency.
* Created a new column: **`TotalServices`** = number of services subscribed.
* Split the data into **training** and **testing** sets for modeling.

---

## Exploratory Data Analysis (EDA)

### **1. Demographic Insights**

* Gender had **no significant impact** on churn.
* **Senior citizens** showed higher churn rates.
* Customers with **partners or dependents** were more likely to stay.

### **2. Tenure and Financial Behavior**

* Churned customers had an **average tenure of ~18 months** vs **~37 months** for loyal customers.
* Most churn occurred **within the first year**.
* Churned customers paid **higher MonthlyCharges**.

### **3. Service-Based Analysis**

* Customers with **Fiber Optic internet** and **Streaming services** churned more frequently.
* Customers with **6–8 subscribed services** had **lower churn rates**.

### **4. Contract and Payment Method**

* **Month-to-Month contracts** showed the **highest churn**.
* **One-Year** and **Two-Year** contracts **significantly reduced churn**.
* Customers using **Electronic Check** payments were more likely to leave.

---

## Key Findings

* **Overall Churn Rate:**

  * 26.5% of customers churned.
  * 73.5% remained loyal.

* **Main churn drivers:**

  * Short tenure (new customers).
  * High monthly charges.
  * Month-to-month contracts.
  * Fiber optic and streaming services.

* **Retention indicators:**

  * Long-term contracts.
  * Multiple bundled services.
  * Having dependents or partners.

---

## Next Steps (Modeling)

1. Train classification models such as:

   * Logistic Regression
   * Random Forest
   * XGBoost

2. Evaluate models using:

   * **Accuracy**, **Precision**, **Recall**, and **F1-score**

3. Predict churn probability for new customers and identify at-risk profiles.

---

## Conclusion

The analysis revealed that **contract length**, **tenure**, and **service bundles** play the most important roles in customer retention.

---

## 📊 Power BI Dashboard

![Power BI Dashboard ](dashboard.png)
By offering **long-term contracts**, **multi-service discounts**, and **better support for high-risk customers**, the company can effectively reduce churn and strengthen customer loyalty.

---

Would you like me to add a **"Visualizations Summary"** section (listing key charts used in the notebook) right after the EDA section? It makes the README look more complete for project presentation.
