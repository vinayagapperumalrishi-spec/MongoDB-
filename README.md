# MongoDB-
Below is a professional **2-page README.md** for your MongoDB CRUD project. You can copy it directly into a file named **README.md** and upload it to GitHub.

---

# Student Database Management System

## MongoDB CRUD Operations Project

### Project Overview

This project demonstrates the implementation of **CRUD (Create, Read, Update, Delete)** operations using **MongoDB**. It is designed to help students understand database creation, collection management, document insertion, querying, updating, deleting, and MongoDB query operators.

The project uses a **Student Database** where each student record contains details such as **Name, Age, Course, and Status**.

---

## Objectives

* Create a MongoDB database and collection.
* Perform Create, Read, Update, and Delete operations.
* Practice MongoDB query operators.
* Build a simple real-world database application.

---

## Technologies Used

* MongoDB
* MongoDB Shell (mongosh)
* Visual Studio Code
* macOS / Windows

---

# Database Setup

```javascript
use studentDB
```

### Create Collection

```javascript
db.createCollection("students")
```

---

# Student Document Structure

```javascript
{
  name: "Rishi",
  age: 20,
  course: "MERN Stack",
  status: "Ongoing"
}
```

---

# CRUD Operations

## 1. Create

### Insert One Document

```javascript
db.students.insertOne({
name:"Rishi",
age:20,
course:"MERN Stack",
status:"Ongoing"
})
```

### Insert Multiple Documents

```javascript
db.students.insertMany([
{name:"Rahul",age:21,course:"Java",status:"Completed"},
{name:"Priya",age:22,course:"Python",status:"Ongoing"},
{name:"Arun",age:19,course:"MERN Stack",status:"Ongoing"}
])
```

---

## 2. Read

Display all students

```javascript
db.students.find()
```

Find MERN Stack students

```javascript
db.students.find({course:"MERN Stack"})
```

Find one student

```javascript
db.students.findOne({name:"Rishi"})
```

---

# Page 2

# Update Operations

### Update One Document

```javascript
db.students.updateOne(
{name:"Rishi"},
{$set:{status:"Completed"}}
)
```

### Update Multiple Documents

```javascript
db.students.updateMany(
{status:"Ongoing"},
{$set:{status:"Completed"}}
)
```

---

# Delete Operations

### Delete One Document

```javascript
db.students.deleteOne({name:"Rahul"})
```

### Delete All Documents

```javascript
db.students.deleteMany({})
```

---

# MongoDB Query Operators

### Greater Than

```javascript
db.students.find({age:{$gt:20}})
```

### Less Than

```javascript
db.students.find({age:{$lt:22}})
```

### IN Operator

```javascript
db.students.find({course:{$in:["Java","Python"]}})
```

### AND Operator

```javascript
db.students.find({
$and:[
{age:{$gt:19}},
{course:"MERN Stack"}
]
})
```

### OR Operator

```javascript
db.students.find({
$or:[
{course:"Java"},
{course:"Python"}
]
})
```

### EXISTS Operator

```javascript
db.students.find({
status:{$exists:true}
})
```

---

# Use Case

A **Student Database Management System** is used to manage student information. The administrator can:

* Add new students
* View student records
* Search students by course
* Update student status
* Delete unwanted records
* Filter data using MongoDB query operators

---

# Project Outcome

After completing this project, I learned to:

* Create MongoDB databases and collections.
* Perform CRUD operations.
* Use MongoDB query operators.
* Manage student records efficiently.
* Understand basic NoSQL database concepts.

---

## Conclusion

This project provides hands-on experience with MongoDB and NoSQL databases. It demonstrates how CRUD operations and query operators can be applied in real-world applications such as student management systems. The project strengthens practical knowledge of database management and prepares students for full-stack development using MongoDB.

---


