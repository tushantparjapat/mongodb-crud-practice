# MongoDB CRUD Practice 🗃️

This project demonstrates the use of **MongoDB** for performing full CRUD operations (Create, Read, Update, Delete) on a sample `users` collection.

---

## 🛠️ Project Setup

- **Database**: `mern_app`
- **Collection**: `users`
- **Tool Used**: MongoDB Compass & Mongo Shell
- **Tech Stack**: JavaScript, MongoDB, Node.js

---

## 📄 Sample Document Structure

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "age": 30,
  "role": "admin"
}
```
##✅ CRUD Operations
Create
```js
db.users.insertOne({ name: "Jane", email: "jane@example.com", age: 28, role: "user" })
```
Read
```
Find all users:
```js
db.users.find()
```
Filter:
```js
db.users.find({ age: { $gt: 25 } })
```
```

Projection:
```js
db.users.find({}, { name: 1, email: 1 })
```

Update:
```js
db.users.updateOne({ name: "Jane" }, { $set: { role: "admin" } })
```

Delete:
```js
db.users.deleteMany({ age: { $gt: 50 } })
```
