# MIST4610-Group-Project

## Team Members:

1. Jack Brobst [@jackbrobst01](https://github.com/jackbrobst01)
2. Zeb Stone zgs18605@uga.edu
3. Wade Pirkl wjp82580@uga.edu 

## Scenario Description:

The task for our project is to design and build a database for an online retail company. The main focus of the database is the Customer entity, who can browse products, add products to their cart, and purchase the items. Some of the other entities consist of Product, Cart, Order, Payment, Shipper, and Address, which all work together to help track the shopping process. The goal was to design this model in a way that represents how an e-commerce store would work in real life. After creating the model, we populated it with data to represent business activity and then made 10 SQL queries to answer questions with the data that real managers would find helpful.

## Data Model:

Our model is based on an online retailer that sells products through an e-commerce platform. Customer, the main entity, stores information about each person who visits our online shop. Each customer can store multiple addresses for their shipping/billing accounts, but addresses cna only be linked to one customer (one to many). Each customer can also have one cart to store what they are shopping for and keep products in the cart while browsing. This is represented by the one-to-one between Cart and Customer.

Cart_Item serves as a bridge between Cart and Product, allowing a cart to hold many products and keep track of how many products are in each cart. Once a customer confirms their purchase, a record is kept in the Order Entity. Each order is linked to the customer who made it. An order can have many products, which is represented by the Order_item table and forms a many-to-many relationship between the two.

Payment is connected to Order through a one to one relationship representing how each order only has one payment and visa versa. The Shipper entity is also connected to Order through a one to one and stores information about the name and how the item was shipped (ground, air, 2-day, etc). Since one shipper can handle many orders, there is a one-to-many relationship between Shipper and Order.

The Product table stores basic product details such as name and price and is linked to the Category table, which groups products into logical sections such as “Electronics” or “Home.” It is connected to the Category entity through a one to many because a product can only be associated with one category, but categories can have many products. Category has a recursive relationship with itself because certain categories can have subcategories.

Overall, the data model represents the main functions and systems on an online shopping center, including browsing items, adding products to a cart, purchasing, and shipping, all while storing information about the customer, like a real-world situation.


<img width="1117" height="516" alt="MISTproject1 data model" src="https://github.com/user-attachments/assets/59d5de87-6554-424c-8303-b753d35974c2" />


## Data Dictionary:
<img width="1147" height="643" alt="image" src="https://github.com/user-attachments/assets/6037ad49-3c62-4900-93e9-20153086a84b" />
<img width="1152" height="826" alt="image" src="https://github.com/user-attachments/assets/e8a3dcfc-5684-44b1-80c4-d07ca4c32d10" />
<img width="1153" height="885" alt="image" src="https://github.com/user-attachments/assets/a7ed8374-16e3-4aa9-9564-4f2fd939025b" />
<img width="1152" height="769" alt="image" src="https://github.com/user-attachments/assets/a82b64c3-c85e-474c-8781-b9369fec0ba9" />
<img width="1165" height="738" alt="image" src="https://github.com/user-attachments/assets/e44b042c-048f-4497-b8ff-44410bb4e09e" />
<img width="1151" height="1044" alt="image" src="https://github.com/user-attachments/assets/28683260-3bcc-425f-ba30-5dc1d6f7507f" />
<img width="1179" height="1098" alt="image" src="https://github.com/user-attachments/assets/d151bda9-09ba-43de-a855-cfddccb69fa6" />
<img width="1149" height="1198" alt="image" src="https://github.com/user-attachments/assets/159dc902-b449-40af-be82-008931b9c6a8" />
<img width="1181" height="837" alt="image" src="https://github.com/user-attachments/assets/de272872-3e20-4eb8-acd5-285da162cd89" />
<img width="1166" height="504" alt="image" src="https://github.com/user-attachments/assets/1efde322-4b96-462d-9427-828101637167" />

## Ten Queries:
  1. Query 1 lists the total daily revenue and number of orders processed each day within the last 90 days. It joins the Payment, order, and shipper tables to show revenue patterns connected to shipping activity, grouping by the payment date.

Managers can use this query to track sales performance trends and identify high- and low-revenue days. It assists in recognizing seasonality, planning staffing levels, and timing promotions or discounts during slower periods.
<img width="1154" height="1036" alt="image" src="https://github.com/user-attachments/assets/eb83957e-c9bf-4bfa-9d0b-bdf5ab530a7b" />


  2. This query identifies the top ten products generating the most revenue in the last 90 days. It combines product, order, and order item data to calculate total revenue per product.
 
This query helps managers determine which products are driving the majority of sales and profit. These insights can guide marketing campaigns, highlight which items to feature on the website, and support better demand forecasting.
<img width="1136" height="834" alt="image" src="https://github.com/user-attachments/assets/623e861d-c8e7-4d93-be5b-60bc81f3f834" />


  3. This query summarizes sales revenue for each product category by linking categories to their products and corresponding order items.
 
Managers use this query to understand which product lines perform best, enabling data-driven inventory planning. It also helps identify underperforming categories that may require improved marketing or product updates.
<img width="1166" height="804" alt="image" src="https://github.com/user-attachments/assets/211f3011-a13b-4e7e-b112-df350926f343" />


  4. This query lists the top 20 customers based on total spending. It also displays the number of orders, average order value, and most recent order date for each.
 
Managers can use this to identify high-value customers for loyalty programs or personalized promotions. It highlights which customers contribute most to profitability and can guide retention and engagement strategies.
<img width="1144" height="875" alt="image" src="https://github.com/user-attachments/assets/fb4348b5-882a-4371-a095-482fb5e73544" />


  5. This query calculates total revenue, number of unique customers, and total orders per state.
 
Managers can use this information to identify strong regional markets and allocate marketing resources effectively. It also helps pinpoint underperforming areas where additional advertising or partnerships could increase sales.
<img width="1148" height="1092" alt="image" src="https://github.com/user-attachments/assets/c7bc92ed-d479-4cbd-b1c0-3f799dc1a4e2" />


  6. This query analyzes each shipping provider’s performance by counting orders shipped and calculating the average order value for each.
 
Managers can use this data to evaluate shipping partners’ performance, identify cost-efficient options, and ensure delivery reliability. It helps balance customer satisfaction with operational costs.
<img width="1166" height="885" alt="image" src="https://github.com/user-attachments/assets/91772488-99c0-4cfd-819e-9cff53c228c8" />


  7. This query shows which customers have ordered the same product more than once, and how many times have they purchased each repeated product.
 
This query helps the marketing department identify repeat buyers and brand-loyal customers for specific products. Customers who reorder the same product demonstrate strong product affinity, which provides an opportunity for targeted marketing campaigns.
<img width="831" height="826" alt="image" src="https://github.com/user-attachments/assets/b7bb3e0e-a6d3-4a07-8d24-6183f9c12754" />


  8. This query shows which products and categories are most frequently found in carts that were abandoned.
 
This query helps marketing and sales teams identify which specific products and categories customers most often add to their carts but fail to purchase, so they can develop ad campaigns about the abandoned products to help finalize their customers’ purchases. 
<img width="827" height="830" alt="image" src="https://github.com/user-attachments/assets/0eb5508a-e264-4fa7-956e-a80291b46112" />


  9. This query shows a list of customers who have items in their cart but have never completed an order.
 
This query allows managers to see which customers are actively engaging with the website (adding items to their carts) but are not completing purchases. These customers represent a key opportunity for targeted marketing strategies such as abandoned cart emails, personalized promotions, or reminders.
<img width="1161" height="643" alt="image" src="https://github.com/user-attachments/assets/a58bcb93-0d8c-4a86-b20f-9109bc896b32" />


## Database Information:
<img width="1176" height="767" alt="image" src="https://github.com/user-attachments/assets/19bd875a-bc55-46f0-8c16-5bf6f51eca16" />

Name of the database: 

