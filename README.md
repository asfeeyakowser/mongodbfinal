# Exp 7 CRUD Operations on Products Collection using MongoDB

**Date:**

## AIM:

To implement **CRUD (Create, Read, Update, and Delete) Operations using MongoDB** on a Products collection to store, retrieve, modify, and delete product information.

## DESIGN STEPS:

### Step 1:

Fork the given repository and clone the forked repository from GitHub.

### Step 2:

Open **MongoDB Shell (mongosh)** or MongoDB Compass and create a database for storing product information.

### Step 3:

Create a collection named **Products** with the fields **id, name, brand, price, category, stock,** and **tags**.

### Step 4:

Insert the following product records into the Products collection.

| id | name       | brand    | price | category    | stock | tags                       |
| -- | ---------- | -------- | ----: | ----------- | ----: | -------------------------- |
| 1  | Laptop     | Dell     | 55000 | Electronics |    30 | ["computer", "technology"] |
| 2  | Smartphone | Samsung  | 30000 | Electronics |    50 | ["mobile", "android"]      |
| 3  | Headphones | Sony     |  2500 | Accessories |   100 | ["audio", "music"]         |
| 4  | Smartwatch | Apple    | 45000 | Electronics |    20 | ["wearable", "ios"]        |
| 5  | Keyboard   | Logitech |  1200 | Accessories |    80 | ["computer", "typing"]     |

### Step 5:

Perform the **Create operation** by inserting all the given product documents into the Products collection.

### Step 6:

Perform the **Read operation** to display all the documents available in the Products collection.

### Step 7:

Retrieve products based on conditions such as **product ID, category, price, brand, stock,** and **tags**.

### Step 8:

Perform the **Update operation** to modify selected product information such as **price, stock,** or **tags**.

### Step 9:

Perform an update operation on multiple documents belonging to a particular product category.

### Step 10:

Perform the **Delete operation** to remove a selected product document from the Products collection.

### Step 11:

Display the final Products collection and verify the changes made through the CRUD operations.

### Step 12:

Execute all the MongoDB commands, capture the required outputs, commit the completed experiment, and push the changes to the forked GitHub repository.

## PROGRAM:
To create a database

use mydb To create collection "product"

db.createCollection("products") To insert all documents in product collections

db.products.insertMany([ { _id: 1, name: "Laptop", brand: "Dell", price: 55000, category: "Electronics", stock: 30, tags: ["computer", "technology"] }, { _id: 2, name: "Smartphone", brand: "Samsung", price: 30000, category: "Electronics", stock: 50, tags: ["mobile", "android"] }, { _id: 3, name: "Headphones", brand: "Sony", price: 2500, category: "Accessories", stock: 100, tags: ["audio", "music"] }, { _id: 4, name: "Smartwatch", brand: "Apple", price: 45000, category: "Electronics", stock: 20, tags: ["wearable", "ios"] }, { _id: 5, name: "Keyboard", brand: "Logitech", price: 1200, category: "Accessories", stock: 80, tags: ["computer", "typing"] } ]) To read all documents in product collections

db.products.find().pretty() To read products below 5000

db.products.find({ price: { $lt: 5000 } }) To read only accessories

db.products.find({ category: "Accessories" }) To read electronics below 50,000

db.products.find({ $and: [ { category: "Electronics" }, { price: { $lt: 50000 } } ] }) To update laptop price

db.products.updateOne( { name: "Laptop" }, { $set: { price: 52000 } } ) To increase keyboard stock by 10

db.products.updateOne( { name: "Keyboard" }, { $inc: { stock: 10 } } ) To add premium tag to smartwatch

db.products.updateOne( { name: "Smartwatch" }, { $push: { tags: "premium" } } ) To delete Keyboard

db.products.deleteOne({ name: "Keyboard" })

## OUTPUT:
After Insertions

<img width="806" height="93" alt="image" src="https://github.com/user-attachments/assets/63ef700a-60a4-4797-85a4-98a049a78cfb" />

After read operation

<img width="442" height="722" alt="image" src="https://github.com/user-attachments/assets/0955c389-620f-48f2-9e32-2f5ea6d3b968" />

To read products below 5000

<img width="555" height="482" alt="image" src="https://github.com/user-attachments/assets/42f0bdd9-2606-41c9-b7f0-9773741dd13f" />

To read only accessories

<img width="541" height="470" alt="image" src="https://github.com/user-attachments/assets/bead638e-7357-434c-a0fc-3b03d48bc567" />

To read electronics below 50,000

<img width="690" height="455" alt="image" src="https://github.com/user-attachments/assets/41b22124-df85-4e9b-ab47-e92356282467" />

After updating the product collections

<img width="526" height="721" alt="image" src="https://github.com/user-attachments/assets/2db6bf11-d99c-496b-b159-ab730d54ef6f" />

After delete operation in product collection

<img width="525" height="643" alt="image" src="https://github.com/user-attachments/assets/60fa66b1-7a2f-444b-b427-bfc6186c6703" />



## RESULT:

The **CRUD Operations on the Products Collection using MongoDB** were implemented successfully. The product documents were created, retrieved, updated, and deleted using appropriate MongoDB commands, and the final changes were successfully verified in the Products collection.
