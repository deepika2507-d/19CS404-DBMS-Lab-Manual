# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**
--
How many patients are covered by each insurance company?

Sample table:Insurance Table

name type

InsuranceID INTEGER

PatientID INTEGER

InsuranceCompany TEXT

PolicyNumber TEXT

PolicyHolder TEXT

ValidityPeriod TEXT
sql
```
SELECT InsuranceCompany, count(PatientID) as TotalPatients from Insurance group by InsuranceCompany;

```

**Output:**

<img width="972" height="741" alt="image" src="https://github.com/user-attachments/assets/09d3e8eb-78b6-48ce-b306-c27f8169fda3" />


**Question 2**
---
<img width="1224" height="757" alt="image" src="https://github.com/user-attachments/assets/6ca03fff-b64a-421e-82b3-707170726580" />

```sql
select DoctorID, count(PrescriptionID) as TotalPrescriptions from Prescriptions group by DoctorID;
```

**Output:**

<img width="954" height="761" alt="image" src="https://github.com/user-attachments/assets/705e4f7d-0013-4e0d-9fa7-a956b27cb89e" />


**Question 3**
---
How many patients have insurance coverage valid in each year?

Sample table:Insurance Table

name type

InsuranceID INTEGER PatientID INTEGER InsuranceCompany TEXT PolicyNumber TEXT PolicyHolder TEXT ValidityPeriod TEXT

```sql
select SUBSTR(ValidityPeriod,1,4) as ValidityYear,count(PatientID) as TotalPatients from Insurance group by SUBSTR(ValidityPeriod,1,4) order by ValidityYear;
```

**Output:**

<img width="855" height="568" alt="image" src="https://github.com/user-attachments/assets/3eec2623-0ddd-449c-8300-b003e162e7a9" />


**Question 4**
---
Write a SQL query to find the total amount of fruits with a unit type of 'LB'.

Note: Inventory attribute contains amount of fruits

Table: fruits

name type

```sql
select SUM(inventory) as total from fruits where unit='LB';
```

**Output:**

<img width="621" height="476" alt="image" src="https://github.com/user-attachments/assets/ede45886-b8f9-4752-9d93-a4622896b808" />


**Question 5**
---
Write a SQL query to find the total income of employees aged 40 or above.

Table: employee

name type

id INTEGER name TEXT age INTEGER city TEXT income INTEGER


```sql
select SUM(income) as total_income from employee where age>=40;
```

**Output:**


<img width="584" height="476" alt="image" src="https://github.com/user-attachments/assets/422177d0-f4c6-4a1e-957c-13f213a6841a" />


**Question 6**
---
Write a SQL query to Calculate the average email length (in characters) for people who lives in Mumbai city

Table: customer

name type

id INTEGER name TEXT
city TEXT email TEXT phone INTEGER
```sql
select AVG(LENGTH(email)) as avg_email_length_below_30 from customer where city='Mumbai';
```

**Output:**

<img width="820" height="521" alt="image" src="https://github.com/user-attachments/assets/37e0373b-e7e1-487e-9395-9ae8bd0e5a58" />



**Question 7**
---

<img width="1210" height="600" alt="image" src="https://github.com/user-attachments/assets/ab3c2f65-504b-4399-8fad-79bea9cae909" />


```sql
select count(*) as COUNT from customer where city<> 'Noida';
```

**Output:**


<img width="575" height="477" alt="image" src="https://github.com/user-attachments/assets/69660a49-83d3-4580-a357-dad83b67d451" />


**Question 8**
---

<img width="1205" height="622" alt="image" src="https://github.com/user-attachments/assets/2145cceb-53a6-4968-9bdb-41991eaa0f4f" />


```sql
select age,MAX(income) from employee group by age having max(income)>2000000;
```

**Output:**


<img width="778" height="536" alt="image" src="https://github.com/user-attachments/assets/5957356d-974a-4cdf-9d70-ac70e3e9ac48" />


**Question 9**
---

<img width="1167" height="677" alt="image" src="https://github.com/user-attachments/assets/28b850c0-529b-4154-b16f-94284f187036" />


```sql
select city,SUM(income) as Income from employee group by city having SUM(income)>200000;
```

**Output:**


<img width="801" height="723" alt="image" src="https://github.com/user-attachments/assets/1cf3643f-6f82-44ce-a601-803d4c512c21" />


**Question 10**
---

<img width="1203" height="635" alt="image" src="https://github.com/user-attachments/assets/b78f3ae2-450c-4362-a219-3cf7a3372744" />


```sql
select occupation,AVG(workhour) from employee1 group by occupation having AVG(workhour) between 10 and 12;
```

**Output:**


<img width="875" height="578" alt="image" src="https://github.com/user-attachments/assets/245de66b-2f19-41fa-ad71-ebcba006e44d" />


## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
