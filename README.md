
# 🍦 Energize Ice Cream Shop

A full-stack web application for a fictional ice cream shop — **Energize Ice Cream** — where customers can browse the menu, build a fully custom ice cream, manage their cart, and submit feedback. Built with vanilla HTML/CSS, React (via CDN), Node.js, Express, and MongoDB.

---

## 🌐 Live Pages

| Page | File | Description |
|------|------|-------------|
| 🏠 Home | `home.html` | Hero slideshow, navigation, store info & footer |
| 📋 Menu | `menu.html` | Browse flavours, bases, sauces, and toppings with prices |
| 🎨 Customize | `customize.html` | Interactive React-powered ice cream builder |
| 🛒 Cart | `cart.html` | View, update, and remove cart items |
| 💬 Feedback | `feedback.html` | Customer experience form |
| ℹ️ About Us | `aboutus.html` | Brand story and feature highlights |
| 🔐 Login | `login.html` | User authentication |
| 📝 Signup | `signup.html` | New user registration |

---

## ✨ Features

### 🎨 Ice Cream Customizer (React)
- Choose from **4 flavours** — Vanilla, Chocolate, Strawberry, Butterscotch
- Pick a **base** — Fudge, Brownie, or Waffle (₹60)
- Add a **sauce** — Chocolate, Caramel, or Red Velvet (₹40)
- Select **multiple toppings** — Sprinkles, Choco Chips, Nuts, Cherry, Oreo (₹10 each)
- Adjust **quantity** and see **live price calculation**
- One-click **Add to Cart**

### 🛒 Cart
- Persists items in `localStorage` and syncs with MongoDB via REST API
- Per-user cart (linked to authenticated session)
- Update quantity or remove individual items
- Clear entire cart

### 🔐 Authentication
- Email + password login and signup
- Session stored in `localStorage` (userId + userEmail)
- Protected routes redirect unauthenticated users to login

### 🖥️ UI / UX
- Auto-playing hero image slideshow on the home page
- Responsive layout with hamburger menu on mobile
- Hover animations and smooth transitions throughout
- Profile dropdown with logout option

---

## 🗂️ Project Structure

```
project/
├── home.html           # Landing page with slideshow
├── menu.html           # Menu listing (React)
├── customize.html      # Ice cream builder (React + Babel)
├── cart.html           # Shopping cart
├── feedback.html       # Feedback form
├── aboutus.html        # About page
├── login.html          # Login form
├── signup.html         # Registration form
├── pg1.css             # Global stylesheet
├── cart.js             # Cart price calculation helpers
├── server.js           # Express + MongoDB backend
├── Node.js             # Entry point / config
└── *.jpg/png/webp/avif # Ingredient & hero images
```

---

## 💰 Pricing Structure

| Item | Price |
|------|-------|
| Ice cream scoop (base) | ₹50 |
| Base (Fudge / Brownie / Waffle) | ₹60 |
| Sauce (Chocolate / Caramel / Red Velvet) | ₹40 |
| Each topping | ₹10 |

Total = `(50 + base + sauce + toppings × 10) × quantity`

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML5, CSS3, JavaScript (ES6+) |
| UI Component | React 18 (CDN) + Babel Standalone |
| Icons | Font Awesome 4.7 |
| Backend | Node.js + Express.js |
| Database | MongoDB + Mongoose |
| Auth | Custom (localStorage session) |

---

## 🚀 Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/) v14+
- [MongoDB](https://www.mongodb.com/) running locally on port `27017`


## 🔌 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/api/signup` | Register a new user |
| `POST` | `/api/login` | Authenticate and get userId |
| `GET` | `/api/cart/:userId` | Fetch all cart items for a user |
| `POST` | `/api/cart/:userId` | Add item to cart |
| `PUT` | `/api/cart/:userId/:itemId` | Update item quantity & total |
| `DELETE` | `/api/cart/:userId/:itemId` | Remove a specific item |
| `DELETE` | `/api/cart/:userId` | Clear entire cart |

---

## 📸 Screenshots

> Place screenshots in a `/screenshots` folder and update the paths below.

| Home | Customize | Cart |
|------|-----------|------|
| ![home](screenshots/home.png) | ![customize](screenshots/customize.png) | ![cart](screenshots/cart.png) |

---

## ⚠️ Known Limitations / Improvements

- Passwords are stored in plain text — add **bcrypt** hashing before deploying
- No JWT — consider adding token-based auth for production
- `menu.html` uses placeholder image URLs — replace with actual ingredient images
- No order/checkout flow yet — a natural next feature to add

---


