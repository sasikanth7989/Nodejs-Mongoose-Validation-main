Add Mongoose Schema Validation
📌 Project Overview

This project demonstrates how to apply Mongoose schema validation to ensure data integrity when inserting records into a MongoDB database.
It enforces rules like required fields, email format, value ranges, and allowed branch names.

🚀 Getting Started
1. Setup Project

Create a new Node.js + Express project and install dependencies:

mkdir mongoose-validation
cd mongoose-validation
npm init -y
npm install express mongoose body-parser

2. Connect to MongoDB

Use either a local MongoDB instance or MongoDB Atlas.

3. Define Schema with Validation

Create a Student schema with the following rules:

Name → required, minimum length of 3 characters

Roll No → required, unique, must be positive

Branch → must be one of: CSE, ECE, IT, MECH, CIVIL

Year → between 1 and 4

Email → required and must follow a valid email format

4. Create POST Route

Implement POST /students to insert a student.
Invalid inputs will trigger automatic validation errors.

5. Error Handling

Use Express middleware to catch validation errors and return:

400 Bad Request → When data violates schema rules

500 Internal Server Error → For unexpected issues

6. Run the Project

Start the server:

node app.js

📂 Project Structure
mongoose-validation/
 ├── app.js
 ├── package.json
 └── README.md

✅ Output
![WhatsApp Image 2025-09-19 at 09 49 23_a3d81c85](https://github.com/user-attachments/assets/a8695cbf-2fd3-4805-b0f4-5b22648535e3)

![WhatsApp Image 2025-09-19 at 09 49 24_c3e7e80a](https://github.com/user-attachments/assets/74d22af5-c184-447a-a7d0-887cdc93cc93)

