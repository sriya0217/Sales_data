Sales Data Cleaning and Preprocessing

This project demonstrates the process of cleaning and preparing a raw sales dataset for further analysis. The dataset was originally provided in CSV format and contained issues such as missing values, duplicate records, inconsistent formatting, and unnecessary columns.

📂 Dataset Information
The dataset represents sales transactions, including order details, customer details, and regional information.

Column Descriptions:
ORDERDATE → Date of the order (converted to proper datetime format, time removed).
ADDRESSLINE1 → Primary customer address.
ADDRESSLINE2 → Secondary customer address (removed during cleaning as it contained redundant/empty values).
CITY → City of the customer.
STATE → State of the customer (missing values filled with "Unknown").
POSTALCODE → Postal/ZIP code (missing values filled with "Unknown").
COUNTRY → Country of the customer.
TERRITORY → Sales territory/region (missing values filled with "Unknown").
CUSTOMERNAME → Name of the customer or company.
CONTACTLASTNAME → Customer’s contact last name.
CONTACTFIRSTNAME → Customer’s contact first name.
PHONE → Customer’s phone number.
SALESREPRESENTATIVE → Assigned sales representative.
PRODUCTCODE → Unique product identifier.
PRODUCTNAME → Name/description of the product.
QUANTITYORDERED → Number of units ordered.
PRICEEACH → Price per unit.
ORDERNUMBER → Unique identifier for each order.
DEALSIZE → Size of the deal (e.g., Small, Medium, Large).

🔧 Data Cleaning Steps

Loaded dataset from CSV using Latin-1 encoding.
Checked for missing values using .isnull().sum().
Dropped all rows with any missing values using .dropna().
Converted ORDERDATE to a proper date format, removing the time component.
Removed the ADDRESSLINE2 column (if present).
Filled missing values in STATE, POSTALCODE, and TERRITORY with "Unknown".
Dropped duplicate rows to ensure unique entries.
Reset the DataFrame index after row removals.
Cleaned column headers by:
Stripping whitespace,
Converting to lowercase,
Replacing spaces with underscores,
Removing special characters.

Saved the cleaned dataset as an Excel file:

      D:\datasets\sales_data_cleaned.xlsx
