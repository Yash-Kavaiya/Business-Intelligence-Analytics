# INTRODUCTION TO SQL
PRE REQUISITES
• Learn basic SQL Queries
https://www.mysqltutorial.org/
Installing and Using MySQL with Workbench
https://dev.mysql.com/doc/workbench/en/
https://www.mysq|tutorial.org (SQL tutorial for MySQL database)
• Case: Retail operations at Smartsense
Create a schema and Import the tables

Sure, let's delve into these concepts:

1. **Database**: A database is a structured set of data. So, a computer database is a structured set of data stored in a computer, especially one that is accessible in various ways. A Database Management System (DBMS) is the software that interacts with end users, applications, and the database itself to capture and analyze the data.

2. **Relational DBMS (RDBMS)**: This type of DBMS defines database relationships in terms of tables, also known as relations. Unlike a spreadsheet, an RDBMS doesn't store all data in one large table, but distributes it across multiple tables. These tables are linked to each other using relationships. The SQL (Structured Query Language) is used to manage and query data in RDBMS. MySQL is an example of a relational DBMS.

3. **Non-Relational DBMS (NoSQL)**: This type of DBMS is designed to overcome the limitations of RDBMS for certain use cases involving large amounts of rapidly changing, diverse data. Instead of tables, NoSQL databases might store data in key-value pairs, wide-column stores, graph formats or documents. They do not typically use SQL for querying data.

Let's break down the two types further:

- **Relational DBMS (MySQL)**: In a relational database, data is organized into one or more tables, each with a unique key identifying each row in the table. These keys can be used to connect one table of data to another, creating a relationship between them. For example, you might have one table containing product information and another containing supplier information. By creating a relationship between the 'Supplier ID' fields in each table, you can create a link that lets you find all products supplied by a particular supplier.

- **Non-Relational DBMS (NoSQL)**: Non-relational databases, or NoSQL databases, can be thought of as "not only SQL" as they may support SQL-like query languages. They are particularly useful for working with large sets of distributed data. NoSQL databases come in a variety of types based on their data model. The main types are document, key-value, wide-column, and graph. They provide flexible schemas and scale easily with large amounts of data and high user loads.

Extra Material :-Database Fundamentals 
https://medium.com/@yash.kavaiya3/database-fundamentals-day-1-100daysofdatascience-f0f34b3871f8

Database and DBMS
https://medium.com/@yash.kavaiya3/database-and-dbms-day-2-100daysofdatascience-72af5b6e78c2

SQL BASICS
• SQL is not a case-sensitive language.
• In MySQL, every statement must be terminated wi
RDBMS is the basis for SQL, and for all modern di
such as MS SQL Server, IBM DB2, Oracle, MySQL
Access.
The data in RDBMS is stored in database objects
table is a collection of related data entries and it consists of
columns and rows.

FIELDS AND RECORDS
• Every table is broken up into smaller entities called fields.
• (Eg: CustomerID, CustomerName, ContactName, Address, City, PostalCode and
Country).
• A field is a column in a table that is designed to maintain specific information
about every record in the table.
• A record, also called a row, is each individual entry that exists in a table.
• A record is a horizontal entity in a table.
• A column is a vertical entity in a table that contains all information associated with a specific field in a table.

Sure, here are the markdown notes for the database schema and the table you provided:

## Database/Schema
A **database** most often contains one or more tables. Each table is identified by a name (e.g., "Customers" or "Orders"). Tables contain records (rows) with data.

## Table: Customers
The "Customers" table contains five records (one for each customer) and seven columns (Cust ID, Cust Name, Contact Name, Address, City, Postal Code, and Country).

Here's the table in markdown format:

| Cust ID | Cust Name | Contact Name | Address | City | Postal Code | Country |
|---------|-----------|--------------|---------|------|-------------|---------|
| 1 | Rajeswari | Raji | 57, Rome | Rome | 12209 | Italy |
| 2 | Anuja | Anu | 120 Hanover St | London | 45465 | UK |
| 3 | Subhashree | Subha | YZ | Mexico | 51544 | Mexico |
| 4 | Jonathan | John | ABC | Chennai | 646965 | India |
| 5 | Alfredo | Alfred | QWRS | Trivandrum | 444455 | India |

Each row in the table represents a customer, with their details spread across the columns. For example, the customer with Cust ID 1 is named Rajeswari, goes by the contact name Raji, lives at 57, Rome in Rome, Italy, and has the postal code 12209.


