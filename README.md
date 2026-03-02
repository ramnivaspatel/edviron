# EDVIRON Revenue, Commission & Settlement Analytics

## 📌 Business Context

This project analyzes transactional payment data processed through Edviron’s platform.

There are three pricing layers in each transaction:

1. Edviron Buying Price (Cost to Edviron)
2. Partner Pricing (ERP Pricing)
3. Merchant Pricing (School Pricing)

Revenue Definitions:

ERP Revenue = Merchant Pricing – Partner Pricing  
Edviron Net Revenue = Partner Pricing – Edviron Buying  
Edviron Gross Revenue = ERP Revenue + Edviron Net Revenue  

Payment gateway settles the entire gross amount to Edviron.  
Edviron later settles ERP’s share.

---

# 🧠 Project Objective

Build a complete financial analytics model that:

- Cleans and standardizes raw data
- Converts Flat / % pricing into absolute INR values
- Computes revenues and settlement metrics
- Generates exposure analysis
- Builds dynamic interactive dashboard

---

# 📁 Workbook Architecture

Sheets:

1. Raw_Data
2. Clean_Data
3. Pricing_Normalized
4. Revenue_Model
5. Reports
6. Dashboard
7. Assumptions_Notes

---

# 💰 Revenue Logic

Pricing Conversion:

If Type = FLAT → Rate  
If Type = PERCENT → Transaction Amount × Rate / 100  

ERP Revenue = Merchant – Partner  
Edviron Net Revenue = Partner – Buying  
Edviron Gross Revenue = ERP Revenue + Edviron Net Revenue  

Settlement:

ERP Payable = ERP Revenue (only SUCCESS)  
Edviron Retained = Edviron Net Revenue (only SUCCESS)  
Pending Exposure = Transaction Amount (if not SUCCESS)

---

# 📊 Dashboard Features

KPI Tiles:
- Total Transactions
- Total GMV
- ERP Revenue
- Edviron Net Revenue
- Edviron Gross Revenue
- Pending Exposure
- Unique Users
- Repeat Frequency

Charts:
- Revenue Split
- Monthly Trend
- Gateway Contribution
- Payment Method Mix

Filters:
- Date Range
- Partner
- Gateway
- Payment Method

---

# 📎 Author

Ramnivas Patel  
Data Analyst | Excel | Power BI | SQL | Python
