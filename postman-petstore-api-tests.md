# Postman API Testing – Week 5

## 🔗 Postman Collection Link
[Postman Workspace – Neira Ahmedbašić](https://speeding-equinox-9547367.postman.co/workspace/Neira-Ahmedba%C5%A1i%C4%87's-Workspace~05a1c4b7-a517-492f-86e3-db397e2b797e/collection/45834032-2c5d455f-95ac-41de-b2e2-cf5415e6b8e5?action=share&creator=45834032)

## 🔗 Swagger API Reference
- Swagger UI: https://petstore.swagger.io/oauth/authorize  
- Import link: https://petstore.swagger.io/v2/swagger.json

---

## 📄 Description

For the fifth homework task, Postman was used to perform API testing based on the Swagger documentation for the Petstore API. The tests included various HTTP methods such as `POST`, `GET`, `DELETE`, and `PUT`, focused on endpoints related to pets and users.

The collection includes both **positive and negative test cases**, validation of expected behavior, status codes, and response time measurements.

---

## ✅ Covered Methods and Scenarios

### 🔹 POST `/pet` – Add New Pet
- ✅ Successfully added pets like "doggie" and "Luna"
- ❌ Negative test: wrong ID type (string) returned 200 instead of expected 400
- ❌ Response time exceeded 200ms in some requests

### 🔹 GET `/pet/findByStatus`
- ✅ Valid retrieval by status (e.g., available)
- ❌ Invalid/empty status returned 200 instead of expected 400/404/422
- ❌ Response time exceeded 200ms

### 🔹 GET `/pet/findByTags`
- ✅ Retrieved pets by tag successfully
- ❌ Slightly over expected response time (e.g., 205ms)

### 🔹 DELETE `/pet/{petId}`
- ✅ First deletion returned 200 or 404 (depending on state)
- ✅ Second deletion correctly returned 404 (pet not found)
- ❌ Empty response body; should include “not found” message

### 🔹 PUT `/pet` – Update Existing Pet
- ✅ Name updated successfully
- ❌ Update without ID incorrectly returned 200 instead of expected error

---

## 🔹 GET `/user/login`
- ✅ Valid login returned session token
- ❌ Response time exceeded 200ms in one case (235ms)
- ✅ Incorrect password returned 400/401
- ✅ Missing parameter returned 400
- ✅ SQL injection attempt rejected

---

## 🔹 POST `/user` – User Creation
- ✅ Valid user creation returned status code 200
- ✅ Response included new user ID

---
## 📌 Summary

This collection demonstrates comprehensive API testing using Postman. It includes:

- Functional tests for valid and invalid inputs
- Verification of HTTP status codes
- Response content validation
- Performance checks based on response time
- Realistic scenarios based on the Swagger specification

Each scenario is clearly documented and replicable. Postman’s scripting features were also used for descriptions and logic handling where needed.

---

Prepared as part of Week 5 QA training.
