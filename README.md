# Automated API Testing Framework (Jest + MongoDB)

![Node.js](https://img.shields.io/badge/Node.js-Backend-green)
![Jest](https://img.shields.io/badge/Tested%20With-Jest-red)
![MongoDB](https://img.shields.io/badge/Database-MongoDB-green)
![Testing](https://img.shields.io/badge/Testing-Automated-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)

Automated testing project demonstrating how to validate REST API behavior using **Jest**, **MongoDB**, and HTTP request testing.

This project shows how backend teams can build a reliable automated testing strategy to validate API responses, database interactions, and error handling before code reaches production.

---

# Problem

Backend APIs that interact with databases can fail in several ways:

- incorrect data retrieval
- unexpected API responses
- failures when querying specific records
- regressions introduced by new code

Without automated testing, these issues may reach production and impact system reliability.

Development teams therefore need a strategy to **validate API behavior automatically and consistently**.

---

# Solution

This project demonstrates how to implement an **automated testing framework** using **Jest** to validate a user API connected to a **MongoDB database**.

The test suite verifies:

- retrieving all users
- retrieving a specific user by ID
- validating API responses
- handling cases where users are not found

HTTP requests are simulated using the **Superagent** library, allowing the tests to interact with the API the same way a real client would.

---

# Testing Architecture

The following diagram illustrates how the automated testing framework is structured.

It highlights three key testing layers:

1️⃣ **Testing Architecture Diagram** – shows how Jest interacts with the API and database  
2️⃣ **Test Pyramid Visual** – demonstrates the testing strategy (unit → API → integration)  
3️⃣ **API Testing Flow** – explains how HTTP requests are executed and validated

![Testing Architecture](https://raw.githubusercontent.com/Thiago771414/imagensProjetos/main/slices/mobile/jest.png)

---

# Test Strategy

The testing approach follows a layered structure commonly used in professional software development teams.

### Unit Tests

Validate isolated logic such as:

- greeting functions
- math operations
- number validation

These tests ensure core logic works independently from external systems.

---

### API Tests

Validate REST endpoints using HTTP requests.

The tests simulate real client interactions with the API using **Superagent**, ensuring:

- correct responses
- proper status codes
- correct user retrieval

---

### Database Tests

Validate persistence logic and interactions with **MongoDB**, ensuring that:

- queries return expected results
- data retrieval works correctly
- invalid queries are handled properly.

---
# API Test Flow

The automated tests simulate the behavior of a real API client.
The flow is:
---

```bash
Jest Test
↓
HTTP Request (Superagent)
↓
User API
↓
MongoDB
↓
Response Validation
```
---

This approach ensures that the API behaves correctly when interacting with the database.

---

# Project Structure

```bash
project/
├── greeting/
├── mathOperations/
├── par-numero/
├── INTEGRATION-TEST/
├── MONGO-DB-TEST/
├── user-repository/
├── package.json
└── README.md
```
---

Each directory demonstrates a different testing strategy.

---

# Technology Stack

Backend Testing

- Node.js
- Jest
- MongoDB
- Superagent

---

# Installation

Install the dependencies:

```bash
npm install --save-dev jest
npm install superagent
```
---
# Configuration

Before running the tests, ensure MongoDB is running locally.

Adjust the MongoDB connection string if necessary.

Running the Tests
# Test Execution Example

Example output when running the test suite:

```bash
PASS greeting.spec.js
PASS mathOperations.spec.js
PASS user-api.spec.js
PASS user-repository.spec.js

Test Suites: 4 passed
Tests: 12 passed
Time: 2.1s
```

Navigate to the project root directory and run:
```bash
npm test
```
Jest will automatically execute all test cases defined in the project.

The results will show whether the API:

returns all users correctly

returns a specific user by ID

handles missing users properly

Business Value

Automated testing frameworks like this help teams:

detect bugs early

prevent regressions

ensure API reliability

improve deployment confidence

support CI/CD pipelines

This ensures backend services remain stable, predictable, and production-ready.

#Author

Thiago Reis Lima
Software Engineer
LinkedIn
```bash
https://www.linkedin.com/in/thiago-lima-2a5896166
```
