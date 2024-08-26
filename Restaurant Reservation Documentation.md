# Restaurant Reservation System 

## INTRODUCTION

The restaurant industry is highly competitive, and the ability to effectively handle reservation is important to keep customers happy and run smoothly. A software solution for a restaurant reservation system simplifies the way tables are booked, guests’ lists are managed, and seat arrangement is done. It is through this that restaurants can have a smooth operation with regards to reservations thereby reducing chances of over-booking or miscommunication on such matters. Through automation of the process of making reservations, restaurants can be able to optimize their seating capacity while giving customers an easy time at the same time.

A restaurant reservation system also has other valuable features including real-time updates, customer management and integration with online booking platforms. These features assist in ensuring that managers in restaurants have up to date records concerning all reservations, tracking client preferences as well as optimizing table turnover rates. Equally important, it can provide automated reminders about upcoming reservations hence minimizing instances of no shows by clients. To sum it all up a Restaurant Reservation System culminates into efficient restaurant operations as well improved eating experiences among their esteemed customers.


## Project Features and Characteristics


## 1. Reservation Module

• Booking: Customers select a date, time, and count of people to make a table 
 reservation.

• Calendar: Shows which times are available or already booked.

• Confirmation: Sends a message to confirm the reservation.

• Customer Records: Keeps track of past reservations.

## 2. Table 

• Table Map: Shows where tables are in the restaurant.

• Assigning Tables: Puts customers at tables based on their booking.

• Live Updates: Shows if tables are free, reserved, or in use.

## 3. User Module

• Customer Info: Saves customer details like name and preferences.

• Staff Roles: Handles different permissions for admins, hosts, and waiters.

• Contact: Lets staff send messages to customers.

## 4. Reports Module

• Booking Reports: Shows daily, weekly, and monthly booking details.

• Table Use: Tracks which tables are used most often.

## 5. Feedback Module

• Feedback: Asks customers how their dining experience was.

• Ratings: Let customers rate their experience.

• Responses: Allows staff to reply to feedback.


## Project Scope

The purpose of the restaurant reservation system is to make easier and organized the 
process for reserving tables, managing these bookings, and handling interactions with 
customers. 
The system will enable customers to book their desired tables through system, see 
real-time availability of seats, and get confirmation details via email. 
It also includes functions for managing tables which helps in assigning them quickly 
by restaurant workers as well as keeps track on status all day long (open/closed). 
The system will handle user management, giving the right to customers and staff 
to make profiles and enter the system based on their roles.
The system also provides reports about reservations, table use rates, as well as feedback 
from customers. 
These details offer important information for managing a restaurant effectively.
With regards to payment section it is going to assist in making transactions online easier; 
meanwhile notification area makes certain that all reminders or updates related with 
customer's bookings are sent out promptly. 
Lastly, the module for feedback will gather and 
handle customer reviews, aiding the restaurant in ongoing enhancement of its services.

## Limitations

Though the restaurant reservation system intends to include necessary functions, there 
are a few restrictions. The main concentration is on dealing with table reservations and it might 
not seamlessly blend in with other systems for restaurant management like inventory or staff 
scheduling because of its limited scope. For real-time updates and notifications, you require a 
constant internet connection that could impact performance if the connectivity is weak or 
unstable. The user management module will have basic role assignments, but it may not 
support more complex permissions. The system can process online payments, but it might lack 
advanced financial reporting. Lastly, while the system will generate standard reports, custom 
report generation might be limited.



## Work breakdown Structure

![image](https://raw.githubusercontent.com/isaaczacck/Restaurant-Reservation-Documentation/cb6a33fd2916ab03813855095969cbb0fcac2a7b/Screenshot%202024-08-23%20114402.png)

## Functional Requirements

### User Requirements

| **No.** | **User**   | **Feature**                | **Requirement**                                                |
|---------|------------|----------------------------|----------------------------------------------------------------|
| 1       | Customer   | User Registration           | Allow users to create an account with name, email, and password. |
| 2       | Customer   | User Login                  | Allow users to log in using email and password.                |
| 3       | Customer   | View Available Tables       | Display available tables for selected date and time.           |
| 4       | Customer   | Make a Reservation          | Allow users to select a table and make a reservation.          |
| 5       | Customer   | Modify Reservation          | Allow users to change date, time, or number of guests.         |
| 6       | Customer   | Cancel Reservation          | Allow users to cancel their reservation.                       |
| 7       | Customer   | Receive Confirmation        | Send a confirmation email/SMS after reservation is made or modified. |
| 8       | Customer   | Payment Process             | Allow user to Pay Using QR code                                |
| 9       | Admin      | Admin Login                 | Allow admins to log in with admin credentials.                 |
| 10       | Admin      | Manage Reservations         | Allow admins to view, modify, or cancel reservations.          |
| 11      | Admin      | View Reports                | Allow admins to generate and view reservation reports.         |
| 12      | Admin      | Manage Tables               | Allow admins to manage table details in the system.            |

### use case
![image](https://github.com/isaaczacck/Restaurant-Reservation-Documentation/blob/main/Use%20Case.jpg?raw=true)

## Database Architecture

### Data Dictionary**

---

#### **Table 1: USER**

| **FIELD NAME** | **DESCRIPTION**                             | **DATA TYPE** | **LENGTH** | **SAMPLE**             |
|----------------|---------------------------------------------|---------------|------------|------------------------|
| USER_ID        | Unique identification of the user           | String        | 255        | USER123456             |
| USERNAME       | Username for login                          | String        | 255        | janedoe                |
| PASSWORD       | User's password (hashed)                    | String        | 255        | ******                 |
| EMAIL          | User's email address                        | String        | 255        | janedoe@example.com    |
| PHONE_NUMBER   | User's contact number                       | String        | 20         | 09123456789            |
| ROLE           | Role of the user                            | String        | 50         | Customer / Staff       |

---

#### **Table 2: RESERVATION**

| **FIELD NAME**        | **DESCRIPTION**                             | **DATA TYPE** | **LENGTH** | **SAMPLE**             |
|-----------------------|---------------------------------------------|---------------|------------|------------------------|
| RESERVATION_ID        | Unique identification of the reservation    | String        | 255        | Reserve12345           |
| USER_ID               | ID of the customer making the reservation   | String        | 255        | USER123456             |
| RESERVATION_DATE      | Date of the reservation                     | Date          |            | 2024-08-21             |
| RESERVATION_TIME      | Time of the reservation                     | Time          |            | 6:00 pm                |
| GUESTS                | Number of guests                            | Integer       |            | 4                      |
| TABLE_ID              | ID of the reserved table                    | String        | 255        | TABLE002               |
| STATUS                | Status of the reservation                   | String        | 50         | Confirmed / Cancelled  |
| CREATED               | Date timestamp of reservation creation      | Date          |            | 2024-08-21 - 2:25 pm   |

---

#### **Table 3: TABLE**

| **FIELD NAME** | **DESCRIPTION**                        | **DATA TYPE** | **LENGTH** | **SAMPLE** |
|----------------|----------------------------------------|---------------|------------|------------|
| TABLE_ID       | Unique identification of the table     | String        | 255        | TABLE002   |
| TABLE_NUMBER   | Table number in the restaurant         | String        | 50         | 12         |
| SEATS          | Number of seats at the table           | Integer       |            | 4          |
| STATUS         | Status of the table                    | String        | 50         | Available / Reserved |

---
#### **Table 4: PAYMENT**

| **FIELD NAME** | **DESCRIPTION**                                                 | **DATA TYPE** | **LENGTH** | **SAMPLE** |
|----------------|-----------------------------------------------------------------|---------------|------------|------------|
| USER_INFO      | Unique identification of the table                              | String   | 255     | TABLE002   |
| REFERENE_N0.   | unique alphanumeric code assigned to each transaction in GCash.|Interger | 255       | 123456789  |


---
#### **Table 5: FEEDBACK**

| **FIELD NAME**   | **DESCRIPTION**                                | **DATA TYPE** | **LENGTH** | **SAMPLE**             |
|------------------|----------------------------------------------|---------------|------------|------------------------|
| FEEDBACK_ID      | Unique identification of the feedback       | String        | 255        | Feedback123456         |
| USER_ID          | ID of the customer giving feedback           | String        | 255        | USER123456             |
| RESERVATION_ID   | ID of the related reservation                | String        | 255        | Reserve789123          |
| RATING           | Customer's rating                            | Integer       |            | 5                      |
| COMMENTS         | Customer's comments                          | String        | 500        | Excellent service!     |
| CREATED          | Date timestamp of feedback submission        | Date          |            | 2024-08-21 – 3:00 pm   |

---


## ERD

For Best View
https://www.canva.com/design/DAGOpYLp1fs/5ACVfuyI1XscCkCIyhPCZw/edit?utm_content=DAGOpYLp1fs&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton


![image](https://raw.githubusercontent.com/isaaczacck/Restaurant-Reservation-Documentation/cc880594effc5437aea1ffa31ed85b05d795d65e/ERD.png)


## Non Functional Requirements

### Product Requirement (PLEASE SKIP THIS)

### Organizational Requirement (PLEASE SKIP THIS)


### External Requirements  (PLEASE SKIP THIS)


## System Testing and Evaluation   (PLEASE SKIP THIS)

### Functional Testing Procedure   (PLEASE SKIP THIS)

### Functional Testing Summary

### Evaluation Procedure

### Recommendation






### Wireframe (PLEASE SKIP THIS)



### High Fidelity (PLEASE SKIP THIS)



### System Screenshot (PLEASE SKIP THIS)
