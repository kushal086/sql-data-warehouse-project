gold.dim_customers

a. Purpose: Stores customer details enriched with demographic and geographic data.

b. Columns:

A. customer_key (INT): Surrogate key uniquely identifying the record.
B. customer_id (INT): Unique numerical identifier for the customer.
C. customer_number (NVARCHAR): Alphanumeric tracking identifier.
D. first_name and last_name (NVARCHAR): The customer name.
E. country (NVARCHAR): Country of residence.
F. marital_status (NVARCHAR): Customer marital status.
G. gender (NVARCHAR): Customer gender.
H. birthdate (DATE): Customer date of birth.
I. create_date (DATE): Date the record was created.

gold.dim_products

a. Purpose: Provides information about the products and their attributes.

b. Columns:

A. product_key (INT): Surrogate key uniquely identifying the product record.
B. product_id (INT): Internal tracking identifier.
C. product_number (NVARCHAR): Alphanumeric code for categorization.
D. product_name (NVARCHAR): Descriptive name of the product.
E. category_id, category, and subcategory (NVARCHAR): Classifications grouping related items.
F. maintenance_required (NVARCHAR): Indicates if maintenance is needed.
G. cost (INT): Base price of the product.
H. product_line (NVARCHAR): The product series it belongs to.
I. start_date (DATE): Date the product became available.

gold.fact_sales

a. Purpose: Stores transactional sales data for analytical purposes.

b. Columns:

A. order_number (NVARCHAR): Unique identifier for the sales order.
B. product_key (INT): Surrogate key linking to dim_products.
C. customer_key (INT): Surrogate key linking to dim_customers.
D. order_date (DATE): Date the order was placed.
E. shipping_date (DATE): Date the order was shipped.
F. due_date (DATE): Date the payment was due.
G. sales_amount (INT): Total monetary value of the line item.
H. quantity (INT): Number of units ordered.
I. price (INT): Price per unit.
