# SQL Tutorial -

- SQL is a standard language for =>  <i>storing, manipulating and retrieving data in databases.</i>
- Our SQL in: MySQL, SQL Server, MS Access, Oracle, Sybase, Informix, Postgres, and other database systems.
<br>

---------------------------------------------------
<br>

## Introduction to SQL -

- SQL is a standard language for <b>accessing and manipulating databases.</b>

### What is SQL?
- Structured Query Language
- SQL lets you access and manipulate databases

### What Can SQL do?
- SQL can execute queries against a database
- SQL can retrieve data from a database
- SQL can insert records in a database
- SQL can update records in a database
- SQL can delete records from a database
- SQL can create new databases
- SQL can create new tables in a database
- SQL can create stored procedures in a database
- SQL can create views in a database
- SQL can set permissions on tables, procedures, and views

<br>
-----------------------------------

SQL is a Standard - BUT....
- Although SQL is an ANSI/ISO standard, there are different versions of the SQL language.
- However, to be compliant with the ANSI standard, they all support at least the major commands (such as SELECT, UPDATE, DELETE, INSERT, WHERE) in a similar manner.

-----------------------------------<br>


### Using SQL in Web Site - 
To build a web site that shows data from a database, you will need:
- An RDBMS database program (i.e. MS Access, SQL Server, MySQL)
- To use a server-side scripting language, like PHP or ASP
- To use SQL to get the data you want
- To use HTML / CSS to style the page

RDBMS - 
- <b>Relational Database Management System.</b>
- RDBMS is the basis for SQL, and for all modern database systems such as MS SQL Server, IBM DB2, Oracle, MySQL, and Microsoft Access.
- The data in RDBMS is stored in database objects called tables. A table is a collection of related data entries and it consists of columns and rows.

E.g. -  Look at the Custmers table:

```SQL
SELECT * FROM Customers;
```

<br>

---------------------------------------------------
<br>


## SQL Syntax - 

SQL Statements
- Most of the actions you need to perform on a database are done with SQL statements.
- SQL statements consist of keywords that are easy to understand.
- SQL statement returns all records from a table named "Customers":

E.g. - Select all record from the Customers table:
```SQL
SELECT * FROM Customers;
```

> NOTE :- Keep in Mind That...
- SQL keywords are <b>NOT case sensitive</b> : select is the same as SELECT


Semicolon after SQL Statements? -
- Some database systems require a semicolon at the end of each SQL statement.
- Semicolon is the standard way to separate each SQL statement in database systems that allow more than one SQL statement to be executed in the same call to the server.

Some of The Most Important SQL Commands -
- SELECT - extracts data from a database
- UPDATE - updates data in a database
- DELETE - deletes data from a database
- INSERT INTO - inserts new data into a database
- CREATE DATABASE - creates a new database
- ALTER DATABASE - modifies a database
- CREATE TABLE - creates a new table
- ALTER TABLE - modifies a table
- DROP TABLE - deletes a table
- CREATE INDEX - creates an index (search key)
- DROP INDEX - deletes an index



<br>

---------------------------------------------------
<br>




#### Continueed










## SQL SELECT Statement -

- The SELECT statement is used to select data from a database.
E.g. - Return data from the Customers table:
```SQL
SELECT CustomerName, City FROM Customers;
```

Syntax -
```
SELECT column1, column2, ...
FROM table_name;
```

Select ALL columns - 
- If you want to return all columns, without specifying every column name, you can use the <b>SELECT * </b> syntax:
E.g. - Return all the columns from the Customers table:
SELECT * FROM Customers;

---------------------------------------------------------

SQL SELECT DISTINCT Statement -

- The SELECT DISTINCT statement is used to return only distinct (different) values.

E.g. - Select all the different countries from the "Customers" table:
SELECT DISTINCT Country FROM Customers;

Syntax
SELECT DISTINCT column1, column2, ...
FROM table_name;



SELECT Example Without DISTINCT -
If you omit the DISTINCT keyword, the SQL statement returns the "Country" value from all the records of the "Customers" table:

E.g. -
SELECT Country FROM Customers;


Count Distinct -
By using the DISTINCT keyword in a function called COUNT, we can return the number of different countries.

E.g. -
SELECT COUNT(DISTINCT Country) FROM Customers;


-----------------------------------------------------


SQL WHERE Clause - 
- The WHERE clause is used to filter records.
- It is used to extract only those records that fulfill a specified condition.

E.g. - 
Select all customers from Mexico:

SELECT * FROM Customers
WHERE Country='Mexico';


Syntax 
SELECT column1, column2, ...
FROM table_name
WHERE condition;


Note: The WHERE clause is not only used in SELECT statements, it is also used in UPDATE, DELETE, etc.!


Text Fields vs. Numeric Fields -

SQL requires single quotes around text values (most database systems will also allow double quotes).

However, numeric fields should not be enclosed in quotes:

E.g. -
SELECT * FROM Customers
WHERE CustomerID=1;


Operators in The WHERE Clause -
You can use other operators than the = operator to filter the search.

E.g. - 
Select all customers with a CustomerID greater than 80:

SELECT * FROM Customers
WHERE CustomerID > 80;

The following operators can be used in the WHERE clause:

Operator -
=	       Equal	
>	       Greater than	
<	       Less than	
>=	     Greater than or equal	
<=	     Less than or equal	
<>	     Not equal. Note: In some versions of SQL this operator may be written as !=	
BETWEEN	 Between a certain range	
LIKE	   Search for a pattern	
IN	     To specify multiple possible values for a column


Exercise:
Select all records where the City column has the value "Berlin".

SELECT * FROM Customers
WHERE city = "Berlin";


-----------------------------------


