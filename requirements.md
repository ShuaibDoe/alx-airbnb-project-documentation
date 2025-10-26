#  Airbnb Clone Backend — Requirement Specifications

##  Objective
This document defines the **technical and functional requirements** for three core backend features of the Airbnb Clone system:
1. User Authentication  
2. Property Management  
3. Booking System  

Each feature includes detailed **API endpoints**, **input/output specifications**, **validation rules**, and **performance criteria** to guide development and ensure consistent backend behavior.

---

##  1. User Authentication Module

###  Functional Overview
This module handles user registration, login, and authentication using JSON Web Tokens (JWT).  
It ensures only verified users can access protected endpoints such as property management or booking.

---

###  API Endpoints

| Method | Endpoint | Description | Authentication Required |
|--------|-----------|-------------|--------------------------|
| `POST` | `/api/v1/auth/register` | Register a new user account |  |
| `POST` | `/api/v1/auth/login` | Authenticate a user and return a JWT |  |
| `GET`  | `/api/v1/auth/profile` | Retrieve logged-in user's profile |  |

---

###  Input Specification

#### `/api/v1/auth/register`
| Field | Type | Required | Validation Rules |
|-------|------|-----------|------------------|
| `first_name` | String |  | Minimum 2 characters |
| `last_name` | String |  | Minimum 2 characters |
| `email` | String |  | Must be valid email format |
| `password` | String |  | Minimum 8 characters, at least 1 letter and 1 number |
| `role` | Enum (`guest`, `host`) |  | Must be one of defined roles |

#### `/api/v1/auth/login`
| Field | Type | Required | Validation Rules |
|-------|------|-----------|------------------|
| `email` | String |  | Must match registered email |
| `password` | String |  | Must match stored hash |

---

###  Output Specification

**Success Response (Login/Register)**
```json
{
  "status": "success",
  "message": "User authenticated successfully",
  "token": "<jwt_token>",
  "data": {
    "user_id": "uuid",
    "first_name": "John",
    "last_name": "Doe",
    "email": "john@example.com",
    "role": "guest"
  }
}
