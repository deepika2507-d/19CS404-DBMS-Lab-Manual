# Experiment 6: Joins

## AIM
To study and implement different types of joins.

## THEORY

SQL Joins are used to combine records from two or more tables based on a related column.

### 1. INNER JOIN
Returns records with matching values in both tables.

**Syntax:**
```sql
SELECT columns
FROM table1
INNER JOIN table2
ON table1.column = table2.column;
```

### 2. LEFT JOIN
Returns all records from the left table, and matched records from the right.

**Syntax:**

```sql
SELECT columns
FROM table1
LEFT JOIN table2
ON table1.column = table2.column;
```
### 3. RIGHT JOIN
Returns all records from the right table, and matched records from the left.

**Syntax:**

```sql
SELECT columns
FROM table1
RIGHT JOIN table2
ON table1.column = table2.column;
```
### 4. FULL OUTER JOIN
Returns all records when there is a match in either left or right table.

**Syntax:**

```sql
SELECT columns
FROM table1
FULL OUTER JOIN table2
ON table1.column = table2.column;
```

**Question 1**
From the following tables write a SQL query to find those orders where the order amount exists between 500 and 2000. Return ord_no, purch_amt, cust_name, city.

Sample table: customer

customer_id | cust_name | city | grade | salesman_id

<img width="604" height="242" alt="image" src="https://github.com/user-attachments/assets/82aa7d13-fe75-4c49-b151-9f839f7b05f2" />

Sample table: orders

ord_no purch_amt ord_date customer_id salesman_id

70001 150.5 2012-10-05 3005 5002

70009 270.65 2012-09-10 3001 5005

70002 65.26 2012-10-05 3002 5001

70004 110.5 2012-08-17 3009 5003

70007 948.5 2012-09-10 3005 5002

70005 2400.6 2012-07-27 3007 5001

70008 5760 2012-09-10 3002 5001

70010 1983.43 2012-10-10 3004 5006

70003 2480.4 2012-10-10 3009 5003

70012 250.45 2012-06-27 3008 5002

70011 75.29 2012-08-17 3003 5007

70013 3045.6 2012-04-25 3002 5001
```sql
SELECT o.ord_no, o.purch_amt, c.cust_name, c.city FROM orders o JOIN customer c ON o.customer_id = c.customer_id WHERE o.purch_amt BETWEEN 500 AND 2000;
```

**Output:**
<img width="1207" height="663" alt="image" src="https://github.com/user-attachments/assets/aea00476-df8b-4e6a-b532-71d22676623f" />


**Question 2**
---
SQL statement to generate a report with customer name, city, order number, order date, order amount, salesperson name, and commission to determine if any of the existing customers have not placed orders or if they have placed orders through their salesman or by themselves.

Sample table: customer

customer_id | cust_name | city | grade | salesman_id

    3002 | Nick Rimando   | New York   |   100 |        5001

    3007 | Brad Davis     | New York   |   200 |        5001
    
    3005 | Graham Zusi    | California |   200 |        5002
    
    3008 | Julian Green   | London     |   300 |        5002
    
    3004 | Fabian Johnson | Paris      |   300 |        5006
    
    3009 | Geoff Cameron  | Berlin     |   100 |        5003
    
    3003 | Jozy Altidor   | Moscow     |   200 |        5007
    
    3001 | Brad Guzan     | London     |       |        5005
Sample table: orders

ord_no purch_amt ord_date customer_id salesman_id

70001 150.5 2012-10-05 3005 5002

70009 270.65 2012-09-10 3001 5005

70002 65.26 2012-10-05 3002 5001

70004 110.5 2012-08-17 3009 5003

70007 948.5 2012-09-10 3005 5002

70005 2400.6 2012-07-27 3007 5001

70008 5760 2012-09-10 3002 5001

70010 1983.43 2012-10-10 3004 5006

70003 2480.4 2012-10-10 3009 5003

70012 250.45 2012-06-27 3008 5002

70011 75.29 2012-08-17 3003 5007

70013 3045.6 2012-04-25 3002 5001

Sample table: salesman

salesman_id | name | city | commission
```sql
SELECT c.cust_name, c.city, o.ord_no, o.ord_date, o.purch_amt AS "Order Amount", s.name, s.commission FROM customer c LEFT JOIN orders o ON c.customer_id=o.customer_id LEFT JOIN salesman s ON c.salesman_id=s.salesman_id;
```

**Output:**
<img width="1219" height="686" alt="image" src="https://github.com/user-attachments/assets/c24e5561-83ec-48af-8df2-f8f9560d1f1b" />

<img width="1232" height="732" alt="image" src="https://github.com/user-attachments/assets/f60093bc-0a57-46d1-9c2d-93f90e39b385" />

<img width="1238" height="593" alt="image" src="https://github.com/user-attachments/assets/a3c1b6a6-5363-4c03-a044-b95f1ca5f824" />

**Question 3**
---
Write a SQL statement to make a report with customer name, city, order number, order date, and order amount in ascending order according to the order date to determine whether any of the existing customers have placed an order or not.

Sample table: orders

ord_no purch_amt ord_date customer_id salesman_id

70001 150.5 2012-10-05 3005 5002

70009 270.65 2012-09-10 3001 5005

70002 65.26 2012-10-05 3002 5001

70004 110.5 2012-08-17 3009 5003

70007 948.5 2012-09-10 3005 5002

70005 2400.6 2012-07-27 3007 5001

70008 5760 2012-09-10 3002 5001

70010 1983.43 2012-10-10 3004 5006

70003 2480.4 2012-10-10 3009 5003

70012 250.45 2012-06-27 3008 5002

70011 75.29 2012-08-17 3003 5007

70013 3045.6 2012-04-25 3002 5001

Sample table: customer

customer_id | cust_name | city | grade | salesman_id

    3002 | Nick Rimando   | New York   |   100 |        5001

    3007 | Brad Davis     | New York   |   200 |        5001
    
    3005 | Graham Zusi    | California |   200 |        5002
    
    3008 | Julian Green   | London     |   300 |        5002
    
    3004 | Fabian Johnson | Paris      |   300 |        5006
    
    3009 | Geoff Cameron  | Berlin     |   100 |        5003
    
    3003 | Jozy Altidor   | Moscow     |   200 |        5007
```sql
SELECT c.cust_name, c.city, o.ord_no, o.ord_date, o.purch_amt AS "Order Amount" FROM customer c LEFT JOIN orders o ON c.customer_id=o.customer_id ORDER BY o.ord_date ASC;
```

**Output:**

<img width="1242" height="668" alt="image" src="https://github.com/user-attachments/assets/be92f304-9437-457e-a8a5-d5daa1e61588" />

<img width="1249" height="735" alt="image" src="https://github.com/user-attachments/assets/55235c65-a347-4594-b1bb-4163dbcf2375" />

<img width="1238" height="524" alt="image" src="https://github.com/user-attachments/assets/627285f2-eb90-4e1b-8e43-66e9c4d8fb60" />



**Question 4**
---
<img width="1222" height="622" alt="image" src="https://github.com/user-attachments/assets/8a27b749-5878-42b6-88e3-befd18d9d2a2" />


```sql
SELECT n.*, d.department_name FROM nurses n INNER JOIN departments d ON n.department_id = d.department_id;
```

**Output:**
<img width="1211" height="737" alt="image" src="https://github.com/user-attachments/assets/9de743aa-f175-4e14-bb9e-61dbd7abbf1d" />

**Question 5**
---
Write an SQL query to retrieve all columns from the 'customer' table (aliased as 'c') using a LEFT JOIN with the 'orders' table on the 'customer_id' column, and filter the results to include only those orders placed between '2012-07-01' and '2012-07-30'.

'customer' Table: (customer_id, cust_name, city, grade, salesman_id)

'orders' Table: (ord_no, purch_amt, ord_date, customer_id, salesman_id)
```sql
SELECT c.* FROM customer c LEFT JOIN orders o ON c.customer_id = o.customer_id WHERE o.ord_date BETWEEN '2012-07-01' AND '2012-07-30';
```

**Output:**
<img width="1224" height="591" alt="image" src="https://github.com/user-attachments/assets/46570020-06a1-48f5-8257-a19d0943a245" />


**Question 6**
---
Write a SQL statement to join the tables salesman, customer and orders so that the same column of each table appears once and only the relational rows are returned.

Sample table: orders

ord_no purch_amt ord_date customer_id salesman_id

70001 150.5 2012-10-05 3005 5002

70009 270.65 2012-09-10 3001 5005

70002 65.26 2012-10-05 3002 5001

70004 110.5 2012-08-17 3009 5003

70007 948.5 2012-09-10 3005 5002

70005 2400.6 2012-07-27 3007 5001

70008 5760 2012-09-10 3002 5001

70010 1983.43 2012-10-10 3004 5006

70003 2480.4 2012-10-10 3009 5003

70012 250.45 2012-06-27 3008 5002

70011 75.29 2012-08-17 3003 5007

70013 3045.6 2012-04-25 3002 5001

Sample table: customer

customer_id | cust_name | city | grade | salesman_id

    3002 | Nick Rimando   | New York   |   100 |        5001

    3007 | Brad Davis     | New York   |   200 |        5001
    
    3005 | Graham Zusi    | California |   200 |        5002
    
    3008 | Julian Green   | London     |   300 |        5002
    
    3004 | Fabian Johnson | Paris      |   300 |        5006
    
    3009 | Geoff Cameron  | Berlin     |   100 |        5003
    
    3003 | Jozy Altidor   | Moscow     |   200 |        5007
    
    
    3001 | Brad Guzan     | London     |       |        5005
Sample table : salesman

salesman_id | name | city | commission

    5001 | James Hoog | New York |       0.15
    
    5002 | Nail Knite | Paris    |       0.13
    
    5005 | Pit Alex   | London   |       0.11
    
    5006 | Mc Lyon    | Paris    |       0.14
    
    5007 | Paul Adam  | Rome     |       0.13
    
    5003 | Lauson Hen | San Jose |       0.12
```sql
-- Paste your SQL code below for Question 6
```

**Output:**
<img width="1221" height="706" alt="image" src="https://github.com/user-attachments/assets/21a88022-72b2-419b-9380-02b79f631476" />

<img width="1212" height="619" alt="image" src="https://github.com/user-attachments/assets/0525620c-ac38-4bfd-8bf0-f4d159740780" />

<img width="1225" height="650" alt="image" src="https://github.com/user-attachments/assets/8e95266b-a0c2-42d0-b699-0d01c899f4ab" />



**Question 7**
---
Write the SQL query that accomplishes the selection of the first name and last name from the "patients" table, with an inner join on the "patient_id" column and a condition filtering for surgeries with a surgery date between '2024-01-01' and '2024-01-31'.

PATIENTS TABLE:

name type

patient_id INT

first_name VARCHAR(50)

last_name VARCHAR(50)

date_of_birth DATE

admission_date DATE

discharge_date DATE

doctor_id INT

SURGERIES TABLE:

name type

surgery_id INT

patient_id INT

surgeon_id INT

surgery_date DATE

```sql
SELECT p.first_name, p.last_name FROM patients p INNER JOIN surgeries s ON p.patient_id = s.patient_id WHERE s.surgery_date BETWEEN '2024-01-01' AND '2024-01-31';
```

**Output:**

<img width="917" height="582" alt="image" src="https://github.com/user-attachments/assets/88cc6241-f272-406e-a5f0-2b1449895d88" />


**Question 8**
---
Write the SQL query that achieves the selection of the "cust_name" and "city" columns from the "customer" table (aliased as "c"), and the "ord_no," "ord_date," and "purch_amt" columns from the "orders" table (aliased as "o"), with a left join on the "customer_id" column and a condition filtering for customers in the city 'London'.

'customer' Table: (customer_id, cust_name, city, grade, salesman_id)

'orders' Table: (ord_no, purch_amt, ord_date, customer_id, salesman_id)

```sql
SELECT c.cust_name, c.city, o.ord_no, o.ord_date, o.purch_amt FROM customer c LEFT JOIN orders o ON c.customer_id = o.customer_id WHERE c.city='London';
```

**Output:**

<img width="1233" height="671" alt="image" src="https://github.com/user-attachments/assets/1575660e-de8b-4624-85d3-a689b31d8309" />

**Question 9**
---

From the following tables write a SQL query to locate those salespeople who do not live in the same city where their customers live and have received a commission of more than 12% from the company. Return Customer Name, customer city, Salesman, salesman city, commission.

Sample table: customer

customer_id | cust_name | city | grade | salesman_id

    3002 | Nick Rimando   | New York   |   100 |        5001

    3007 | Brad Davis     | New York   |   200 |        5001
    
    3005 | Graham Zusi    | California |   200 |        5002
    
    3008 | Julian Green   | London     |   300 |        5002
    
    3004 | Fabian Johnson | Paris      |   300 |        5006
    
    3009 | Geoff Cameron  | Berlin     |   100 |        5003
    
    3003 | Jozy Altidor   | Moscow     |   200 |        5007
    
    3001 | Brad Guzan     | London     |       |        5005
Sample table: salesman

salesman_id | name | city | commission

    5001 | James Hoog | New York |       0.15
    
    5002 | Nail Knite | Paris    |       0.13
    
    5005 | Pit Alex   | London   |       0.11
    
    5006 | Mc Lyon    | Paris    |       0.14
    
    5007 | Paul Adam  | Rome     |       0.13
    
    5003 | Lauson Hen | San Jose |       0.12
```sql
SELECT c.cust_name AS "Customer Name", c.city, s.name AS "Salesman", s.city, s.commission FROM customer c JOIN salesman s ON c.salesman_id = s.salesman_id WHERE c.city <> s.city AND s.commission > 0.12;
```

**Output:**

<img width="1247" height="753" alt="image" src="https://github.com/user-attachments/assets/f56c518e-7468-424f-8c31-ff9b2087bcd2" />



**Question 10**
---
<img width="1225" height="631" alt="image" src="https://github.com/user-attachments/assets/5b833835-e40b-4d7e-aea7-16a75f3560eb" />


```sql
SELECT p.first_name AS patient_name FROM patients p INNER JOIN test_results t ON p.patient_id=t.patient_id WHERE t.test_name='Blood Pressure';
```

**Output:**

<img width="539" height="569" alt="image" src="https://github.com/user-attachments/assets/1917c440-652d-48a1-a209-3aa4998f5d02" />


## RESULT
Thus, the SQL queries to implement different types of joins have been executed successfully.
