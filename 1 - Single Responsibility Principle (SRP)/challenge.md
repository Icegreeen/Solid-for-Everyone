### Challenge: Product Management System

You have been hired to develop a product management system for an online store. The system should allow adding, removing, updating, and listing products. Additionally, it should also calculate the total price of a purchase, including fee calculation.

Requirements:

1 - Implement separate classes to perform the following operations: 

- [ ]  **ProductManager**: Responsible for managing products, including addition, removal, updating, and listing.
-  [ ] **PriceCalculator**: Responsible for calculating the total price of a purchase, including fees.

2 - The ProductManager class should have the following methods:

- [ ] **addProduct(product: Product): void**: Adds a new product to the list of products.
- [ ] **removeProduct(productId: string)**: void: Removes a product from the list of products based on its ID.
- [ ] **updateProduct(productId: string, updatedProduct: Product): void**: Updates the information of an existing product based on its ID.
- [ ] **listProducts(): Product[]**: Returns a list of all currently available products.

3 - The PriceCalculator class should have the following method:

- [ ] **calculateTotalPrice(products: Product[])**: number: Calculates the total price of a purchase, including the price of all products and applicable fees.

4 - Each product should be represented by an object with the following properties:

- [ ] **id:** Unique identifier of the product (string).
- [ ] **name:** Name of the product (string).
- [ ] **price:** Unit price of the product (number).
- [ ] **quantity:** Quantity of the product (number).

5 - The system should calculate a 5% fee on the total purchase price.

### Instructions:

- Implement the classes according to the above requirements in TypeScript.
- You may simulate storing products in memory; it is not necessary to persist the data in a database.
- Create instances of the classes and demonstrate the system's functionality with examples of adding, removing, updating, and listing products, as well as calculating the total price of a purchase.

### Notes:

- Make sure to follow the Single Responsibility Principle (SRP) when implementing the classes.
- Test your code with different scenarios to ensure it functions correctly in various situations.