# EX 3 SubQueries, Views and Joins 


## Create employee Table
```sql
CREATE TABLE EMP (EMPNO NUMBER(4) PRIMARY KEY,ENAME VARCHAR2(10),JOB VARCHAR2(9),MGR NUMBER(4),HIREDATE DATE,SAL NUMBER(7,2),COMM NUMBER(7,2),DEPTNO NUMBER(2));
```
## Insert the values
```sql
INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7369, 'SMITH', 'CLERK', 7902, '17-DEC-80', 800, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7499, 'ALLEN', 'SALESMAN', 7698, '20-FEB-81', 1600, 300, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7521, 'WARD', 'SALESMAN', 7698, '22-FEB-81', 1250, 500, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7566, 'JONES', 'MANAGER', 7839, '02-APR-81', 2975, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7654, 'MARTIN', 'SALESMAN', 7698, '28-SEP-81', 1250, 1400, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7698, 'BLAKE', 'MANAGER', 7839, '01-MAY-81', 2850, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7782, 'CLARK', 'MANAGER', 7839, '09-JUN-81', 2450, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7788, 'SCOTT', 'ANALYST', 7566, '19-APR-87', 3000, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7839, 'KING', 'PRESIDENT', NULL, '17-NOV-81', 5000, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7844, 'TURNER', 'SALESMAN', 7698, '08-SEP-81', 1500, 0, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7876, 'ADAMS', 'CLERK', 7788, '23-MAY-87', 1100, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7900, 'JAMES', 'CLERK', 7698, '03-DEC-81', 950, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7902, 'FORD', 'ANALYST', 7566, TO_DATE('03-DEC-81', 'DD-MON-RR'), 3000, 20, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7934, 'MILLER', 'CLERK', 7782, TO_DATE('23-JAN-82', 'DD-MON-RR'), 1300, 10, 10);
```

## Create department table
```sql
CREATE TABLE DEPT (DEPTNO NUMBER(2) PRIMARY KEY,DNAME VARCHAR2(14),LOC VARCHAR2(13));
```
## Insert the values in the department table
```sql
INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (10, 'ACCOUNTING', 'NEW YORK');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (20, 'RESEARCH', 'DALLAS');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (30, 'SALES', 'CHICAGO');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (40, 'OPERATIONS', 'BOSTON');
```

### Q1) List the name of the employees whose salary is greater than that of employee with empno 7566.


### QUERY:
![image](https://github.com/MohammedFaizal05/EX-3-SubQueries-Views-and-Joins/assets/120553195/c7feb8db-e943-43f6-857a-1be5640fd3cf)


### OUTPUT:
![image](https://github.com/MohammedFaizal05/EX-3-SubQueries-Views-and-Joins/assets/120553195/6d5579a7-34f5-4130-91ad-e24d4cbe8af5)

### Q2) List the ename,job,sal of the employee who get minimum salary in the company.

### QUERY:

![image](https://github.com/MohammedFaizal05/EX-3-SubQueries-Views-and-Joins/assets/120553195/40b90a39-0993-4f55-a85e-0e58bf3e618a)

### OUTPUT:
![image](https://github.com/MohammedFaizal05/EX-3-SubQueries-Views-and-Joins/assets/120553195/9f29e108-8f59-4cea-9a37-a264c3b7ebbd)

### Q3) List ename, job of the employees who work in deptno 10 and his/her job is any one of the job in the department ‘SALES’.

### QUERY:
![image](https://github.com/MohammedFaizal05/EX-3-SubQueries-Views-and-Joins/assets/120553195/71183847-8ee4-430f-bd0f-679833ba36fd)


### OUTPUT:

![image](https://github.com/MohammedFaizal05/EX-3-SubQueries-Views-and-Joins/assets/120553195/455b4228-3bbc-4f66-a171-8fbba71a0250)

### Q4) Create a view empv5 (for the table emp) that contains empno, ename, job of the employees who work in dept 10.

### QUERY:
![image](https://github.com/MohammedFaizal05/EX-3-SubQueries-Views-and-Joins/assets/120553195/d45efc2f-de42-466e-979e-c78a92bbc156)


### OUTPUT:
![image](https://github.com/MohammedFaizal05/EX-3-SubQueries-Views-and-Joins/assets/120553195/b2f9551d-da3c-4f2f-94cd-ec7b81fa9119)

### Q5) Create a view with column aliases empv30 that contains empno, ename, sal of the employees who work in dept 30. Also display the contents of the view.

### QUERY:
```
CREATE VIEW emv30 AS SELECT empno AS "Employee Number",ename AS "Employee Nmae",sal AS "Salary" from em WHERE deptno = 30;
SELECT * FROM emv30;
```
### OUTPUT:
![image](https://github.com/MohammedFaizal05/EX-3-SubQueries-Views-and-Joins/assets/120553195/86c4f9f3-49b2-4dc1-9aa5-e571d360b99f)

### Q6) Update the view empv5 by increasing 10% salary of the employees who work as ‘CLERK’. Also confirm the modifications in emp table

### QUERY:
```
UPDATE emv5 SET sal = al * 1.1 WHERE job = 'CLERK';
```

### OUTPUT:
![image](https://github.com/MohammedFaizal05/EX-3-SubQueries-Views-and-Joins/assets/120553195/4a61addb-cdc1-4ee9-9468-9adc073a6b24)

## Create a Customer1 Table
```sql
CREATE TABLE Customer1 (customer_id INT,cust_name VARCHAR(20),city VARCHAR(20),grade INT,salesman_id INT);
```
## Inserting Values to the Table
```sql
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3002, 'Nick Rimando', 'New York', 100, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3007, 'Brad Davis', 'New York', 200, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3005, 'Graham Zusi', 'California', 200, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3008, 'Julian Green', 'London', 300, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3004, 'Fabian Johnson', 'Paris', 300, 5006);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3009, 'Geoff Cameron', 'Berlin', 100, 5003);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3003, 'Jozy Altidor', 'Moscow', 200, 5007);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3001, 'Brad Guzan', 'London', NULL, 5005);
```
## Create a Salesperson1 table
```sql
CREATE TABLE Salesman1 (salesman_id INT,name VARCHAR(20),city VARCHAR(20),commission DECIMAL(4,2));
```
## Inserting Values to the Table
```sql
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5001, 'James Hoog', 'New York', 0.15);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5002, 'Nail Knite', 'Paris', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5005, 'Pit Alex', 'London', 0.11);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5006, 'Mc Lyon', 'Paris', 0.14);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5007, 'Paul Adam', 'Rome', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5003, 'Lauson Hen', 'San Jose', 0.12);
```
### Q7) Write a SQL query to find the salesperson and customer who reside in the same city. Return Salesman, cust_name and city.

### QUERY:
```
SELECT salesman1.name AS "Salesman",customer1.cust_name AS "Customer Name",sales1.city AS "City" from salesman1 INNER JOIN customer1 ON salesman1.city = customer.city;
```

### OUTPUT:
![image](https://github.com/MohammedFaizal05/EX-3-SubQueries-Views-and-Joins/assets/120553195/ffb6c51c-957f-447e-b1be-91a1ead454a5)

### Q8) Write a SQL query to find salespeople who received commissions of more than 13 percent from the company. Return Customer Name, customer city, Salesman, commission.


### QUERY:
```
SELECT customer1.cust_name AS "Customer Name",customer1.city AS "Customer City",salesman1.name AS "Salesman",salesman1.commission AS "Commission" FROM salesman1 INNER JOIN customer1 ON salesman.salesman_id = customer1.salesman_id WHERE salesman1.commission  > 0.13;
```

### OUTPUT:
![image](https://github.com/MohammedFaizal05/EX-3-SubQueries-Views-and-Joins/assets/120553195/ca6bc269-ae15-446b-83f0-d511fcd36b90)

### Q9) Perform Natural join on both tables

### QUERY:

```
SELECT customer1.cust_name AS "Customer Name",customer1.city AS "Customer City",salesman1.name AS "Salesman",salesman1.commission AS "Commission" FROM salesman1 INNER JOIN customer1 ON salesman.salesman_id = customer1.salesman_id WHERE salesman1.commission  > 0.13;
```
### OUTPUT:
![image](https://github.com/MohammedFaizal05/EX-3-SubQueries-Views-and-Joins/assets/120553195/55d331db-43f5-4e3a-8cbe-039103c0dc56)

### Q10) Perform Left and right join on both tables

### QUERY:

### LEFT JOIN:
```
SELECT * FROM salesman1 LEFT JOIN customer1 ON salesman1.salesman_id = customer1.salesman_id;
```
### OUTPUT:
![image](https://github.com/MohammedFaizal05/EX-3-SubQueries-Views-and-Joins/assets/120553195/c277c7e3-c7a1-4355-b52a-74afe06025e1)
### RIGHT JOIN:
```
SELECT * FROM salesman1 RIGHT JOIN customer1 ON salesman1.salesman_id = customer1.salesman_id;
```
### OUTPUT:
![image](https://github.com/MohammedFaizal05/EX-3-SubQueries-Views-and-Joins/assets/120553195/f50c0fe8-d075-46c8-a0a1-b13349135b57)

### RESULT:
Hence successfully created SubQueries, Views and Joins.
