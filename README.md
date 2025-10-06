# Codeplus

````markdown
# 🚀 CodePlus

**CodePlus** is a real-time problem-solving and collaborative coding platform built using the **MERN Stack** (MongoDB, Express.js, React, Node.js) with **Socket.IO** for instant communication and **Ngrok** for backend tunneling during local development.  
The platform allows users to engage in **1v1 coding challenges, problem-solving rooms, and learning discussions** — all in real-time.

---

## 🧠 Tech Stack

### **Frontend**
- ⚡ **Vite + React.js** — for a blazing-fast and modern UI development experience
- 🎨 **Tailwind CSS** — for responsive and clean design
- 🔄 **Socket.IO Client** — for real-time communication
- 🌐 **Axios** — for API requests
- 🔑 **React Router DOM** — for client-side routing

### **Backend**
- 🧩 **Node.js + Express.js** — server-side framework
- 🗄️ **MongoDB + Mongoose** — NoSQL database for user data, room data, and chat history
- 🧠 **Socket.IO Server** — enables 1v1 communication and room management
- 🌍 **Ngrok** — exposes the local backend to the internet for testing

---

## ⚙️ Installation & Setup

Follow these steps to run the project locally 👇

### 1️⃣ Clone the repository
```bash
git clone https://github.com/your-username/codeplus.git
cd codeplus
````

---

### 2️⃣ Install dependencies

#### Backend

```bash
cd codeplus-backend
npm install express cors mongoose socket.io http path ngrok dotenv
```

#### Frontend

```bash
cd ../codeplus-frontend
npm create vite@latest .
# Select React + JavaScript
npm install
npm install axios socket.io-client react-router-dom tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

---

### 3️⃣ Setup Tailwind CSS

In `tailwind.config.js`:

```js
content: ["./index.html", "./src/**/*.{js,ts,jsx,tsx}"],
theme: {
  extend: {},
},
plugins: [],
```

In `index.css`:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

---

### 4️⃣ Setup MongoDB Connection (Backend)

In your backend folder, create a `.env` file:

```bash
MONGO_URI=mongodb+srv://<your-username>:<your-password>@cluster.mongodb.net/codeplus
PORT=5000
```

And in `server.js` (or `index.js`):

```js
import mongoose from "mongoose";
mongoose.connect(process.env.MONGO_URI)
  .then(() => console.log("✅ MongoDB connected"))
  .catch(err => console.log("❌ MongoDB error:", err));
```

---

### 5️⃣ Run the Servers

#### Backend

```bash
cd codeplus-backend
node server.js
```

#### Frontend

```bash
cd ../codeplus-frontend
npm run dev
```

---

### 6️⃣ Using Ngrok for Tunneling (Backend)

Ngrok exposes your local backend to the internet — useful for connecting with others in real-time or testing external APIs.

#### Install Ngrok (One-time)

```bash
npm install -g ngrok
```

#### Run Ngrok Tunnel

```bash
ngrok http 5000
```

Copy the generated HTTPS link and update it in your frontend’s `.env`:

```bash
VITE_BACKEND_URL=https://your-ngrok-url.ngrok-free.app
```

---

## ⚡ Features

* 👤 **User Authentication** — secure login & signup using MongoDB
* 💬 **1v1 Problem Room** — real-time interaction via Socket.IO
* 🧑‍💻 **Code Collaboration** — live discussion and sharing
* 🌈 **Vite + Tailwind UI** — super-fast and modern interface
* 🌍 **Ngrok Integration** — for easy backend sharing
* 🧠 **MERN Architecture** — modular and scalable

---

## 📁 Project Structure

```
codeplus/
codeplus-frontend/
│
├── public/
│   └── index.html
│
├── src/
│   ├── App.jsx
│   ├── index.js
│   ├── img.png
│
│   ├── pages/
│   │   ├── Login.jsx
│   │   ├── Signup.jsx
│   │   ├── Home.jsx
│   │   ├── ProblemSolve.jsx
│   │   └── OneVOne.jsx
│
│   ├── components/
│   │   └── (optional shared components like Navbar, Button, etc.)
│
├── package.json
└── README.md
│
└codeplus-backend/
 │
 ├── server.js              <-- Socket.IO + Express
 ├── config/
 │    └── db.js             <-- MongoDB connection
 ├── models/
 │    ├── User.js
 │    ├── Problem.js
 │    └── Solution.js
 ├── routes/
 │    ├── authRoutes.js
 │    ├── problemRoutes.js
 │    └── progressRoutes.js
 ├── controllers/
 │    ├── authController.js
 │    ├── problemController.js
 │    └── progressController.js
 └── middleware/
      └── authMiddleware.js


---

## 🧩 Environment Variables

Create `.env` files for both backend and frontend:

### **Backend `.env`**

```
PORT=5000
MONGO_URI=<your-mongo-connection-string>
```

### **Frontend `.env`**

```
VITE_BACKEND_URL=http://localhost:5000
# or Ngrok link when tunneling
```

---

## 💡 Development Notes

* The frontend and backend must run simultaneously.
* When using Ngrok, the backend URL in frontend `.env` must be updated.
* Always restart the frontend after changing `.env` variables.
* MongoDB should be running before launching the backend.

---

## 🧪 Commands Summary

| Command           | Description                     |
| ----------------- | ------------------------------- |
| `npm install`     | Install dependencies            |
| `npm run dev`     | Start frontend (Vite)           |
| `node server.js`  | Start backend                   |
| `ngrok http 5000` | Start Ngrok tunnel              |
| `npm run build`   | Build production-ready frontend |

---

## 🌐 Deployment (Optional)

You can deploy:

* Frontend → **Vercel / Netlify**
* Backend → **Render / Railway / AWS**
* Database → **MongoDB Atlas**

---

## 👨‍💻 Contributors

* **Krishnagopal Tyagi** — Full Stack Developer
* **[Your Teammates’ Names]** — Contributors

---

## 🛡️ License

This project is licensed under the **MIT License** — feel free to use, modify, and distribute it.

---

## ⭐ Acknowledgments

* [Vite](https://vitejs.dev/)
* [Tailwind CSS](https://tailwindcss.com/)
* [MongoDB](https://www.mongodb.com/)
* [Socket.IO](https://socket.io/)
* [Ngrok](https://ngrok.com/)
* [Node.js](https://nodejs.org/)

---

```

---

Would you like me to **customize it for your exact folder structure and filenames** (like `server.js`, `User.js`, etc.) so it perfectly fits your CodePlus repo?  
If yes — please upload or paste your folder structure here.
```
