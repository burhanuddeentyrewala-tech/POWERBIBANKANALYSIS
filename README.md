# 🏦 Banking Customer Analytics Dashboard — Power BI & Python

An end-to-end Business Intelligence project designed to help a retail bank understand its customers, financial product usage, loyalty segmentation, and branch performance — using **Power BI** for reporting and **Python** for data preprocessing.

---

## 📈 Project Summary

This dashboard enables stakeholders to explore:

✔ Deposit & loan distribution by customer profile  
✔ Loyalty tier segmentation and engagement level  
✔ Risk classification impact on financial products  
✔ Investment advisor portfolio tracking  
✔ Branch performance and customer demographics  
✔ Drill-through to view individual customer records  

---

## 🧬 Data Model (Star Schema)

The star-schema design supports optimized analytics and slicer filtering.

### **Fact Table**
- **Clients – Banking**
  - Financial metrics: Deposits, Loans, Savings, Credit Cards, Checking Accounts
  - Risk & engagement: Loyalty, Risk Weight, Properties Owned
  - Demographics: Age, Gender (FK), Relationship Type (FK), Advisor (FK)

### **Dimension Tables**
| Table | Description | Join |
|-------|-------------|------|
| Banking Relationship | Defines BR categories | 1 ↔ Many via BRId |
| Investment Advisor | Advisor ID / Name mapping | 1 ↔ Many via IAId |
| Gender | Customer gender dimension | 1 ↔ Many via GenderId |
| Period | Placeholder for time-based reporting | Not yet connected |

🔄 **DAX Measures** created for:  
Bank Deposit, Bank Loan, Business Lending, Checking Accounts, Credit Cards Balance, Savings Account, Foreign Currency Accounts, Engagement Length, Total Credit Card Amount

📌 *This improves accuracy & aggregation performance.*

---

## 🔗 Query Dependencies & Data Processing

All tables originate from the primary source CSV and are transformed via Power Query:

✔ Removed duplicates & validated foreign keys  
✔ Standardized financial metrics  
✔ Conditional columns created for engagement & loyalty tiers  
✔ Loaded clean model into Power BI  

---

## 📊 Dashboard Pages

### 1️⃣ Summary Dashboard
High-level customer profile overview:
- Total Deposits & Loans KPIs
- Product ownership by age, loyalty tier & nationality
- Geographic branch comparison

---

### 2️⃣ Deposit Analysis
- Deposit value trends by customer segment
- Saving vs. Checking adoption
- Deposit correlation with loyalty & risk-weight
- Advisor performance in deposit mobilization

---

### 3️⃣ Loan Analysis
- Loan distribution by age bracket & business type
- Risk-weighted loan portfolio
- Credit card exposure vs. customer engagement
- Property ownership as a lending qualifier

---

### 🔍 Drill-Through Page
Hidden from standard navigation

Used to **view individual customer financial profiles**, including:
- Full product engagement
- Advisor relationship
- Loyalty score breakdown

Great for **KYC and portfolio audits**.

---

## 🚀 Key Insights Discovered

- Higher deposits are concentrated among **Platinum loyalty tier** customers.
- Risk weight rises with **multiple lending products**.
- Young customers adopt **checking products** early but hold fewer properties.
- Advisors influence deposit & credit card engagement in specific branches.

---

## 🧠 Tools & Techniques Used

| Category | Technology |
|---------|------------|
| Data Preprocessing | Python, Pandas, Jupyter Notebook |
| Semantic Modeling | Power BI Desktop |
| Measure Logic | DAX Calculated Measures |
| Reporting | Interactive dashboards, drill-downs, filters |

---

## 🗂 Repository Structure

