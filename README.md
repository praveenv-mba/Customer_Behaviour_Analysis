# 🛍️ Customer Shopping Behaviour Analysis

## 📖 Overview

This project analyzes **customer shopping behaviour** using transactional data from **3,900 purchases** across various product categories.
The objective is to uncover insights into **spending patterns, customer segments, product preferences, and subscription behaviour** to guide strategic business decisions and improve customer engagement.

---

## 📊 Dataset Summary

* **Rows:** 3,900
* **Columns:** 18
* **Key Features:**

  * **Customer Demographics:** Age, Gender, Location, Subscription Status
  * **Purchase Details:** Item Purchased, Category, Purchase Amount, Season, Size, Colour
  * **Shopping Behaviour:** Discount Applied, Promo Code Used, Previous Purchases, Purchase Frequency, Review Rating, Shipping Type
* **Missing Data:** 37 missing values in the *Review Rating* column

---

## 🧠 Exploratory Data Analysis (EDA) using Python

### 1. Data Loading

* Imported the dataset using **Pandas**.
* Performed initial inspection using `.info()` and `.describe()` to understand structure and statistics.

### 2. Data Cleaning

* **Missing Data Handling:**
  Imputed missing values in the *Review Rating* column using the **median rating per product category**.
* **Column Standardization:**
  Converted column names to **snake_case** for readability.

### 3. Feature Engineering

* Created an **age_group** column by binning customer ages.
* Derived **purchase_frequency_days** from purchase timestamps.

### 4. Data Consistency Check

* Checked redundancy between `discount_applied` and `promo_code_used`; dropped `promo_code_used`.

### 5. Database Integration

* Connected Python to **MySQL** using `SQLAlchemy` and loaded the cleaned DataFrame into the database for SQL-based business analysis.

---

## 🧩 SQL Analysis (Business Insights)

Structured SQL queries were performed in **MySQL** to answer key business questions:

1. **Revenue by Gender** – Compared total revenue between male and female customers.
2. **High-Spending Discount Users** – Identified discount users with above-average spending.
3. **Top 5 Products by Rating** – Ranked products by highest average review rating.
4. **Shipping Type Comparison** – Compared average purchase amounts between Standard and Express shipping.
5. **Subscribers vs. Non-Subscribers** – Analyzed spending behaviour and total revenue contribution.
6. **Discount-Dependent Products** – Found 5 products most dependent on discounts for sales.
7. **Customer Segmentation** – Classified customers as *New*, *Returning*, or *Loyal* based on purchase history.
8. **Top 3 Products per Category** – Identified most purchased items in each category.
9. **Repeat Buyers & Subscriptions** – Analyzed correlation between high purchase frequency and subscription likelihood.
10. **Revenue by Age Group** – Measured total revenue contribution by age segments.

---

## 📊 Power BI Dashboard

An **interactive Power BI dashboard** was developed to visually present key insights from the analysis.

**Dashboard Highlights:**

* KPIs: Total Revenue, Average Purchase Value, Active Subscribers
* Filters for Gender, Age Group, and Season
* Visuals:

  * **Bar charts** for revenue by category and age group
  * **Pie charts** for subscription distribution
  * **Trend line** for monthly sales
  * **Cards** displaying top-rated and top-selling products

> ![Power BI Dashboard Preview]<img width="1209" height="662" alt="Screenshot 2025-10-28 191325" src="https://github.com/user-attachments/assets/470ff7f0-6719-49f8-9530-95a8cc70ead4" />


---

## 💡 Business Recommendations

Based on data insights, the following recommendations were proposed:

* **Boost Subscriptions:** Promote exclusive benefits and loyalty rewards for subscribers.
* **Customer Loyalty Programs:** Reward repeat buyers to strengthen brand loyalty.
* **Review Discount Policy:** Balance discount offers with profitability to maintain healthy margins.
* **Product Positioning:** Highlight *top-rated* and *best-selling* products in marketing campaigns.
* **Targeted Marketing:** Focus advertising on high-revenue **age groups** and **Express shipping** users.

---

## ⚙️ How to Run the Project

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/customer-shopping-behaviour-analysis.git
   cd customer-shopping-behaviour-analysis
   ```

2. **Install Required Libraries:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Python Notebook:**

   ```bash
   jupyter notebook
   ```

   Execute cells for data cleaning, EDA, and database integration.

4. **Database Setup:**

   * Create a **PostgreSQL** database.
   * Import the cleaned dataset.
   * Run SQL scripts from the `/sql_queries/` folder to reproduce the analysis.

5. **View the Power BI Dashboard:**

   * Open the `.pbix` file in Power BI Desktop.
   * Interact with filters and visuals to explore insights.

6. **Presentation:**

   * Review the presentation under `/report/` for summarized insights and recommendations.

---

## 📬 Contact

**Author:** Praveen V
**Email:** praveenbrayanir.com
**LinkedIn:** https://linkedin.com/in/praveen-v-11653b22b
**Portfolio:** https://github.com/praveenv-mba

---

Would you like me to include a **“Project Folder Structure”** section (showing where scripts, data, and reports are stored)? It can make your README even more professional for recruiters.
