# 🍔 FOODIES – Full Stack MERN Application

FOODIES is a **full‑stack food ordering & management platform** built using the **MERN stack (MongoDB, Express, React, Node.js)**. The application supports **users, sellers, products, carts, and orders**, with a clean separation between **client (frontend)** and **server (backend)**.

This README explains the **project architecture, folder structure, request flow, and key design decisions** in an **interview‑ready format**.

---

## 🚀 Tech Stack

### Frontend (Client)

* **React (Vite)**
* **Context API** for state management
* **Tailwind CSS** for styling
* **React Router DOM**

### Backend (Server)

* **Node.js**
* **Express.js**
* **MongoDB + Mongoose**
* **JWT Authentication**
* **Multer + Cloudinary** (Image Uploads)

### Deployment

* **Vercel** (Frontend & Backend)

---

## 📂 Project Structure

```
FOODIES/
│
├── client/          # Frontend (React)
├── server/          # Backend (Node + Express)
├── README.md
```

---

# 🖥️ CLIENT (Frontend)

```
client/
├── public/
├── src/
│   ├── assets/
│   ├── components/
│   │   └── seller/
│   ├── context/
│   │   └── AppContext.jsx
│   ├── pages/
│   │   ├── seller/
│   │   ├── Cart.jsx
│   │   ├── HomePage.jsx
│   │   ├── MyOrders.jsx
│   │   ├── ProductCategory.jsx
│   │   └── Profile.jsx
│   ├── App.jsx
│   ├── main.jsx
│   ├── products.js
│   └── index.css
├── .env
├── tailwind.config.js
├── vite.config.js
└── package.json
```

---

## 🔹 `src/components/`

Reusable UI components used across multiple pages.

### Seller Components

* `SellerLayout.jsx` – Layout wrapper for seller dashboard
* `SellerLogin.jsx` – Seller authentication
* `Navbar.jsx`, `Footer.jsx` – Global layout components
* `FoodCard.jsx` – Product card UI
* `BestSeller.jsx`, `WhyWeAreBest.jsx` – Marketing sections

**Interview Explanation:**

> Components are reusable, presentation‑focused units that keep pages clean and maintainable.

---

## 🔹 `src/pages/`

Pages represent **route‑level components**.

### User Pages

* `HomePage.jsx` – Landing page
* `Cart.jsx` – Cart management
* `MyOrders.jsx` – User order history
* `Profile.jsx` – User profile
* `ProductCategory.jsx` – Category‑wise products

### Seller Pages

* `AddProducts.jsx` – Add new products
* `Orders.jsx` – Seller order management
* `ProductList.jsx` – Seller products

**Interview Explanation:**

> Pages handle routing and orchestration, while components focus on UI.

---

## 🔹 `src/context/AppContext.jsx`

* Global state management
* Stores user, cart, auth state

**Interview Line:**

> Context API helps avoid prop drilling and centralizes shared state.

---

## 🔹 `App.jsx` & `main.jsx`

* `main.jsx` – React entry point
* `App.jsx` – Route definitions and layout setup

---

# 🛠️ SERVER (Backend)

```
server/
├── config/
├── controller/
├── middleware/
├── models/
├── routes/
├── index.js
├── .env
├── package.json
└── vercel.json
```

---

## 🔹 `config/`

Handles **external services and app configuration**.

* `db.js` – MongoDB connection
* `cloudinary.js` – Cloudinary setup
* `multer.js` – File upload handling

---

## 🔹 `models/` (Database Layer)

Defines MongoDB schemas using Mongoose.

* `UserModel.js` – Users & authentication
* `Product.js` – Products
* `order.js` – Orders
* `address.js` – Delivery addresses

**Interview Line:**

> Models enforce schema consistency and simplify DB operations.

---

## 🔹 `controller/` (Business Logic)

Contains core application logic.

* `userController.js`
* `sellerController.js`
* `productController.js`
* `cartController.js`
* `orderController.js`
* `addressController.js`

**Interview Line:**

> Controllers separate business logic from routing.

---

## 🔹 `middleware/`

* `authUser.js` – User JWT authentication
* `authSeller.js` – Seller authentication

**Interview Line:**

> Middleware ensures security and avoids code duplication.

---

## 🔹 `routes/`

Defines REST API endpoints.

* `userRoute.js`
* `sellerRoute.js`
* `productRoute.js`
* `cartRoute.js`
* `orders.js`
* `addressRoute.js`

---

## 🔹 `index.js` (Backend Entry Point)

* Initializes Express
* Connects DB
* Registers middleware
* Mounts routes
* Starts server

---

# 🔁 API Request Flow

```
Client → Route → Middleware → Controller → Model → Response
```

**Interview Explanation:**

> This flow ensures security, clean logic separation, and scalability.

---

# 🔐 Authentication

* JWT‑based authentication
* Separate roles: **User & Seller**
* Token verified using middleware

---

# 📦 Key Features

* User & Seller authentication
* Product management
* Cart & checkout flow
* Order tracking
* Image uploads via Cloudinary
* Responsive UI

---

# ⚙️ Environment Variables

### Client

```
VITE_API_URL=...
```

### Server

```
MONGO_URI=...
JWT_SECRET=...
CLOUDINARY_KEY=...
```

---

# ▶️ How to Run Locally

### Backend

```bash
cd server
npm install
npm run dev
```

### Frontend

```bash
cd client
npm install
npm run dev
```

---

# 🎯 Architecture Strengths (Interview Ready)

* Modular & scalable
* Clean MVC separation
* Secure authentication
* Production‑ready structure

---

# 👤 Author

**Omkar Bandikatte**
Full Stack Developer | MERN Stack

---
