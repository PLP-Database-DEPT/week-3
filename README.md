# SQL Assignment Week 2: Customer Bill Management Queries

## Learning Objectives
- Understand and practice SQL syntax for data manipulation and retrieval.
- Perform CRUD (Create, Read, Update, Delete) operations on a database.
- Write queries with conditions, sorting, and aggregations to extract meaningful insights.
- Implement SQL transactions to ensure data integrity when performing multiple operations.
- Use joins and groupings to analyze related data from multiple tables.

---

## What You'll Need
- A computer with internet access.
- A code editor (e.g., Visual Studio Code).
- MySQL Workbench or another SQL database environment.

---

## Scenario
You are tasked with retrieving and managing data from a Bill Management System's database. The system tracks customer bills, including their status, due dates, and amounts. It also handles payments and categorizes the bills according to different categories (e.g., electronics, furniture). This assignment will help you practice SQL queries related to data retrieval, filtering, transactions, and aggregations.

---

## Submission Instructions
1. Clone the project to your local computer.
2. Create a file named `answers.sql` in your project folder.
3. Run each query on MySQL Workbench and, once successful, copy and paste the query into `answers.sql` in Visual Studio Code.
4. Use comments to document your queries. For example:
   ```sql
   -- Question 1.1
   SELECT * FROM orders;
After completing all queries, push your answers.sql file to GitHub and submit it for review.
Assignment Questions
1. Insert a New Customer
Write an SQL query to insert a new customer into the customer table with the following details:

customerName: 'Alice Johnson'
email: 'alice.johnson@example.com'
phoneNumber: '+11234567890'
customerAddress: '789 Maple Ave, Boston'
Set the dateCreated to the current timestamp.
2. Insert a Bill and Associated Items
Write an SQL query to insert a bill into the bills table for the customer with id = 1. Use the following details:

BillDate: '2024-11-15'
DueDate: '2024-12-01'
TotalAmount: 200.00
Status: 'Pending'
Assign a CategoryID of your choice.
Then, insert two associated records into the bill_items table with the following details:

ItemDescription: 'Laptop', Quantity: 1, UnitPrice: 150.00, LineTotal: 150.00
ItemDescription: 'Mouse', Quantity: 1, UnitPrice: 50.00, LineTotal: 50.00
3. Update Customer Information
Write an SQL query to update the customerAddress of the customer whose email is 'alice.johnson@example.com' to '123 Elm St, New York'.

4. Delete Unpaid Bills
Write an SQL query to delete all rows from the bills table where the Status is 'Pending' and the DueDate has already passed the current date.

5. Retrieve Customer and Their Bills
Write an SQL query to retrieve the customerName, email, and all associated BillID, BillDate, TotalAmount, and Status for each customer. Ensure customers without bills are also included.

6. Summarize Payments by Customer
Write an SQL query to calculate the total PaymentAmount for each customer. Display the customerName, email, and the total PaymentAmount.

7. Transactions for Adding a Payment
Write an SQL query to perform the following operations as a transaction:

Deduct the payment amount (e.g., 200.00) from the TotalAmount in the bills table for BillID = 2.
Insert a new payment record into the payments table with:
PaymentDate: Current date
PaymentAmount: 200.00
PaymentMethod: 'Credit Card'
BillID: 2
Commit the transaction only if both steps succeed.

8. Identify Overdue Bills
Write an SQL query to retrieve all bills where the Status is not 'Paid' and the DueDate is earlier than the current date. Show the BillID, customerName, TotalAmount, and DueDate.

9. Top Categories by Revenue
Write an SQL query to calculate the total revenue (LineTotal) for each category of items sold. Display the CategoryID, name, and the total revenue in descending order.

10. Most Active Customers
Write an SQL query to retrieve the top 5 customers who have made the highest number of payments. Show the customerName, email, and the total number of payments made by each.

11. Transactions for Updating Bill Status
Write an SQL query to perform the following operations as a transaction:

Update the Status of the bill with BillID = 3 to 'Paid'.
Insert a new payment record into the payments table with:
PaymentDate: Current date
PaymentAmount: 100.00
PaymentMethod: 'Bank Transfer'
BillID: 3
Commit the transaction only if both steps succeed.
