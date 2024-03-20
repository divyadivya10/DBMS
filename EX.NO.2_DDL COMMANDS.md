# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS 
### DATE
## AIM:
To create a student database and execute DDL queries using SQL.


## THEORY
### DDL (Data Definition Language)

* DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema.
* It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.
* DDL is a set of SQL commands used to create, modify, and delete database structures but not data.
* These commands are normally not used by a general user, who should be accessing the database via an application.

 
### List of DDL commands: 
1. CREATE: This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
2. DROP: This command is used to delete objects from the database.
3. ALTER: This is used to alter the structure of the database.
4. TRUNCATE: This is used to remove all records from a table, including all spaces allocated for the records are removed.
5. RENAME: This is used to rename an object existing in the database.

## Query:
### 1) Create a database studentdb

### SQL QUERY:

create database studentdbb;

### OUTPUT:

![Screenshot 2024-03-20 101914](https://github.com/divyadivya10/DBMS/assets/119560271/f3cd8cef-2b4a-48e4-bedc-7a1b3348ea5e)

### 2) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 

create table student(RegisterNumber int,Name varchar(100),Age int,Address varchar(250),PhoneNumber int) ;


### OUTPUT:

![Screenshot 2024-03-20 101926](https://github.com/divyadivya10/DBMS/assets/119560271/84cec1e9-374b-49b9-8bc6-4e7ea4e72e35)


### 3) Alter the above student table by adding another attribute department

### SQL QUERY: 

 alter table student add dept varchar(20);


### OUTPUT:

![Screenshot 2024-03-20 101936](https://github.com/divyadivya10/DBMS/assets/119560271/ff418c45-1970-4aac-a534-19a8964d45a1)




### 4) Rename the student table to mystudent

### SQL QUERY: 

rename table student to mystudent;

### OUTPUT:

![Screenshot 2024-03-20 102245](https://github.com/divyadivya10/DBMS/assets/119560271/3d4f28d0-cf0a-4605-8991-98287638932a)


### 5) Delete the mystudent rows using truncate keyword

### SQL QUERY: 

truncate table mystudent;


### OUTPUT:

![Screenshot 2024-03-20 102334](https://github.com/divyadivya10/DBMS/assets/119560271/3c1b3d3a-c59c-41cb-97b6-7037290807d0)

### 4) Drop the mystudent table
 
### SQL QUERY: 

drop table mystudent;

### OUTPUT:

![image](https://github.com/divyadivya10/DBMS/assets/119560271/2775f330-d889-4f0e-b014-92b8a7df52d7)



## Result:
         Thus the basic DDL commands in SQL are executed. 


