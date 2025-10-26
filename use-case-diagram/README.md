#  Airbnb Clone Backend — Use Case Diagram

##  Objective
The goal of this task is to **visualize the system interactions** in the Airbnb Clone backend application using a **Use Case Diagram**.  
This diagram identifies **all key actors** (users and external systems) and their **interactions** with the backend system for core functionalities like **user authentication, property management, bookings, and payments**.

---

##  Overview
This diagram represents how different types of users interact with the **Airbnb Clone backend system** to perform operations such as:
- Registering and logging into the system
- Managing property listings (for hosts)
- Browsing and booking properties (for guests)
- Processing payments through an external gateway
- Monitoring system activity (for administrators)

---

##  Actors
| Actor | Description |
|--------|--------------|
| **Guest (User)** | A customer who registers, browses properties, books stays, and makes payments. |
| **Host** | A property owner who lists, updates, and manages properties. |
| **Admin** | Oversees platform activity, manages users, and monitors transactions. |
| **Payment Gateway (External System)** | Handles payment processing securely (e.g., Stripe or PayPal). 



##  Key Use Cases
### **For Guest**
- Register / Login / Logout  
- Browse available properties  
- View property details  
- Book a property  
- Make payment  
- View or cancel bookings  

### **For Host**
- Register / Login / Logout  
- Add, update, or delete a property  
- View property booking requests  
- Approve or reject bookings  

### **For Admin**
- Manage users and listings  
- Monitor bookings and payments  
- Generate system reports  

### **For Payment Gateway**
- Process and verify payments  
- Send payment confirmation or failure response  


##  Diagram Description
The **Airbnb Clone System** is represented as a single system boundary that connects to four primary actors:
- **Guest** interacts with the system to perform user and booking actions.  
- **Host** interacts with the system for property management.  
- **Admin** oversees operations.  
- **Payment Gateway** integrates externally for payment verification.


##  Tools Used
- **Draw.io (Diagrams.net)** – Used to design the Use Case Diagram  
- **Git & GitHub** – For version control and repository management  



##  Repository Structure
