# EX.NO 4 Data Control Language (DCL) Commands and Transaction Control Languages (TCL) in SQL
### DATE:
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## Data Control Language (DCL) commands
* Data control language (DCL) is used to access the stored data.
* It is mainly used for revoke and to grant the user the required access to a database.
## List of DCL commands: 
1. GRANT : It is used to insert data into a table.
2. REVOKE: It is used to update existing data within a table.
## Transaction control language(TCL) commands
1. COMMIT : COMMIT command in SQL is used to save all the transaction-related changes permanently to the disk
2. START TRANSACTION : to start the transaction
3. ROLLBACK : undo the transaction upto savepoint 
4. SAVEPOINT : create a savepoint to save the different parts of the same transaction using different names

### Q1) Create a table employee with employee id ,name and Address

### QUERY:
```
sql
create table employee(
emp_id numeric,
emp_name varchar(10),
addr varchar(40)
);
```


### OUTPUT:

![Screenshot 2024-04-03 110934](https://github.com/divyadivya10/DBMS/assets/119560271/9be3acf9-3f58-48bf-8492-b27d65d90240)

### Q2) Insert three rows into emploee table 


### QUERY:
```
insert into employee values(1,'Luffy','EastBlue');
insert into employee values(2,'Shanks','GodValley');
insert into employee values(3,'Grap','MarinFord');
```


### OUTPUT:
![Screenshot 2024-04-03 111003](https://github.com/divyadivya10/DBMS/assets/119560271/26b903d3-b62f-4ea3-b3a4-ee9b4a746794)


### Q3) Start the transaction and create a save point s1.

### QUERY:
```
savepoint A;
```

### OUTPUT:

![Screenshot 2024-04-03 111014](https://github.com/divyadivya10/DBMS/assets/119560271/ce87e8b6-8052-4490-a515-c95938cc4a08)


### Q4) Perform insertion into employee table.

### QUERY:

```
insert into employee(4,'Robin','EniesLobby');
```

### OUTPUT:
![Screenshot 2024-04-03 111048](https://github.com/divyadivya10/DBMS/assets/119560271/9cacafb7-d1a3-45b8-9232-efa1ae8fbb33)



### Q5)	Display the employee table and create a save point s2 .


### QUERY:
```
insert into employee(4,'Robin','EniesLobby');
```



### OUTPUT:
![Screenshot 2024-04-03 111110](https://github.com/divyadivya10/DBMS/assets/119560271/44e06c0d-40a6-4555-a9bb-50c34238f611)


### Q6)	Perform updation on any one of the row.


### QUERY:
```
sql
update employee set emp_name='Nico Robin' where emp_id=4;
```

### OUTPUT:
![Screenshot 2024-04-03 111119](https://github.com/divyadivya10/DBMS/assets/119560271/5a3e272f-e63d-44aa-8258-87ae375f28e5)



### Q7) Display the employee table and rollback to  save point s2 


### QUERY:
```
sql
select * from employee;
rollback to s2;
```


### OUTPUT:
![Screenshot 2024-04-03 111130](https://github.com/divyadivya10/DBMS/assets/119560271/bc50238d-1533-44ed-b308-b69a5d8db936)


### Q8) Display the employee table and commit the changes; 


### QUERY:
```
sql
select * from employee;
commit;
```


### OUTPUT:
![Screenshot 2024-04-03 111143](https://github.com/divyadivya10/DBMS/assets/119560271/5286580e-881d-4274-9ec3-90131109dc20)



### Q9) Rollback to save point s1;


### QUERY:
```
sql
rollback to A;
```


### OUTPUT:
![Screenshot 2024-04-03 111155](https://github.com/divyadivya10/DBMS/assets/119560271/607591af-36b3-4a1a-9d6f-81102ed6b06a)



### Q10)	Create a new user and grant access to any one database with "insert and update"


### QUERY:
```
CREATE USER new_user;
GRANT INSERT, UPDATE ON database_name TO new_user;
```


### OUTPUT:
![Screenshot 2024-04-03 111207](https://github.com/divyadivya10/DBMS/assets/119560271/72c24e64-00e4-487e-8f82-017688f19195)



### Q11) Check the user access and display the result 


### QUERY:
```
SHOW GRANTS FOR new_user;
```


### OUTPUT:
![Screenshot 2024-04-03 111216](https://github.com/divyadivya10/DBMS/assets/119560271/fd0beef2-396a-412a-bd81-39977821db30)



### Q12) Revoke the privillages.

### QUERY:
```
SHOW GRANTS FOR new_user;
REVOKE INSERT, UPDATE ON database_name FROM new_user;
SHOW GRANTS FOR new_user;
```


### OUTPUT:
![Screenshot 2024-04-03 111314](https://github.com/divyadivya10/DBMS/assets/119560271/9c1a012f-e0d8-46eb-97a4-769fdb42d6e5)



## RESULT :
Thus the basic TCL and DCL commands are executed.
