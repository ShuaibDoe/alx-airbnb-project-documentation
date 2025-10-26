## Objective

- Create a feature documentation diagram that clearly shows all the main backend modules and their functionalities (User Authentication, Property Management, Booking System, and Payments).

## Core Modules and Their Functionalities

You’ll base your Draw.io diagram on these main system modules and sub-features 

## 1 User Management (Authentication & Authorization)

- Handles user registration, login, profile updates, and access control.

  Features:

  Register new user (guest/host)

  Login / Logout

  Password hashing (bcrypt)

  JWT-based authentication

  Manage user profile (edit name, phone, picture)

  Role-based access control (Guest, Host, Admin)

  View user details

## 2 Property Management (Host Side)

- Hosts can manage property listings and make them available for booking.

Features:

  Add a new property
  Update property details
  Delete property
  Upload property images
  Set property pricing and availability
  View all properties owned by host

## 3 Property Browsing (Guest Side)

- Guests can explore and search for available properties.

Features:

  View all properties
  Filter by location, price, or amenities
  View detailed property page
  Check property availability
  Read host information and reviews

## 4 Booking Management

- Handles reservation creation, updates, and cancellations.

Features:

  Create a new booking
  View booking details
  Cancel booking
  Host approval (optional)
  View booking history (guest and host)
  Prevent overlapping bookings

## 5 Payment Processing

- Manages all payment transactions using a secure gateway (Stripe/PayPal).

Features:

  Initiate payment during booking
  Process payment via payment gateway
  Handle payment confirmation/failure
  Generate payment receipt
  Issue refunds on cancellations
  Record transaction details in database

## 6 Admin Management (Optional but Recommended)

- Admins maintain platform integrity and monitor system activity.

Features:

  Manage users (suspend/activate)
  Manage listings (approve/remove)
  Monitor bookings and payments
  Generate platform reports