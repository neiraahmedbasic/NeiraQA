# QA Portfolio – Neira Ahmedbasic

Welcome to my QA portfolio! This repository showcases my practical work in manual testing, API testing with Postman, SQL validation, structured bug reporting, and usability improvements. The goal of this portfolio is to demonstrate my knowledge and hands-on experience in software testing across different tools and methods.

---

## 📁 Contents

### ✅ Manual Testing

- Test Cases for mobile and web applications (iOS apps, chat apps, e-commerce flows)
- Boundary Value Analysis (BVA) and Equivalence Partitioning (EP)
- Pre-test and Re-test scenarios
- Usability feedback (layout, navigation, messaging)
- Structured Bug Reports with reproduction steps and expected vs. actual outcomes
- Test Plan document describing scope, objectives, tools, and schedule

📄 Example Files:
- `mobile-testing-ios-viber-instagram-messenger.md.md`
- `boundary-value-analysis-week3.md`
- `bug-reports-cosmetic-cloth-reserved.md`
- `Improvement.md`

#### 🧾 Test Case Example

```
Test Case ID: TC_VIBER_001  
Title: Validate Viber chat functionality without internet connection  
Platform: iPhone 13, App version 25.5.2  
Steps:  
1. Turn off mobile data and Wi-Fi  
2. Open Viber  
3. Try to send a message  
Expected result: Message fails to send with appropriate offline notification  
```

---

### 🔌 API Testing – Postman

- Full Postman collection with organized folders for each endpoint
- Tests include GET, POST, PUT, DELETE methods
- Use of **Authorization tokens** (Bearer Token)  Content-Type: application/json
Authorization: Bearer {{auth_token}}
- Environment variables used for base URL and authentication  
- Tokens, sensitive data, and dynamic variables should be managed via environment files
- JSON request bodies and response schema can be validated using scripts
- Tests can be run via Postman Collection Runner or Newman for automation
- Headers set for `Content-Type`, `Authorization`, etc.  
- Included Postman test scripts with validations (status codes, response time, schema checks)
- Test report exported and documented

📄 File:
- `postman-petstore-api-tests.md`

#### 🔐 Headers & Authorization Example

```
POST /user/login
Host: petstore.swagger.io
Content-Type: application/json
Authorization: Bearer {{auth_token}}
```

#### 🧪 Postman Test Snippet

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Response time is less than 1000ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(1000);
});
```

---

### 🗄️ SQL Queries

- SQL statements to verify data integrity and correctness
- SELECT queries for data retrieval
- JOINs to validate relational consistency
- UPDATE and DELETE queries (tested on non-production environments)
- Validation of imported data

📄 File:
- `sql-queries-.md`

---

### 🔧 Bug Reports

- Categorized bug reports (cosmetic, functional, layout-related)
- Reproducible steps, expected and actual results, environment details
- Severity and priority tagging

📄 Example:
- `bug-reports-cosmetic-cloth-reserved.md`

---

### 📄 Test Plan

- Testing objectives and scope
- Features to be tested / not tested
- Roles, responsibilities, tools used
- Entry/Exit criteria and schedules

📄 Example:
- `test-plan.md`

---

### 🧾 Improvement Suggestions

- UI/UX feedback on layout and navigation
- Message clarity and accessibility feedback
- Actionable suggestions based on usability heuristics

📄 File:
- `Improvement.md`

---

## 🛠️ Tools & Technologies

- **Postman** (API testing, environments, scripting)
- **SQL** (MySQL – query validation)
- **Chrome DevTools** (Frontend and network debugging)
- **Excel / Markdown** (Manual test case writing)
- **GitHub** (Version control and collaboration)

---

## 🔗 Notes

- Each file in this repository represents a QA task or deliverable.
- Bug reports follow consistent structure for clarity and reproducibility.
- API testing is fully configured with headers, environments, tokens, and test validations.
- Test plan and test cases are aligned with QA best practices.

---

## 📧 Contact

If you have any questions or would like to get in touch, feel free to contact me via GitHub:  
🔗 https://github.com/neiraahmedbasic
