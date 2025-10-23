# MIST4610-Group-Project

## Team Members:

1. Jack Brobst jdb54521@uga.edu
2. Zeb Stone zgs18605@uga.edu

## Scenario Description:

The goal of this project is to design and build a relational database that models the operations of an online retail company. The main focus of the database is the Customer, who browses products, adds them to their cart, and places orders. The database also includes entities like Product, Category, Cart, Order, Payment, Shipper, and Address, which help track different parts of the shopping process from start to finish. The purpose of this project is to organize and connect these entities in a way that accurately reflects how an online store works in real life. After creating the data model, we generated sample data and populated each table to represent real business activity. Finally, we will run SQL queries on the data to answer business-like questions.

## Data Model:

Our model is based on the structure of an online retail company that sells products through an e-commerce platform. The main entity is Customer, which stores information about each user who shops on the site. A customer can have multiple addresses saved for shipping and billing purposes, which is why there is a one-to-many relationship between Customer and Address. Each customer can also have one active Cart, where they can add products before completing a purchase.

The Cart_Item entity serves as a bridge between Cart and Product, allowing a cart to contain multiple products and keeping track of quantities for each. Once a customer confirms their purchase, a record is created in the Order table. Each order is linked back to the customer who made it, and an order can contain multiple products, which is represented by the Order_Item table. This associative entity connects Order and Product, forming a many-to-many relationship between them.

The Payment table is directly connected to the Order table in a one-to-one relationship, since each order has one payment record. The Shipper entity stores information about the shipping providers responsible for delivering the orders. Since one shipper can handle many orders, there is a one-to-many relationship between Shipper and Order.

The Product table stores basic product details such as name and price and is linked to the Category table, which groups products into logical sections such as “Electronics” or “Home.” The Category entity also includes a recursive relationship, since some categories can have subcategories.

Overall, this data model represents the essential functions of an online store, including browsing and adding items to a cart, purchasing, and shipping, while maintaining relationships that reflect how real-world e-commerce systems operate.

<img width="1117" height="516" alt="MISTproject1 data model" src="https://github.com/user-attachments/assets/db3d402c-c5c8-430d-b633-ddcdb0c2c393" />


## Data Dictionary:
<img width="1147" height="643" alt="image" src="https://github.com/user-attachments/assets/6037ad49-3c62-4900-93e9-20153086a84b" />


## Ten Queries:

## Database Information:


