# Secure User Authentication System

This project implements a **secure user authentication system** using **Node.js, Express, MongoDB, and JWT**. Users can **register, log in, and access protected routes** securely.

## Features 🚀
- ✅ Secure **user registration & login**
- ✅ **Password hashing** using bcrypt.js
- ✅ **JWT-based authentication**
- ✅ **Role-based access control** (Admin/User)
- ✅ **Protected API routes**
- ✅ **MongoDB for persistent storage**

---

## Installation & Setup 🛠️

### **1️⃣ Clone the Repository**
git clone https://github.com/PoojithaTmlpkl/CODECRAFT_FD_1
cd UserAuthentication
``

## **2️⃣ Install Dependencies**
npm install


### **3️⃣ Set Up Environment Variables**
Create a `.env file in the root folder and add:
MONGO_URI=mongodb+srv://your_mongodb_url
JWT_SECRET=your_secret_key
PORT=5000


### **4️⃣ Run the Server**
node server.js
OR using **nodemon** (for auto-restart on changes):
npm install -g nodemon
nodemon server.js


---

## API Endpoints 📌

### **🔹 User Registration**
- **URL:** `POST /api/auth/register
- **Request Body:**

{
  "username": "testuser",
  "email": "test@example.com",
  "password": "securepassword"
}

- **Response:** `201 Created

### **🔹 User Login**
- **URL:** `POST /api/auth/login
- **Request Body:**

{
  "email": "test@example.com",
  "password": "securepassword"
}

- **Response:**

{
  "token": "your_jwt_token",
  "user": { "id": "123", "username": "testuser", "role": "user" }
}


### **🔹 Access Protected Route**
- **URL:** `GET /api/protected/dashboard
- **Headers:** `Authorization: Bearer your_jwt_token
- **Response:**

{
  "message": "Welcome to your dashboard, User ID: 123"
}


### **🔹 Admin-Only Route**
- **URL:** `GET /api/protected/admin
- **Headers:** `Authorization: Bearer your_jwt_token
- **Access:** Only users with role `admin



#3Folder Structure 📂

UserAuthentication/
├── models/
│   └── User.js  # User schema
├── routes/
│   ├── auth.js  # Auth routes
│   ├── protected.js  # Protected routes
├── middleware/
│   ├── authMiddleware.js  # JWT authentication
│   ├── roleMiddleware.js  # Role-based access control
├── .env  # Environment variables
├── server.js  # Main server file
├── package.json  # Dependencies
├── README.md  # Documentation


---

## Technologies Used 🛠️
- **Node.js** & **Express.js** (Backend Framework)
- **MongoDB** & **Mongoose** (Database)
- **bcrypt.js** (Password Hashing)
- **jsonwebtoken (JWT)** (Authentication)
- **dotenv** (Environment Variables)
- **CORS** (Security)

---

## Contributing 🤝
Feel free to contribute to this project! Fork the repository, create a feature branch, and submit a pull request. 🚀

---

## License 📜
This project is licensed under the MIT License.

