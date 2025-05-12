# Airbnb Clone – Backend Requirements Specification

## Overview

This document outlines the **technical** and **functional** requirements for core backend features of the Airbnb Clone project. It specifies how APIs should behave, including endpoints, inputs, outputs, validations, and performance expectations.

---

## 1. User Authentication

### 1.1 Functional Requirements
- Allow users to register and log in securely.
- Passwords must be encrypted (e.g., using bcrypt).
- Provide a session token (JWT) upon successful login.

### 1.2 API Endpoints

| Method | Endpoint          | Description               |
|--------|-------------------|---------------------------|
| POST   | `/api/register`   | Register a new user       |
| POST   | `/api/login`      | Authenticate user         |
| GET    | `/api/logout`     | Log out user (invalidate token) |

### 1.3 Input/Output

#### POST `/api/register`
**Input (JSON):**
```json
{
  "name": "Alice Smith",
  "email": "alice@example.com",
  "password": "securePass123"
}
