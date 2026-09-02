# 🏢 Property Management Analytics Dashboard

<p align="center">
  <img src="https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
  <img src="https://img.shields.io/badge/Power_Query-217346?style=for-the-badge&logo=microsoft&logoColor=white" />
  <img src="https://img.shields.io/badge/DAX-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
  <img src="https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white" />
  <img src="https://img.shields.io/badge/Data_Modeling-0078D4?style=for-the-badge&logo=microsoft&logoColor=white" />
  <img src="https://img.shields.io/badge/Power_BI_Service-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
</p>

An interactive **Power BI dashboard** designed to analyze property sales, revenue, income, expenses, payment status, and geographical performance to support data-driven property management decisions.

## 📑 Table of Contents

- [Overview](#-overview)
- [Problem Statement](#-problem-statement)
- [Dataset](#-dataset)
- [Methods](#️-methods)
- [Key Insights](#-key-insights)
- [Dashboard](#-dashboard--model--output)
- [How to Run this Project](#️-how-to-run-this-project)
- [Results & Conclusion](#-results--conclusion)
- [Future Work](#-future-work)


## 📌 Overview

The **Property Management Analytics Dashboard** is a Power BI project developed to provide a comprehensive overview of property business performance. The dashboard brings together financial, property, geographical, and salesperson-level information into a single interactive report. Users can analyze key business metrics such as **Revenue, Income, Expenses, and Properties Sold** while using filters and parameter selections to explore the data from different perspectives. The project demonstrates practical skills in **data cleaning, data modeling, DAX, KPI development, dashboard design, and business data analysis using Power BI**.


## ❓ Problem Statement

Property management businesses generate data across sales, expenses, properties, locations, payment statuses, and customers. Without a centralized reporting solution, identifying business performance and trends can be challenging.

This project aims to answer key business questions:

- What are the overall revenue, income, expenses, and property sales?
- How does financial performance change over time?
- Which sales channels and property types drive the highest expenses?
- Which geographical markets generate the most revenue?
- How are property transactions and payment statuses performing?

The goal is to transform raw property data into an **interactive Power BI dashboard** that enables efficient performance monitoring and data-driven decision-making.


## 📂 Dataset

The project uses a structured property management dataset consisting of **four related tables**: `Client_Table`, `Property_Table`, `Sales_Table`, and `Expense_Table`.

Together, these tables capture information about properties, clients, sales transactions, payment status, and property-related expenses.

### 📋 Dataset Structure

#### 👤 Client Table

Contains information about clients associated with property sales.

| Column | Description |
|---|---|
| `ClientID` | Unique identifier for each client |
| `Name` | Client name |
| `Occupation` | Client's occupation |
| `Img` | URL used to display the client's profile image |

---

#### 🏠 Property Table

Contains the main characteristics and listing information for each property.

| Column | Description |
|---|---|
| `PropertyID` | Unique identifier for each property |
| `Country` | Country where the property is located |
| `Type` | Property type such as Apartment, Condo, Single Family, or Townhouse |
| `Bedrooms` | Number of bedrooms |
| `Bathrooms` | Number of bathrooms |
| `SquareFootage` | Total property area |
| `Price` | Listed property price |
| `ListedDate` | Date the property was listed |
| `Status` | Current property status, such as Sold or Pending |
| `Img` | URL of the property image |

---

#### 💰 Sales Table

Contains property sales transactions and connects properties with clients.

| Column | Description |
|---|---|
| `SaleID` | Unique identifier for each sale |
| `PropertyID` | Property associated with the transaction |
| `SaleDate` | Date of the property sale |
| `Means of Sales` | Sales channel — Broker, Direct, or Online |
| `ClientID` | Client associated with the transaction |
| `Payment Status` | Payment status — Paid or Pending |

---

#### 💸 Expense Table

Contains expenses associated with individual properties.

| Column | Description |
|---|---|
| `ExpenseID` | Unique identifier for each expense |
| `PropertyID` | Property associated with the expense |
| `ExpenseType` | Type of expense, such as Maintenance, Renovation, or Property Taxes |
| `Amount` | Expense amount |
| `Date` | Date on which the expense was recorded |

---

### 🔗 Data Relationships

The four tables are connected using common identifier fields:

- `PropertyID` connects the **Property**, **Sales**, and **Expense** tables.
- `ClientID` connects the **Client** and **Sales** tables.
- The `Sales_Table` acts as the transaction-level link between properties and clients.

This relational structure allows the Power BI dashboard to analyze financial and sales performance across properties, clients, countries, property types, and sales channels.


## ⚙️ Methods

The project followed an end-to-end **Power BI workflow**:

### 1. Data Cleaning & Transformation
- Imported Excel datasets into **Power BI**.
- Used **Power Query (M)** to clean data, correct data types, format dates, and prepare tables for analysis.

### 2. Data Modeling
- Built relationships between **Property, Sales, Client, Expense, and Calendar** tables.
- Applied **Star Schema principles** for simpler relationships, efficient filtering, improved performance, and easier DAX calculations.

#### Data Model
![Power BI Data Model](https://github.com/krutik-dhabaliya/property-management-powerbi-dashboard/blob/main/Output%20(Images)/Star%20Schema.png)

### 3. DAX & KPI Development
Created **DAX measures** for key business metrics including:
- Revenue
- Income
- Expense
- Properties Sold
- Percentage Change

### 4. Dashboard Development
Built an interactive dashboard using **KPI cards, charts, maps, tables, slicers, and dynamic parameters** to analyze financial, property, geographic, and sales performance.

## 💡 Key Insights

- **Strong Financial Performance:** The dashboard reports **£25.5M in revenue** and **£16.8M in income**, with total expenses of **£8.7M**.

- **Expense Growth:** Monthly expenses increased from **£0.4M in January** to a peak of **£1.8M in August**, indicating higher spending toward the later months.

- **Sales Channel:** **Online sales** accounted for the largest share of expenses at **39.66% (£3.5M)**, followed by Direct and Broker channels.

- **Property Type:** **Single Family properties** generated the highest expense share at **32.76% (£2.9M)**, while Townhouses had the lowest at **13.22% (£1.2M)**.

- **Geographic Performance:** Revenue varied significantly across countries, highlighting differences in market performance and potential opportunities for geographic targeting.

- **Sales Activity:** A total of **44 properties were sold**, providing a clear view of overall transaction performance for the selected period.

## 📊 Dashboard / Model / Output

### Property Management Dashboard

The final dashboard provides a single-page overview of property management performance.

It includes:

- KPI cards for **Revenue, Income, Expense, and Properties Sold**
- Financial year selection
- Dynamic parameter selection
- Monthly trend analysis
- Expense by sales channel
- Expense by property type
- Property transaction details
- Payment status tracking
- Revenue by country
- Salesperson performance analysis

### Dashboard Preview

![Property Management Analytics Dashboard](https://github.com/krutik-dhabaliya/property-management-powerbi-dashboard/blob/main/Output%20(Images)/Property_Managemet_Dashboard.jpg)

## ▶️ How to Run this Project?

To explore the dashboard locally:

1. Clone or download this GitHub repository.

2. Install **Microsoft Power BI Desktop** if it is not already installed.

3. Open the Power BI project file:

   `Property_Management.pbix`

4. If required, update the dataset source through:

   **Home → Transform Data → Data Source Settings**

5. Refresh the dataset.

6. Use the dashboard's **Financial Year selector, parameter selector, charts, tables, and other interactive elements** to explore the analysis.

## 📈 Results & Conclusion


## 📈 Results & Conclusion

The **Property Management Analytics Dashboard** transforms property data into an interactive report for monitoring financial, sales, geographic, and property-level performance.

The dashboard provides stakeholders with a centralized view of key KPIs while enabling deeper analysis through dynamic filters and parameters.

Overall, the project demonstrates an end-to-end **Power BI workflow**, including data transformation, data modeling, DAX calculations, and interactive dashboard development.


## 🚀 Future Work

- **Cloud Data Integration:** Replace Excel-based sources with a scalable database or cloud data platform such as **Snowflake, Azure SQL Database, or SQL Server**.
- **Automated Refresh:** Publish the dashboard to **Power BI Service** and configure scheduled data refreshes based on reporting needs.
- **Advanced Analytics:** Add **YoY growth, profit margins, and forecasting** for deeper business insights.
- **Enhanced Reporting:** Implement **drill-through pages and dynamic tooltips** for detailed property-level analysis.


⭐ If you found this project useful or interesting, consider giving the repository a star!
