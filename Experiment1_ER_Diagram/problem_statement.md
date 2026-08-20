# ER Diagram Workshop – Submission Template

## Objective
To understand and apply ER modeling concepts by creating ER diagrams for real-world applications.

## Purpose
Gain hands-on experience in designing ER diagrams that represent database structure including entities, relationships, attributes, and constraints.

---

# Scenario A: City Fitness Club Management

**Business Context:**  
FlexiFit Gym wants a database to manage its members, trainers, and fitness programs.

**Requirements:**  
- Members register with name, membership type, and start date.  
- Each member can join multiple programs (Yoga, Zumba, Weight Training).  
- Trainers assigned to programs; a program may have multiple trainers.  
- Members may book personal training sessions with trainers.  
- Attendance recorded for each session.  
- Payments tracked for memberships and sessions.

### ER Diagram:

<img width="752" height="412" alt="image" src="https://github.com/user-attachments/assets/0483f803-0e3d-467c-959f-79aea6cb693c" />



### Entities and Attributes

<img width="827" height="307" alt="image" src="https://github.com/user-attachments/assets/5d890744-735f-4a60-a45f-dbcb991cc077" />


### Relationships and Constraints

<img width="806" height="160" alt="image" src="https://github.com/user-attachments/assets/d695e2a1-c040-43ab-8d3d-43f0f9a755e9" />


### Assumptions
- Membership type determines allowed programs but not restricted in ER model. -Personal training sessions are optional. -Payments cover both membership fees and session fees.
---

# Scenario B: City Library Event & Book Lending System

**Business Context:**  
The Central Library wants to manage book lending and cultural events.

**Requirements:**  
- Members borrow books, with loan and return dates tracked.  
- Each book has title, author, and category.  
- Library organizes events; members can register.  
- Each event has one or more speakers/authors.  
- Rooms are booked for events and study.  
- Overdue fines apply for late returns.

### ER Diagram:

<img width="707" height="808" alt="image" src="https://github.com/user-attachments/assets/c3442a1f-6596-426c-88bc-89ba2cd31ce9" />


### Entities and Attributes

<img width="822" height="367" alt="image" src="https://github.com/user-attachments/assets/ca71b7f3-f75b-4536-a2c6-91231d26baee" />


### Relationships and Constraints

<img width="826" height="335" alt="image" src="https://github.com/user-attachments/assets/c7fb8b19-9415-4691-b568-d6181d160077" />


### Assumptions
- Overdue fines are stored per Loan record.
BookCopy not modeled
Rooms serve both events and study bookings.


---

# Scenario C: Restaurant Table Reservation & Ordering

**Business Context:**  
A popular restaurant wants to manage reservations, orders, and billing.

**Requirements:**  
- Customers can reserve tables or walk in.  
- Each reservation includes date, time, and number of guests.  
- Customers place food orders linked to reservations.  
- Each order contains multiple dishes; dishes belong to categories (starter, main, dessert).  
- Bills generated per reservation, including food and service charges.  
- Waiters assigned to serve reservations.

### ER Diagram:
<img width="792" height="470" alt="image" src="https://github.com/user-attachments/assets/3d097a4b-6601-457a-8eb2-827716706bfd" />


### Entities and Attributes

| Entity   | Attributes (PK, FK)                 | Notes                                                    |
|----------|-------------------------------------|----------------------------------------------------------|
|CHEF      |chef_id (PK),chef_name,chef_salary   |each chef is uniquely identified by chef_id Prepares meals|
|MEAL      |meal_name(PK),meal_price             |A meal is prepared by chefs,ordered by customers          |
|INGREDENTS|ing_name(PK),description             |Each ingredient has a unique name and is linked to meals  |
|CUSTOMERS |cust_phone(PK),cust_name,cust_address|Customer place orders for meals                           |
|SUPPLIER  |S_id(PK),S_name,S_city               |suppiler attend to customers                              |

### Relationships and Constraints

<img width="841" height="258" alt="image" src="https://github.com/user-attachments/assets/ffbc88ed-737f-4885-9411-3fe38348ad2e" />







### Assumptions
- Each chef can prepare multiple meals, but a meal is prepared by only one chef. A customer can place multiple orders, and each order may include one or more meals. Each meal consists of one or more ingredients, and an ingredient may be used in multiple meals.
  

---

## Instructions for Students

1. Complete **all three scenarios** (A, B, C).  
2. Identify entities, relationships, and attributes for each.  
3. Draw ER diagrams using **draw.io / diagrams.net** or hand-drawn & scanned.  
4. Fill in all tables and assumptions for each scenario.  
5. Export the completed Markdown (with diagrams) as **a single PDF**
