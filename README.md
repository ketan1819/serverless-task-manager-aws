# serverless-task-manager-aws

# 🚀 Serverless Task Manager Application (AWS)

## 📌 Overview

This project demonstrates the development of a **serverless web application** using AWS services:

* AWS Lambda (Backend Logic)
* Amazon API Gateway (API Exposure)
* Amazon DynamoDB (Database)

The application performs basic **CRUD operations**:

* Create Task
* Get Tasks
* Delete Task

---

## 🏗️ Architecture

```
Client (Postman)
        ↓
API Gateway
        ↓
AWS Lambda
        ↓
DynamoDB (Tasks Table)
```

---

# 🧩 Implementation Steps

---

## 🔹 Step 1: Create DynamoDB Table

We created a table in:
👉 Amazon DynamoDB

### Configuration:

* Table Name: `Tasks`
* Primary Key: `taskId` (String)

### 📸 Screenshot:

![DynamoDB Table](images/dynamodb-table.png)

---

## 🔹 Step 2: Create Lambda Functions

We created **3 AWS Lambda functions** for different operations:

### 🔸 (a) CreateTask Function

* Inserts task into DynamoDB

### 🔸 (b) GetTasks Function

* Retrieves all tasks

### 🔸 (c) DeleteTask Function

* Deletes task using `taskId`

### 📸 Screenshot:

*Add screenshots of each function (CreateTask, GetTasks, DeleteTask) here*

---

## 🔹 Step 3: All Lambda Functions (Overview)

All three functions are visible in AWS Lambda dashboard.

### 📸 Screenshot:

*Add screenshot showing all Lambda functions in one frame*

---

## 🔹 Step 4: Create API Gateway

We created an API using:
👉 Amazon API Gateway (HTTP API)

### Sub-Steps:

1. Created HTTP API
2. Selected Lambda integrations
3. Added routes:

   * POST → `/create-tasks`
   * GET → `/get-all-tasks`
   * DELETE → `/delete-task`
4. Deployed API
5. Generated Invoke URL

### 📸 Screenshot:

*Add step-by-step screenshots of API Gateway creation*

---

## 🔹 Step 5: Testing using Postman

We tested all APIs using:
👉 Postman

### 🔸 Create Task (POST)

* URL: `/create-tasks`
* Body:

```json
{
  "taskId": "101",
  "taskName": "Final Demo"
}
```

### 🔸 Get Tasks (GET)

* URL: `/get-all-tasks`

### 🔸 Delete Task (DELETE)

* URL: `/delete-task`

### 📸 Screenshot:

*Add Postman screenshots for all API calls*

---

## 🔹 Step 6: Verify Data in DynamoDB

After API execution:

* Data was successfully inserted into DynamoDB
* Data was retrieved correctly
* Data was deleted successfully

### 📸 Screenshot:

*Add screenshot of DynamoDB table showing data*

---

# ✅ Results

* Successfully implemented serverless architecture
* All APIs working correctly
* Data stored and retrieved from DynamoDB
* End-to-end flow verified

---

# 🧠 Key Learnings

* Understanding of Serverless Architecture
* Working with AWS Lambda functions
* API creation using API Gateway
* NoSQL database operations using DynamoDB
* API testing using Postman

---

# 🎯 Conclusion

This project demonstrates a complete **serverless application workflow** using AWS services. It eliminates the need for managing servers and provides a scalable, efficient solution for backend development.

---

# 🏆 Technologies Used

* AWS Lambda
* Amazon API Gateway
* Amazon DynamoDB
* Postman

---

# 📢 Author

**Name:** Ketan Sonawane
**Course:** Cloud Native Application
**Activity:** Serverless Application Development

---
