# Business Questions

## Update of PK's after checking
Customers Table: 

Tool - DuckDB on the command prompt for quick analysis of csv files with SQL 

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
    - I think the data here is dirty and so it will be hard to pin down the exact Primary key
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

## Questions
1. How many customers exist?
- On the customers table I was able to find 96096 unique Customer ID's
2. How many orders exist?
- There is about 99441 order IDs
- There is about 96478 orders that were delivered
3. Which products sell the most?
- There are no specific product names so instead I will look for which category of products sell the most:
    -  SELECT column_name
        FROM table_name
        WHERE column_name IS NOT NULL
        GROUP BY column_name
        ORDER BY COUNT(*) DESC
        LIMIT 1
     -- this is to find the mode
    - Most Common Category: cama_mesa_banho
    -Note: This identifies frequency, not necessarily revenue.
4. Which states generate the most orders?
- I will use the same to search for the mode of the most products
- SP is the state that generates the most orders
5. What kind of company is this?
 - This is an ecommerce marketplace for sellers
 - They dont own the products but are the online marketplace that sellers use to sell their items
 - Similar to Takealot or Amazon
6. Who creates value?
- Customers who buy the products
- Sellers who provide the products
- The Ecommerce website and application that provides the platform for the customers to reach the producs of the sellers
- Payments from credit / debit cards, boletos and vouchers
7. What is at the center of the business:
The orders table will definitely be at the center of the business and the data model as it has the most direct and indirect connections and relationships
    Direct Connections:
        - Customers
        - Order Items
        - Order Payments
        - Order Reviews
    Indirect Connections:
        - Sellers
        - Geolocation
        - Products