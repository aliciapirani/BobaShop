# BobaShop

## Team Name: 
Women In SQL

## Team Members:
Alicia Pirani 

Alekhya Seelam

Diya Tahliani

Linzey Nguyen

Lancey Charles

## Scenario Description: 
The objective is to design and implement a relational database that effectively captures the operations of a boba shop. At the core of this model is the Store entity, which interacts with various related components, including employees, transactions, drinks, and more. We aim to accurately represent these relationships, generate sample data, and populate the entities with relevant attributes. Additionally, we seek to execute meaningful queries on this data to gain valuable insights into the boba shop's performance and operations.

## Data Model:
Explanation of data model: 

Our data model is based on the structure of a hypothetical boba shop. It tracks employees, stores, drinks, transactions, payments, customer information, loyalty programs, and inventory.

One-to-Many Relationships:

Store - Employee: One store has many employees, but many employees can only work at one store.

Store - Transaction: One store can have many transactions, but many transactions link back to one store.

Store - Inventory: One store can have multiple inventory items, but many inventory items link back to one store.

Vendor - Inventory: One vendor can supply multiple products, but multiple products can only come from one vendor.

Customer - Transaction: One customer can make many transactions, but many transactions link back to one customer. 

Transaction - Payment: One transaction can have many payments, but payments can only link back to one transaction.

Transaction - TransactionItem: One transaction can have multiple transaction items, but many transaction items link back to one transaction.

Drink - TransactionItem: A drink can be in many transaction items, but many transaction items link back to one drink.

One-to-One Relationship:

Customer - LoyaltyProgram: One customer can have one loyalty program and one loyalty program can only link back to one customer.


Many-to-Many Relationship:

Drink - Transaction: One drink can be involved in multiple transactions, and one transaction can include multiple drinks.

One-to-Many Recursive Relationship: 

Employee's Boss - Employee: An employee who is a boss can look over many employees, but many employees report to one boss.

<img width="867" alt="Screenshot 2024-10-02 at 9 08 16 PM" src="https://github.com/user-attachments/assets/41b00d58-8f7c-412a-a1a7-00d7ed489242">

## Data Dictionary: 


## Ten Queries:


## Database Information:

