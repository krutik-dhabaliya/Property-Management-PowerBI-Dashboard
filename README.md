# 🏢 Property Management Analytics Dashboard

<p  align="center">  <img  src="https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"  />  <img  src="https://img.shields.io/badge/Power_Query-217346?style=for-the-badge&logo=microsoft&logoColor=white"  />  <img  src="https://img.shields.io/badge/DAX-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"  />  <img  src="https://img.shields.io/badge/Data_Modeling-0078D4?style=for-the-badge&logo=microsoft&logoColor=white"  />  <img  src="https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white"  />  </p>

An interactive **Power BI dashboard** designed to analyze property sales, revenue, income, expenses, payment status, and geographical performance to support data-driven property management decisions.


## 📌 Overview

The **Property Management Analytics Dashboard** is a Power BI project developed to provide a comprehensive overview of property business performance. The dashboard brings together financial, property, geographical, and salesperson-level information into a single interactive report. Users can analyze key business metrics such as **Revenue, Income, Expenses, and Properties Sold** while using filters and parameter selections to explore the data from different perspectives. The project demonstrates practical skills in **data cleaning, data modeling, DAX, KPI development, dashboard design, and business data analysis using Power BI**.

## ❓ Problem Statement

Property management businesses generate data across property sales, financial transactions, locations, payment statuses, sales channels, and sales representatives.

When this information is stored across raw tables, it can be difficult for decision-makers to quickly answer questions such as:

- How much revenue and income is the business generating?
- How much is being spent on expenses?
- How many properties have been sold?
- How does performance change from month to month?
- Which sales channels account for the largest share of expenses?
- Which property types contribute most to expenses?
- Which countries generate the most revenue?
- Which transactions are still pending?
- How are individual salespeople performing?

The goal of this project is to transform the underlying property data into an **interactive and easy-to-understand Power BI dashboard** that allows stakeholders to monitor these metrics efficiently.


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

### 📥 Data Source

The source data is stored in **Microsoft Excel** and imported into **Power BI**, where it is transformed and modeled for analysis.

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
