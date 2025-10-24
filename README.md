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

## Database Information:


