#  Airbnb Clone Backend — Data Flow Diagram (DFD)

##  Objective
The goal of this task is to design a **Data Flow Diagram (DFD)** that represents how data moves through the **Airbnb Clone backend system**.  
The diagram shows the interactions between **users, processes, data stores,** and **external systems** for core operations such as user management, property listings, bookings, and payments.

---

##  Overview
The DFD illustrates the **flow of data** within the system — from input (user actions) to output (system responses).  
It provides a visual model of:
- **External Entities** (actors such as Guests, Hosts, Admins)
- **Processes** (functions that handle data, e.g., Register User, Book Property)
- **Data Stores** (database components such as Users, Properties, Bookings, Payments)
- **Data Flows** (arrows showing how data moves between processes and entities)

---

##  Key Components

### **1 External Entities**
| Entity | Description |
|--------|--------------|
| **Guest** | Interacts with the system to register, browse properties, make bookings, and payments. |
| **Host** | Manages property listings and handles booking requests. |
| **Admin** | Manages users, listings, and monitors transactions. |
| **Payment Gateway** | External service used to process secure payments. |

---

### **2 Main Processes**
| Process ID | Process Name | Description |
|-------------|---------------|-------------|
| **P1** | User Authentication | Handles user registration, login, and authorization. |
| **P2** | Property Management | Allows hosts to add, edit, or delete property listings. |
| **P3** | Booking Management | Handles creation, approval, and cancellation of bookings. |
| **P4** | Payment Processing | Manages all payment transactions and confirmations. |
| **P5** | Admin Operations | Oversees system data, users, and reports. |

---

### **3 Data Stores**
| Data Store | Description |
|-------------|--------------|
| **D1: Users Database** | Stores user details (name, email, password, role). |
| **D2: Properties Database** | Stores property details (title, description, price, availability). |
| **D3: Bookings Database** | Stores booking records, dates, and status. |
| **D4: Payments Database** | Stores transaction details and receipts. |

---

##  **Data Flow Summary**

### **A. User Registration Flow**
1. Guest submits registration data → `User Authentication (P1)`  
2. Process stores data in `Users Database (D1)`  
3. Confirmation returned to Guest  

### **B. Property Management Flow**
1. Host adds property details → `Property Management (P2)`  
2. Process stores data in `Properties Database (D2)`  
3. Confirmation returned to Host  

### **C. Booking Flow**
1. Guest requests booking → `Booking Management (P3)`  
2. Availability checked in `Properties Database (D2)`  
3. Booking stored in `Bookings Database (D3)`  
4. Confirmation sent to Guest and Host  

### **D. Payment Flow**
1. Guest initiates payment → `Payment Processing (P4)`  
2. Payment sent to `Payment Gateway` for verification  
3. Transaction stored in `Payments Database (D4)`  
4. Payment confirmation sent to Guest  

### **E. Admin Flow**
1. Admin retrieves or updates data → via `Admin Operations (P5)`  
2. Accesses all data stores (Users, Properties, Bookings, Payments)  

---

##  Tools Used
- **Draw.io (Diagrams.net)** – Used to design the DFD  
- **Git & GitHub** – For version control and project management  

---

##  Repository Structure
