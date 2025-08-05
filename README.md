QA Portfolio – Neira Ahmedbasic

Welcome to my QA portfolio! This repository showcases my practical work in manual testing, API testing with Postman, SQL validation, structured bug reporting, and usability improvements. The goal of this portfolio is to demonstrate my knowledge and hands-on experience in software testing across different tools and methodologies.

📁 Contents
✅ Manual Testing
Test cases for mobile and web applications (iOS apps, chat apps, e-commerce flows)

Boundary Value Analysis (BVA) and Equivalence Partitioning (EP)

Pre-test and Re-test scenarios

Usability feedback focusing on layout, navigation, and messaging clarity

Structured bug reports with detailed reproduction steps, expected vs. actual results

Test Plan documents describing scope, objectives, tools, and schedules

📄 Example Files:

Improvement.md

QA_Test_Cases_and_Bug_Reports.md

boundary-value-analysis-week3.md

bug-reports-cosmetic-cloth-reserved.md

🧾 Test Case Example
vbnet
Kopiraj
Uredi
Test Case ID: TC_VIBER_001  
Title: Validate Viber chat functionality without internet connection  
Platform: iPhone 13, App version 25.5.2  
Steps:  
1. Turn off mobile data and Wi-Fi  
2. Open Viber  
3. Try to send a message  
Expected result: Message fails to send with appropriate offline notification  
🔌 API Testing – Postman
Full Postman collections with organized folders for each endpoint

Tests include GET, POST, PUT, DELETE methods

Use of Authorization tokens (Bearer Token) and environment variables for secure handling of sensitive data

Validation of JSON request bodies and response schemas with test scripts

Automated test runs via Postman Collection Runner or Newman

Well-defined headers such as Content-Type and Authorization

Exported test reports documenting results and coverage

📄 File:

postman-petstore-api-tests.md

🗄️ SQL Queries
SQL statements for verifying data integrity and correctness

SELECT queries for data retrieval and validation

JOINs to ensure relational consistency

UPDATE and DELETE queries executed on non-production environments

Validation of imported and migrated data

📄 File:

sql-queries-.md

🔧 Bug Reports
Categorized bug reports (functional, cosmetic, layout-related)

Clear and reproducible steps with expected and actual results

Detailed environment and severity/priority classification

📄 Example:

bug-reports-cosmetic-cloth-reserved.md

🔗 Notes
All files in this repository represent real QA deliverables and tasks

Bug reports follow a consistent and clear format for easy reproducibility

API testing includes detailed validations, token management, and error handling

Test plans and cases align with industry best practices for comprehensive coverage

