# Data Dictionary

## Table Name
Customers
### What does it represent?
- It shows the company records of the customers they have had before and states and city of where they live 
    - Customer ID
    - Customer Unique ID
    - Customer Zip Code Prefix
    - Customer City
    - Customer State
### Possible Primary Key:
- Most likely primary key will be the Customer Unique ID cause it should have no duplicates cause it is unique 
### Possible Foreign Keys:
- The possible foreign keys will be the Zip Code Prefix, City and State as they all relate to the Geolocation Table.
### Interesting Columns:
- Customer ID
### Questions:
- Does Customer ID have any duplicates
- Does Customer ID and Customer Unique ID overlap well or affect the data's health
- The IDs are very long and chaotic, will other tables make them make more sense to who the customer is 

## Table Name
Geolocation
### What does it represent?
- The table shows the geolocation of the places the company sells to
    - Geolocation Zip Code Prefix
    - Geolocation Longitude
    - Geolocation Latitude
    - Geolocation City
    - Geolocation State
### Possible Primary Key:
- It would have to be Geolocation Zip Code Prefix
### Possible Foreign Keys:
- It would be the city and state. 
### Interesting Columns:
- I noticed some spelling errors in the city columns that need to be cleaned 
### Questions:
- Are there any duplicates in Geolocation Zip Code Prefix


## Table Name
Order Items 
### What does it represent?
- It shows all the order information
    - Order ID
    - Order Item ID
    - Product ID
    - Seller ID
    - Shipping Limit Date
    - Price
    - Freight Value
### Possible Primary Key:
- Order ID
### Possible Foreign Keys:
- Product ID and Seller ID most likely
### Interesting Columns:
- The Feight Value and Order Item ID
### Questions:
- Who is paying for the Freight, the customer or the company
- What does the Order Item ID refer to and are the numbers even correct on it as there seems to be a lot of duplication and the price seems to change so could it be a item or number of items (I may be able to solve this by checking the order_payments Dataset)
- Order ID might have a few duplicates


## Table Name
Order Payments
### What does it represent?
- Orders that have been paid and the methods used
     - Order ID
     - Payment Sequential
     - Payment Type
     - Payment Installments
     - Payment Value
### Possible Primary Key:
- Order ID
### Possible Foreign Keys:
- Payment value is possible key as it may relate to price and could help see if the customer also has to pay for the Freight Value too
### Interesting Columns:
- The Payment Sequential
    - means that a payment was processed as part of a strict, predetermined order
- Payment Type
    - Has a payment type called Boleto
        - Boleto bancário (commonly called a boleto) is a regulated Brazilian payment method that uses a voucher or invoice containing a barcode, numeric line, and Pix QR code to pay for purchases, bills, or services.
### Questions:
- In payment Sequential what could 1 and 2 mean as they seem to be the only numbers in the data


## Table Name
Order Reviews
### What does it represent?
- All the reviews from Customers who bought items from the company
    - Review ID
    - Order ID
    - Review Score
    - Review Comment Title
    - Review Comment Message
    - Review Creation Date
    - Review Answer Timestamp
### Possible Primary Key:
- Order ID
### Possible Foreign Keys:
- None
### Interesting Columns:
- Review score as it could give some insights on which items are most liked
### Questions:
- Not much. Just cleaning up duplications.

## Table Name
Orders
### What does it represent?
- The orders and their statuses 
    - Order ID
    - Customer ID
    - Order Status
    - Purchase Timestamp
    - Approval Timestamp
    - Delivered Carrier Date
    - Estimated Delivery Date
### Possible Primary Key:
-  Order ID
### Possible Foreign Keys:
- Customer ID
### Interesting Columns:
- Some null values in some areas
- Order Status
- Delivered Carrier Date vs Estimated Delivery Date
### Questions:
- What is the difference between our estimated delivery dates and our actual delivery date
- Why are there some null values
    - Are they cancelled orders, missed order, returns
Is there duplication in the Order ID that matches the other Order tables

## Table Name
Products
### What does it represent?
- The products in the company
     - Product ID
     - Category Name 
     - Name Length (Spelt wrong on the dataset)
     - Description Length (Spelt wrong on the dataset)\
     - Photo Quantity
     - Product Weight
     - Product Height
     - Product Length
     - Product Width
### Possible Primary Key:
- Product ID
### Possible Foreign Keys:
- Category Name
### Interesting Columns:
- Its a pretty straight foward table
### Questions:
- Nothing comes to mind

## Table Name
Sellers
### What does it represent?
- The sellers in the ecommerce business
    - Seller ID
    - Seller Zip Code prefix
    - Seller City 
    - Seller State
### Possible Primary Key:
- Seller ID
### Possible Foreign Keys:
- Seller Zip Code prefix
- Seller City 
- Seller State
### Interesting Columns:
- The city column needs some checking and fixing with the errors
### Questions:
- Nothing really comes to mind

## Table Name
Translation
### What does it represent?
- Translations for words in Portugese to English
    - Product Category
    - Product Category Name English
### Possible Primary Key:
- None 
### Possible Foreign Keys:
- None
### Interesting Columns:
- This table is more of an information table and doesnt affect the data directly
### Questions:
- Not really

## Central Table:
- Most likey customers table (Maybe the Orders Table)

## Possible Lifecycle:
- Customer places an order
- It gets approved and verified by their bank
- It gets approved by the ecommerce company
- An estimation of delivery is made by the company delivery system and availability of their items and the customer is most likely given a timeline
- It is delivered (or not if cancelled or unpaid)
- Possible review(s) is made by the customer

## Update of PK's after checking
Customers Table: 

Tool - DuckDB for quick analysis of csv files with SQL 

Code:
SELECT
    COUNT(*) AS total_rows,
    COUNT(DISTINCT col) AS product_id,
    COUNT(*) - COUNT(col) AS null_count
FROM 'olist_products_dataset.csv';

### Customers Table 
    - customers_id
### Geolocation Table 
    - unknown
### Order Items Table 
    - unknown
    - I think the data here is dirty and so it will be hard to pin down the exact Primary key OR there is a composite key
### Order Payments Table 
    - I still suspect that order ID is but due to duplicates the total row doesnt match though there are no nulls so theres a high chance
### Order Reviews Table 
    - review_id most definitely but theres still dupes
### Orders Table 
    - order_id 
### Products Table 
    - products_id 
### Sellers Table 
    - sellers_id
### Category Translation Table 
    - none

