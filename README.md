# BobaShop

## Team Name: 
Women In SQL

## Team Members:
Alicia Pirani [@aliciapirani](https://github.com/aliciapirani)

Alekhya Seelam [@alekhyaseelam](https://github.com/alekhyaseelam)

Diya Tahliani [@diyatahliani](https://github.com/diyatahliani)

Linzey Nguyen [@linzeynguyen](https://github.com/linzeynguyen)

Lancey Charles [@lanceycha](https://github.com/lanceycha)

## Scenario Description: 
The objective is to design and implement a relational database that effectively captures the operations of a boba shop. At the core of this model is the Store entity, which interacts with various related components, including employees, transactions, drinks, and more. We aim to accurately represent these relationships, generate sample data, and populate the entities with relevant attributes. Additionally, we seek to execute meaningful queries on this data to gain valuable insights into the boba shop's performance and operations.

## Data Model:
### Explanation of data model: 

Our data model is based on the structure of a hypothetical boba shop. It tracks employees, stores, drinks, transactions, payments, customer information, loyalty programs, and inventory.

### One-to-Many Relationships:

Store - Employee: One store has many employees, but many employees can only work at one store.

Store - Transaction: One store can have many transactions, but many transactions link back to one store.

Store - Inventory: One store can have multiple inventory items, but many inventory items link back to one store.

Vendor - Inventory: One vendor can supply multiple products, but multiple products can only come from one vendor.

Customer - Transaction: One customer can make many transactions, but many transactions link back to one customer. 

Transaction - Payment: One transaction can have many payments, but payments can only link back to one transaction.

Transaction - TransactionItem: One transaction can have multiple transaction items, but many transaction items link back to one transaction.

Drink - TransactionItem: A drink can be in many transaction items, but many transaction items link back to one drink.

### One-to-One Relationship:

Customer - LoyaltyProgram: One customer can have one loyalty program and one loyalty program can only link back to one customer.


### Many-to-Many Relationship:

Drink - Transaction: One drink can be involved in multiple transactions, and one transaction can include multiple drinks.

### One-to-Many Recursive Relationship: 

Employee's Boss - Employee: An employee who is a boss can look over many employees, but many employees report to one boss.

<img width="867" alt="Screenshot 2024-10-02 at 9 08 16 PM" src="https://github.com/user-attachments/assets/41b00d58-8f7c-412a-a1a7-00d7ed489242">

## Data Dictionary: 

### Table: Store 

<img width="885" alt="store " src="https://github.com/user-attachments/assets/a887b708-0c07-4753-a645-a372c8d2d42f">

### Table: Employee

<img width="882" alt="employee" src="https://github.com/user-attachments/assets/34210ffb-188f-43b8-beab-5aaf4e21b95d">

### Table: Payment
<img width="918" alt="payment" src="https://github.com/user-attachments/assets/e4b28b40-1fec-4608-9bc3-31974d9865b9">

### Table: Transaction
<img width="882" alt="transaction" src="https://github.com/user-attachments/assets/103c44e7-7f7a-4b92-8471-539dad18b67c">

### Table: Transaction Item
<img width="973" alt="transaction item" src="https://github.com/user-attachments/assets/616491d8-e761-470e-8176-29c059e4ee0f">

### Table: Vendor 
<img width="973" alt="vendor" src="https://github.com/user-attachments/assets/60c3975b-70e5-4d00-bd2c-a787e5b0e8a9">

### Table: Customer
<img width="973" alt="customer" src="https://github.com/user-attachments/assets/09f74b81-063c-446d-88e4-8f48bcce07fa">

### Table: Loyalty Program
<img width="973" alt="loyalty program" src="https://github.com/user-attachments/assets/0ad7eaa1-ceea-42f3-9f5a-48b9d82e30f4">

### Table: Drink 
<img width="973" alt="drink" src="https://github.com/user-attachments/assets/b8d62343-8362-4fb9-b571-49359cf035b5">

### Table: Inventory
<img width="973" alt="inventory" src="https://github.com/user-attachments/assets/dd880c5b-023e-43d9-94d9-3e8fd51c6a0e">

## Ten Queries:

### Query #1: Provide a list of puree products in our inventory and their vendor that have a price higher than the average price of products in the same category.
This query is relevant from a managerial perspective because it shows which puree products from which vendor are costing the boba shop too much money. This information can help save the shop money or even make a switch of vendors. 

<img width="789" alt="Q1" src="https://github.com/user-attachments/assets/3641a5b4-6841-45c7-a227-aa16a7763110">

### Query #2:  List the names of customers who have made transactions that include a drink with a price greater than $5.00.
This query is relevant from a managerial perspective because it shows who the shop's best customers are and which drinks are making the shop good money. This information can help the shop market to a specific target market and promote specific drinks. 

<img width="754" alt="Q2" src="https://github.com/user-attachments/assets/e6f01bed-e375-46e1-bcda-99d3fc9cc250">

### Query #3: List the top five most profitable drinks based on sales minus cost. Show from most profitable to least profitable.
This query is relevant from a managerial perspective because it shows the most profitable drinks. This information can help the shop focus on identifying and promoting these top five most profitable drinks to increase the shop's overall profit. 

<img width="965" alt="Q3" src="https://github.com/user-attachments/assets/12671556-c07b-4b4a-bb97-7296c630f36e">

### Query #4: List the quantity ordered of drinks for customers who have loyalty points greater than 50.
This query is relevant from a managerial perspective because it shows how many drinks were ordered by customers having loyalty points higher that 50. This information highlights the effectiveness of loyalty programs, aiding in inventory management and revenue forecasting to ensure popular items are always available to meet demand.

<img width="848" alt="Q4" src="https://github.com/user-attachments/assets/c0f1c617-334b-41a8-97b5-82bd64020a39">

### Query #5: What are the least popular drinks based on sales in the last 3 months?
This query is relevant from a managerial perspective because it shows the least popular drinks by looking at sales from the past three months. This information can help managers understand customer preferences and adjust their offerings accordingly to improve sales and inventory management.

<img width="710" alt="Q5" src="https://github.com/user-attachments/assets/b5873773-92d0-46f3-a25a-91dd9528619c">

### Query #6: List the total sales for each drink in the last month.
This query is relevant from a managerial perspective because it shows each drinks sales from the past month. This information can help managers identify underperforming products that may need promotional support or discontinuation. 

<img width="877" alt="Q6" src="https://github.com/user-attachments/assets/a3b6b0b0-1d8e-4137-9712-e8b4b54d9221">

### Query #7: Which day in September had the highest sales?
This query is relevant from a managerial perspective because it identifies peak shopping times and customer behavior patterns. This information allows managers to plan staffing, inventory, and promotions more effectively for similar future events, maximizing sales opportunities. 

<img width="754" alt="Q7" src="https://github.com/user-attachments/assets/df6cc45e-93d4-4431-b128-2109961bc736">

### Query #8: Which customers have total loyalty points greater than 75?
This query is relevant from a managerial perspective because it identifies the customers with greater that 75 loyalty points which allows managers to recognize and reward their most engaged and valuable customers. This information is crucial for developing targeted marketing strategies and personalized offers, which can enhance customer retention and the customer's relationship with the store. 

<img width="793" alt="Q8" src="https://github.com/user-attachments/assets/b1daba1e-3b42-4aac-a3d5-e6e3cc21e9b3">

### Query #9: List the drinks with minimum inventory below the average. Show from least to greatest. 
This query is relevant from a managerial perspective because it monitos drinks with inventory levels below average. This information is crucial for maintaining optimal stock levels and ensuring customer satisfaction. It also helps prevent stockouts and informs reordering strategies, ultimately supporting sales and minimizing losses.

<img width="564" alt="Q9" src="https://github.com/user-attachments/assets/0f04f688-57f4-4931-8825-a675db78598b">

### Query #10: Which payment type has revenue above the average revenue?
This query is relevant from a managerial perspective because it identifies payment types with above the average revenue. This information can help managers make decisions about technology investments, such as upgrading payment systems or integrating new payment options that appeal to customers. 

<img width="907" alt="Q10" src="https://github.com/user-attachments/assets/ae11b412-3e31-4a6a-9995-ec73545e9a73">

## Database Information:

<img width="985" alt="database information" src="https://github.com/user-attachments/assets/9ff8283f-b936-4757-8083-0dbefa9a2638">

Name of the database: cs_asp54028
Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Qx; (where x is to be replaced by the query number).
