# Experiment 3: DML Commands

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**
--
<img width="613" height="417" alt="image" src="https://github.com/user-attachments/assets/24de4419-611b-4084-9522-4a0140af483d" />


sql
<img width="613" height="43" alt="image" src="https://github.com/user-attachments/assets/bbb71492-f8d9-4065-bab8-73279bec77f3" />



**Output:**

<img width="597" height="673" alt="image" src="https://github.com/user-attachments/assets/5cb7349e-e456-4323-a49e-edc5253feffb" />


**Question 2**
---
<img width="610" height="395" alt="image" src="https://github.com/user-attachments/assets/9c433ab5-89c3-430f-99c9-6b1288586f93" />


sql
<img width="613" height="56" alt="image" src="https://github.com/user-attachments/assets/53769997-0721-4abb-bf57-bc2ecefd611a" />



**Output:**

<img width="606" height="476" alt="image" src="https://github.com/user-attachments/assets/003877a5-8dbb-4bd3-b11a-51f87dc5b093" />

**Question 3**
---
<img width="611" height="489" alt="image" src="https://github.com/user-attachments/assets/631c2444-d516-4d0e-ab79-d71d884b6dc0" />

sql
<img width="615" height="45" alt="image" src="https://github.com/user-attachments/assets/19722189-8c1f-4162-b777-5a8aa46c5892" />



**Output:**

<img width="608" height="574" alt="image" src="https://github.com/user-attachments/assets/47f10861-ae8a-4b2a-980c-6e24fd8df53b" />


**Question 4**
---
<img width="612" height="364" alt="image" src="https://github.com/user-attachments/assets/14c808f3-9641-4d1b-aeca-b54f7fae5060" />

sql
<img width="604" height="40" alt="image" src="https://github.com/user-attachments/assets/709c609b-1744-40d3-825d-ed48c61c9252" />



**Output:**

<img width="618" height="382" alt="image" src="https://github.com/user-attachments/assets/5dc5e103-13df-458e-9159-2f34808e9905" />


**Question 5**
---

<img width="600" height="423" alt="image" src="https://github.com/user-attachments/assets/fbfa1370-bd5a-41a0-8ed7-6902b0ab84b6" />

sql
<img width="887" height="642" alt="638914530-da3be8b7-8910-4125-b15e-40eee04c83e8" src="https://github.com/user-attachments/assets/a110bab8-3417-4909-a59e-8ec6c41ee6b0" />



**Output:**

<img width="850" height="551" alt="image" src="https://github.com/user-attachments/assets/792f0c0d-bde4-49f3-ac3b-bbfaa2d50ae2" />


**Question 6**
---
<img width="850" height="512" alt="image" src="https://github.com/user-attachments/assets/fb5dd007-2fd4-4a0e-88ab-d05ebc8f4bbc" />


sql

<img width="618" height="41" alt="image" src="https://github.com/user-attachments/assets/c86b7f99-9043-426e-a414-92feb7ab0de1" />


**Output:**

<img width="867" height="320" alt="image" src="https://github.com/user-attachments/assets/79eac073-56f3-4297-a9a2-51ca0dae884a" />


**Question 7**
---
<img width="842" height="606" alt="image" src="https://github.com/user-attachments/assets/5696fb54-369c-4969-b494-8988347234b1" />


sql

<img width="610" height="55" alt="image" src="https://github.com/user-attachments/assets/58449f14-5d99-4bc7-b4e7-571b97bc7013" />


**Output:**

<img width="852" height="583" alt="image" src="https://github.com/user-attachments/assets/184ab8f3-4bbe-44b4-8ef7-bb3b06eb90f3" />


**Question 8**
---
-- Paste Question 8 here

```sql
-- Paste your SQL code below for Question 8
```

**Output:**

![Output8](output.png)

**Question 9**
---

<img width="877" height="655" alt="image" src="https://github.com/user-attachments/assets/bc1852fe-0071-477a-93f7-05aa793a21cf" />


sql

<img width="610" height="52" alt="image" src="https://github.com/user-attachments/assets/ea5d589a-ff27-4713-a1de-fb9b6821b743" />


**Output:**

<img width="836" height="582" alt="image" src="https://github.com/user-attachments/assets/8d746a1c-9a8c-4c96-a7f4-2d2251327b28" />


**Question 10**
---

<img width="892" height="520" alt="image" src="https://github.com/user-attachments/assets/ebd4d5fc-5f8d-42ad-8dc3-649e3969d832" />


sql

<img width="613" height="54" alt="image" src="https://github.com/user-attachments/assets/41dc1614-b847-40b3-9b1e-f63a9fb95b81" />


**Output:**

<img width="615" height="456" alt="image" src="https://github.com/user-attachments/assets/4e815368-f8f8-4874-a59f-a7519e72f7b8" />


## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
