# Experiment 2: DDL Commands

## AIM
To study and implement DDL commands and different types of constraints.

## THEORY

### 1. CREATE
Used to create a new relation (table).

**Syntax:**
```sql
CREATE TABLE (
  field_1 data_type(size),
  field_2 data_type(size),
  ...
);
```
### 2. ALTER
Used to add, modify, drop, or rename fields in an existing relation.
(a) ADD
```sql
ALTER TABLE std ADD (Address CHAR(10));
```
(b) MODIFY
```sql
ALTER TABLE relation_name MODIFY (field_1 new_data_type(size));
```
(c) DROP
```sql
ALTER TABLE relation_name DROP COLUMN field_name;
```
(d) RENAME
```sql
ALTER TABLE relation_name RENAME COLUMN old_field_name TO new_field_name;
```
### 3. DROP TABLE
Used to permanently delete the structure and data of a table.
```sql
DROP TABLE relation_name;
```
### 4. RENAME
Used to rename an existing database object.
```sql
RENAME TABLE old_relation_name TO new_relation_name;
```
### CONSTRAINTS
Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE) or after it is created (using ALTER TABLE).
### 1. NOT NULL
When a column is defined as NOT NULL, it becomes mandatory to enter a value in that column.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) NOT NULL
);
```
### 2. UNIQUE
Ensures that values in a column are unique.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) UNIQUE
);
```
### 3. CHECK
Specifies a condition that each row must satisfy.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) CHECK (logical_expression)
);
```
### 4. PRIMARY KEY
Used to uniquely identify each record in a table.
Properties:
Must contain unique values.
Cannot be null.
Should contain minimal fields.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) PRIMARY KEY
);
```
### 5. FOREIGN KEY
Used to reference the primary key of another table.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size),
  FOREIGN KEY (column_name) REFERENCES other_table(column)
);
```
### 6. DEFAULT
Used to insert a default value into a column if no value is specified.

Syntax:
```sql
CREATE TABLE Table_Name (
  col_name1 data_type,
  col_name2 data_type,
  col_name3 data_type DEFAULT 'default_value'
);
```

**Question 1**

<img width="606" height="172" alt="image" src="https://github.com/user-attachments/assets/67c3f7ab-6346-4a5b-b7e8-917d3c90b7fc" />


```sql
<img width="388" height="149" alt="image" src="https://github.com/user-attachments/assets/6f8e0729-41a2-4998-a566-cd545db98d52" />

```

**Output:**
<img width="617" height="234" alt="image" src="https://github.com/user-attachments/assets/a6189f55-b84b-4a8c-ad8f-d9ba90595c7a" />


**Question 2**
---
<img width="612" height="135" alt="image" src="https://github.com/user-attachments/assets/b81f666a-8690-4ed4-992a-db7a62deb941" />

```sql

<img width="543" height="111" alt="image" src="https://github.com/user-attachments/assets/6bddbba2-cedf-415f-a0a4-240e429bc3f9" />

```

**Output:**

<img width="610" height="213" alt="image" src="https://github.com/user-attachments/assets/6f690f1f-3f3d-416f-bdbe-f3cdebd29e2b" />


**Question 3**
---

<img width="607" height="246" alt="image" src="https://github.com/user-attachments/assets/03726c53-441d-428c-858b-85d1964659a1" />

```sql

<img width="591" height="143" alt="image" src="https://github.com/user-attachments/assets/4011edc3-fbe6-4a74-9f3d-5ea2240329c9" />


```

**Output:**

<img width="613" height="204" alt="image" src="https://github.com/user-attachments/assets/a4298e52-d45f-4492-ac1c-a3544b51fc20" />


**Question 4**
---
<img width="613" height="205" alt="image" src="https://github.com/user-attachments/assets/4239b186-0afc-4f71-ac83-1d1d7678ea69" />


```sql

<img width="373" height="127" alt="image" src="https://github.com/user-attachments/assets/c6ecece2-5162-462e-a517-908bfff5edca" />


```

**Output:**

<img width="617" height="233" alt="image" src="https://github.com/user-attachments/assets/ab16fadf-a196-49d4-ab20-d8e0745733d5" />


**Question 5**
---

<img width="613" height="199" alt="image" src="https://github.com/user-attachments/assets/58dd62fe-1c1a-47f6-8013-37c2996e4d33" />

```sql

<img width="402" height="122" alt="image" src="https://github.com/user-attachments/assets/eea1632d-71b5-4e4a-8b65-cf6e31129d4f" />

```

**Output:**

<img width="615" height="229" alt="image" src="https://github.com/user-attachments/assets/bda75f48-7506-47c9-93a8-f71eedd7edad" />


**Question 6**
---

<img width="486" height="231" alt="image" src="https://github.com/user-attachments/assets/9522d859-2887-4a0c-b348-08c032d2812f" />


```sql

<img width="460" height="95" alt="image" src="https://github.com/user-attachments/assets/e0c5470b-7d18-4b36-bbe5-e131d84713dd" />


```

**Output:**

<img width="639" height="234" alt="image" src="https://github.com/user-attachments/assets/c5a4b92d-a07a-4ae9-abf6-e54199612238" />


**Question 7**
---

<img width="610" height="234" alt="image" src="https://github.com/user-attachments/assets/7ba481be-a4dd-4f91-b0fb-12eb93576681" />

```sql
<img width="246" height="131" alt="image" src="https://github.com/user-attachments/assets/0e8d4dba-918c-4b19-9848-d2a975fd61b7" />

```

**Output:**

<img width="613" height="413" alt="image" src="https://github.com/user-attachments/assets/c668fd63-6254-47ef-9a61-314a099136d4" />


**Question 8**
---

<img width="614" height="203" alt="image" src="https://github.com/user-attachments/assets/34e8cda1-fb44-4ca4-822c-017b3ee33754" />


```sql
<img width="434" height="94" alt="image" src="https://github.com/user-attachments/assets/1b4c4dcc-de8b-403e-a794-d94ae7c6b1e3" />

```

**Output:**
<img width="611" height="257" alt="image" src="https://github.com/user-attachments/assets/647ebb6a-9940-4216-a359-dca590fb3eb9" />

**Question 9**
---
<img width="464" height="191" alt="image" src="https://github.com/user-attachments/assets/5c09bce6-b7a6-48ae-be96-a01abc96bf2c" />

```sql
<img width="293" height="143" alt="image" src="https://github.com/user-attachments/assets/c0d712fb-abdf-4039-881b-6c1f516c185d" />

```

**Output:**

<img width="650" height="218" alt="image" src="https://github.com/user-attachments/assets/3a50cc65-21e4-47bb-b37f-ed55ae6f5167" />

**Question 10**
---
<img width="597" height="255" alt="image" src="https://github.com/user-attachments/assets/0e4e0d95-9a33-4e77-a5c9-f34e834a75ff" />

```sql
<img width="273" height="72" alt="image" src="https://github.com/user-attachments/assets/2152b858-547b-4fb5-a326-614dc3d1c355" />

```

**Output:**

<img width="645" height="222" alt="image" src="https://github.com/user-attachments/assets/ef83e057-9358-40f5-b0de-960618651be3" />

## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
