# 🛍️ Customer Shopping Behavior Analysis

## 📋 Project Overview

This is an **industry-standard end-to-end data analytics portfolio project** that analyzes retail customer shopping behavior to uncover actionable business insights. The project demonstrates proficiency in data preparation, SQL analysis, and business intelligence visualization using Python, PostgreSQL, and Power BI.

### 🎯 Business Objective

A leading retail company seeks to understand customer shopping behavior to improve sales, customer satisfaction, and long-term loyalty. Management has observed changing purchasing patterns across demographics, product categories, and sales channels. This analysis aims to identify key factors (discounts, reviews, seasons, payment preferences) that drive consumer decisions and repeat purchases.

### 🔑 Key Business Question

**"How can the company leverage consumer shopping data to identify trends, improve customer engagement, and optimize marketing and product strategies?"**

---

## 📊 Dataset Information

- **Source**: Customer Shopping Behavior Dataset
- **Records**: 3,900 customer transactions
- **Features**: 18 attributes including demographics, purchase details, and behavioral metrics
- **Format**: CSV file

### Key Attributes:

- Customer Demographics (Age, Gender, Location)
- Purchase Information (Item, Category, Amount, Payment Method)
- Behavioral Metrics (Review Rating, Previous Purchases, Frequency)
- Business Factors (Discount, Subscription Status, Shipping Type)

---

## 🛠️ Technologies & Tools

| Category                    | Tools                         |
| --------------------------- | ----------------------------- |
| **Programming**             | Python 3.x                    |
| **Data Analysis**           | Pandas, NumPy                 |
| **Database**                | PostgreSQL                    |
| **Data Visualization**      | Power BI, Matplotlib, Seaborn |
| **Database Connectivity**   | SQLAlchemy, psycopg2          |
| **Development Environment** | Jupyter Notebook, VS Code     |
| **Version Control**         | Git, GitHub                   |

---

## 📁 Project Structure

```
Customer_Shopping_Behavior_Analysis/
│
├── customer_shopping_behavior.csv      # Raw dataset
├── main.ipynb                          # Data preparation & EDA notebook
├── customer_behavior.sql               # SQL queries for business insights
├── Analysis_Report.docx                # Comprehensive analysis report
├── README.md                           # Project documentation
└── LICENSE                             # MIT License
```

---

## 🔄 Project Workflow

### 1️⃣ **Data Preparation & Modeling (Python)**

- Import and explore raw data
- Handle missing values using median imputation
- Standardize column names
- Create derived features (age groups, purchase frequency)
- Remove redundant columns
- Load cleaned data into PostgreSQL database

### 2️⃣ **Data Analysis (SQL)**

- Connect Python to PostgreSQL using SQLAlchemy
- Execute 10 business-critical SQL queries
- Analyze customer segments, loyalty, and purchase drivers
- Extract insights on revenue, discounts, and product performance

### 3️⃣ **Visualization & Insights (Power BI)**

- Build interactive dashboards
- Visualize key patterns and trends
- Enable data-driven decision making

### 4️⃣ **Report & Presentation**

- Document findings and recommendations
- Create stakeholder-ready presentations
- Provide actionable business insights

---

## 🔍 Key Business Questions Analyzed

1. **Revenue Analysis**: Total revenue by gender
2. **Discount Optimization**: High-value customers using discounts
3. **Product Quality**: Top 5 products by review rating
4. **Shipping Comparison**: Purchase amounts by shipping type
5. **Subscription Impact**: Revenue comparison for subscribers vs non-subscribers
6. **Discount Strategy**: Products with highest discount usage
7. **Customer Segmentation**: New, Returning, and Loyal customers
8. **Category Performance**: Top 3 products per category
9. **Repeat Buyer Behavior**: Subscription likelihood for repeat buyers
10. **Demographic Insights**: Revenue contribution by age group

---

## 📈 Key Findings

### Revenue Insights

- **Male customers** generated $157,890 in revenue
- **Female customers** generated $75,191 in revenue
- **Young Adults** contribute the highest revenue ($62,143)

### Customer Segmentation

- **Loyal Customers**: 3,116 (79.8%)
- **Returning Customers**: 701 (18.0%)
- **New Customers**: 83 (2.1%)

### Subscription Analysis

- **Subscribers**: Average spend $59.49, Total revenue $62,645
- **Non-subscribers**: Average spend $59.87, Total revenue $170,436
- More customers prefer not to subscribe (2,847 vs 1,053)

### Product Performance

- **Top-rated products**: Gloves (3.86), Sandals (3.84), Boots (3.82)
- **Highest discount usage**: Hat (50%), Sneakers (49.66%), Coat (49.07%)

### Shipping Preferences

- **Express shipping**: Average purchase $60.48
- **Standard shipping**: Average purchase $58.46

---

## 💻 Installation & Setup

### Prerequisites

```bash
Python 3.8+
PostgreSQL 12+
Jupyter Notebook
Power BI Desktop (optional)
```

### Installation Steps

1. **Clone the repository**

```bash
git clone https://github.com/CodeWithKaushal/Customer_Shopping_Behavior_Analysis.git
cd Customer_Shopping_Behavior_Analysis
```

2. **Install required Python packages**

```bash
pip install pandas numpy sqlalchemy psycopg2-binary jupyter
```

3. **Set up PostgreSQL database**

```sql
CREATE DATABASE Customer_Behavior;
```

4. **Update database credentials in notebook**

```python
username = "your_username"
password = "your_password"
host = "localhost"
port = "5432"
database = "Customer_Behavior"
```

5. **Run the Jupyter notebook**

```bash
jupyter notebook main.ipynb
```

---

## 📝 Usage

### Running the Analysis

1. **Data Preparation**: Execute cells in `main.ipynb` to clean and prepare data
2. **Database Loading**: Run the SQLAlchemy code to load data into PostgreSQL
3. **SQL Analysis**: Execute queries in `customer_behavior.sql` or pgAdmin
4. **Visualization**: Open Power BI and connect to the PostgreSQL database

---

## 📊 Sample SQL Queries

### Revenue by Gender

```sql
SELECT gender, SUM(purchase_amount) as revenue
FROM customer
GROUP BY gender;
```

### Customer Segmentation

```sql
WITH customer_type AS (
  SELECT customer_id, previous_purchases,
    CASE
      WHEN previous_purchases = 1 THEN 'New'
      WHEN previous_purchases BETWEEN 2 AND 10 THEN 'Returning'
      ELSE 'Loyal'
    END AS customer_segment
  FROM customer
)
SELECT customer_segment, COUNT(*) AS "Number of Customers"
FROM customer_type
GROUP BY customer_segment;
```

---

## 🎓 Skills Demonstrated

- ✅ Data Cleaning & Preprocessing
- ✅ Exploratory Data Analysis (EDA)
- ✅ Feature Engineering
- ✅ SQL Query Development
- ✅ Database Management (PostgreSQL)
- ✅ Data Visualization
- ✅ Business Intelligence
- ✅ Statistical Analysis
- ✅ Documentation & Reporting
- ✅ Version Control (Git/GitHub)

---

## 🚀 Future Enhancements

- [ ] Implement machine learning models for churn prediction
- [ ] Build customer lifetime value (CLV) models
- [ ] Add recommendation system for product suggestions
- [ ] Create automated reporting pipeline
- [ ] Deploy interactive dashboard online
- [ ] Integrate real-time data streaming

---

## 📄 Deliverables

1. ✅ **Python Notebook** - Data cleaning and preparation
2. ✅ **SQL Scripts** - Business analysis queries
3. ✅ **Analysis Report** - Comprehensive findings document
4. ✅ **README Documentation** - Project overview and setup
5. ⏳ **Power BI Dashboard** - Interactive visualizations (in progress)
6. ⏳ **Presentation Slides** - Stakeholder communication (in progress)

---

## 👤 Author

**Kaushal Divekar**

- GitHub: [@CodeWithKaushal](https://github.com/CodeWithKaushal)
- Project Link: [Customer Shopping Behavior Analysis](https://github.com/CodeWithKaushal/Customer_Shopping_Behavior_Analysis)

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Dataset sourced from public retail transaction data
- Inspired by industry-standard data analytics practices
- Thanks to the data science community for best practices and guidance

---

## 📞 Contact & Feedback

For questions, suggestions, or collaboration opportunities:

- Create an issue in this repository
- Connect via GitHub

---

**⭐ If you find this project helpful, please consider giving it a star!**
