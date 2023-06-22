## Ex-08 Implement the keyword Case Cross Join full outer join
## AIM:-
To write a sql query to perform keyword- Case,Cross Join,full outer join in SQL.

## PROCEDURE:-
### STEP 1:
create database KEY_FUNCTION .

### STEP 2:
create table TableA,TableB,Employees.

### STEP 3:
Insert Value to the tables.

### STEP 4:
Perform Case on Employees and Cross Join,full outer join on TableA,TableB.

## PROGRAM:-
#### Developed By : Sarankumar J
#### Register Number : 212221230087
```sql
CREATE DATABASE KEY_FUNCTION;
USE KEY_FUNCTION;
CREATE TABLE TableA (
  ID INT PRIMARY KEY,
  Name VARCHAR(50)
);
CREATE TABLE TableB (
  ID INT PRIMARY KEY,
  Name VARCHAR(50)
);
CREATE TABLE Employees (
  ID INT PRIMARY KEY,
  FirstName VARCHAR(50),
  LastName VARCHAR(50),
  Salary DECIMAL(10, 2),
  Department VARCHAR(50)
);
INSERT INTO TableA (ID, Name) VALUES
(1, 'John'),
(2, 'Alice'),
(3, 'Mike');
INSERT INTO TableB (ID, Name) VALUES
(4, 'Sarah'),
(5, 'Tom'),
(6, 'Emily');
INSERT INTO Employees (ID, FirstName, LastName, Salary, Department) VALUES
(1, 'John', 'Doe', 50000.00, 'HR'),
(2, 'Jane', 'Smith', 60000.00, 'Finance'),
(3, 'Michael', 'Johnson', 75000.00, 'IT'),
(4, 'Emily', 'Davis', 55000.00, 'Marketing'),
(5, 'David', 'Brown', 70000.00, 'Finance');

SELECT *
FROM TableA
CROSS JOIN TableB;

SELECT *
FROM TableA
FULL OUTER JOIN TableB ON TableA.ID = TableB.ID;

SELECT ID, Salary,
  CASE
    WHEN Salary < 50000 THEN 'Low'
    WHEN Salary >= 50000 AND Salary < 100000 THEN 'Medium'
    WHEN Salary >= 100000 THEN 'High'
    ELSE 'Unknown'
  END AS SalaryRange
FROM Employees;
```
## OUTPUT:-
![git](./op1.png)

![git](./op2.png)

![git](./op3.png)
## RESULT:-
A sql query to perform keyword- Case,Cross Join,full outer join in SQL has been executed.
