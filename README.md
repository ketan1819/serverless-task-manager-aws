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

![DynamoDB Table](photos/1.png)
![DynamoDB Table](photos/10.png)

---

## 🔹 Step 2: Create Lambda Functions

We created **3 AWS Lambda functions** for different operations:
![](photos/2.png)


### 🔸 (a) CreateTask Function

* Inserts task into DynamoDB

![](photos/3.png)
![](photos/4.png)

### 🔸 (b) GetTasks Function

* Retrieves all tasks

![](photos/5.png)
![](photos/6.png)

### 🔸 (c) DeleteTask Function

* Deletes task using `taskId`

![](photos/7.png)
![](photos/8.png)
![](photos/9.png)



---

## 🔹 Step 3: All Lambda Functions (Overview)

All three functions are visible in AWS Lambda dashboard.

### 📸 Screenshot:
![](photos/22.png)


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
![](photos/11.png)
![](photos/12.png)
![](photos/13.png)
![](photos/14.png)
![](photos/15.png)


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
## 📸 Screenshot:
![](photos/16.png)
![](photos/17.png)

### 🔸 Get Tasks (GET)

* URL: `/get-all-tasks`

## 📸 Screenshot:
![](photos/18.png)

### 🔸 Delete Task (DELETE)

* URL: `/delete-task`

## 📸 Screenshot:
![](photos/19.png)

### Result : After deleting task whose id is 101
## 📸 Screenshot:
![](photos/20.png)

---

## 🔹 Step 6: Verify Data in DynamoDB

After API execution:

* Data was successfully inserted into DynamoDB
* Data was retrieved correctly
* Data was deleted successfully

### 📸 Screenshot:
![](photos/21.png)



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
