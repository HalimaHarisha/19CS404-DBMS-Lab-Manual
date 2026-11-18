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
*Paste or attach your diagram here*  
![ER Diagram](er_diagram_fitness.png)

### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|--------------------|-------|
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |

### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|------------|---------------|-------|
|              |            |               |       |
|              |            |               |       |
|              |            |               |       |

### Assumptions
- 
- 
- 

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
*Paste or attach your diagram here*  
![ER Diagram](er_diagram_library.png)

### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|--------------------|-------|
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |

### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|------------|---------------|-------|
|              |            |               |       |
|              |            |               |       |
|              |            |               |       |

### Assumptions
- 
- 
- 

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
<img width="832" height="440" alt="image" src="https://github.com/user-attachments/assets/59d26a32-1290-4796-beb8-d399bcf463c8" />


### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|--------------------|-------|
| CUSTOMER | Customer_ID (PK), Name, Phone, Email | Customer details |
| RESERVATION | Reservation_ID (PK), Customer_ID (FK), Table_ID (FK), Waiter_ID (FK), Reservation_Date, Time, No_of_Guests | Table reservation and walk-in details |
| RESTAURANT_TABLE | Table_ID (PK), Table_Number, Capacity, Status | Restaurant table details |
| WAITER | Waiter_ID (PK), Name, Phone | Waiter details |
| FOOD_ORDER | Order_ID (PK), Reservation_ID (FK), Order_Date, Order_Status | Customer food orders |
| ORDER_ITEM | Order_Item_ID (PK), Order_ID (FK), Dish_ID (FK), Quantity, Price | Dishes included in each order |
| DISH | Dish_ID (PK), Category_ID (FK), Dish_Name, Price | Food menu details |
| CATEGORY | Category_ID (PK), Category_Name | Starter, Main, Dessert |
| BILL | Bill_ID (PK), Reservation_ID (FK), Total_Amount, Food_Charge, Service_Charge, Payment_Status | Billing details |
### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|------------|---------------|-------|
| CUSTOMER – RESERVATION | 1 : M | Partial – Total | A customer can make multiple reservations |
| RESERVATION – RESTAURANT_TABLE | M : 1 | Total – Partial | Each reservation is assigned to one table |
| WAITER – RESERVATION | 1 : M | Partial – Total | A waiter serves multiple reservations |
| RESERVATION – FOOD_ORDER | 1 : M | Partial – Total | A reservation can have multiple food orders |
| FOOD_ORDER – ORDER_ITEM | 1 : M | Total – Total | Each order contains multiple dishes |
| DISH – ORDER_ITEM | 1 : M | Total – Total | A dish can appear in multiple order items |
| CATEGORY – DISH | 1 : M | Total – Partial | Each dish belongs to one category |
| RESERVATION – BILL | 1 : 1 | Total – Total | Each reservation generates one bill |
| RESTAURANT_TABLE – RESERVATION | 1 : M | Partial – Total | A table can be reserved multiple times |


### Assumptions
1. Each customer is uniquely identified by Customer_ID.
2. A customer can make multiple reservations.
3. Each reservation is assigned to one restaurant table.
4. Customers can make reservations or walk in without prior booking.
5. Each reservation is served by one waiter.
6. A reservation can have multiple food orders.
7. Each food order contains one or more dishes.
8. Each dish belongs to only one category, such as Starter, Main Course, or Dessert.
9. Each reservation generates one bill including food and service charges.
10. A restaurant table can be reserved multiple times at different dates and time slots.
11. Bills can have different payment statuses such as Paid, Pending, or Partially Paid.
12. Table availability is checked before confirming a reservation.

## Instructions for Students

1. Complete **all three scenarios** (A, B, C).  
2. Identify entities, relationships, and attributes for each.  
3. Draw ER diagrams using **draw.io / diagrams.net** or hand-drawn & scanned.  
4. Fill in all tables and assumptions for each scenario.  
5. Export the completed Markdown (with diagrams) as **a single PDF**
