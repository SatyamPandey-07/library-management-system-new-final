# 📚 Library Management System

A **sexy**, modern, and fully responsive **Library Management System** built with **React, Tailwind CSS, Node.js, Express, and MongoDB**.

🔥 **Includes neon buttons, framer-motion animations, dark mode toggle, and a GitHub-themed UI.**

---

## 🚀 Tech Stack

### Frontend
- ⚛️ **React.js + Vite** – Superfast & modular
- 🎨 **Tailwind CSS** – Stylish utility-first design
- 🔀 **Framer Motion** – Satisfying page transitions
- 🔥 **Lottie** – Beautiful animations
- 🍞 **React Toastify** – Toast notifications
- 🔁 **React Router DOM** – Smooth routing
- 📦 **Axios** – Seamless API communication
- 🌘 **Dark/Light Mode Toggle** – Global context-based

### Backend
- 🖥️ **Node.js + Express.js** – Fast and scalable API server
- 🍃 **MongoDB + Mongoose** – NoSQL DB for all books/users
- 🔐 **JWT Authentication** – Secure login/signup
- 🪲 **Bcrypt.js** – Hashed passwords for safety
- 🛉 **Nodemailer** – Email verification system

---

## ✨ Key Features

### Frontend
✅ GitHub-themed UI with Dark/Light toggle  
✅ Lottie animations on Signup page  
✅ Neon buttons, glowing hover effects  
✅ Role-based Dashboards (User/Admin)  
✅ Live stats (Books, Users, Rentals)  
✅ Search, Filter, and Pagination  
✅ Toasts for all actions  
✅ Framer-motion modals and animations  
✅ Mobile responsive (fully adaptive)

### Backend
✅ JWT & Bcrypt authentication  
✅ Role-based logic (Admin/User)  
✅ User verification via email (with token)  
✅ CRUD for books, rentals, and users  
✅ Status tracking & dashboard counters  
✅ Secure MongoDB queries with Mongoose  
✅ Reusable controller structure

---

## 📁 Folder Structure

```bash
library-management/
├── backend/
│   ├── config/             # MongoDB & ENV configs
│   ├── controllers/        # Route logic for Auth, Books, Rentals
│   ├── middleware/         # Auth checks & role guards
│   ├── models/             # Mongoose schemas
│   ├── routes/             # API route files
│   ├── utils/              # Token generation, mailer, etc.
│   └── server.js           # Main server entry point
│
├── frontend/
│   ├── public/             # Static files
│   └── src/
│       ├── assets/         # Lottie files, images, etc.
│       ├── components/     # Buttons, Navbar, Modal, StatsCard
│       ├── context/        # ThemeProvider (Dark/Light mode)
│       ├── hooks/          # Custom hooks (if any)
│       ├── pages/          # All Pages (Home, Signup, AdminDashboard)
│       ├── routes/         # React Router-based route structure
│       ├── services/       # Axios instances and API services
│       ├── App.jsx         # Root Component
│       ├── main.jsx        # App entry
│       └── index.css       # Global styles
├── .env                    # Env variables
├── .gitignore
├── README.md               # Project info
└── package.json (x2)       # One in frontend & one in backend
```

---

## 🔐 Authentication Flow
- User signs up → gets verification email
- Email token verifies user → isVerified = true
- Login with JWT → role-based access: admin or user

### Admin Panel:
- Book Management, Rental Requests, User Control

### 📊 Admin Dashboard Overview
- 📚 Total Books, Users, Rentals
- ⚙️ Approve/Reject Rental Requests
- 🠍 View Unverified Users
- ❌ Close Rental Issues
- 📈 Charts with recharts or chart.js
- 🎯 Stats: Avatars from Dicebear / UI-Avatars

---

## 🛠️ Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/library-management.git
cd library-management
```

### 2️⃣ Setup Backend
```bash
cd backend
npm install
npm run dev # Runs on http://localhost:5000
```

### 3️⃣ Setup Frontend
```bash
cd frontend
npm install
npm run dev # Runs on http://localhost:5173
```

### .env Requirements (backend/.env)
```ini
MONGO_URI=your_mongo_uri
JWT_SECRET=your_jwt_secret
EMAIL_USER=your_email
EMAIL_PASS=your_email_password
BASE_URL=http://localhost:5000
```

---

## 🔗 API Endpoints

| Method | Route                    | Access       | Description               |
|--------|--------------------------|--------------|---------------------------|
| POST   | /api/auth/signup         | Public       | Register user             |
| POST   | /api/auth/login          | Public       | Login user                |
| GET    | /api/users/verify/:id    | Public       | Email verification        |
| GET    | /api/books               | Public       | Get all books             |
| POST   | /api/books               | Admin Only   | Add new book              |
| PUT    | /api/books/:id           | Admin Only   | Update book               |
| DELETE | /api/books/:id           | Admin Only   | Delete book               |
| POST   | /api/rentals/request     | User         | Request a book rental     |
| POST   | /api/rentals/close/:id   | Admin        | Close rental issue        |

---

## 📸 UI Preview

| Page            | Features                                                |
|-----------------|---------------------------------------------------------|
| HomePage        | Hero split layout, Lottie, Neon CTA, Typewriter headline |
| Signup/Login    | Floating Labels, Dark UI, Toasts, Verification logic     |
| Admin Panel     | User list, Rentals list, Charts, Modals, Dicebear avatars |
| User Panel      | Borrowed books list, Status indicators, Animations       |
| Book Listings   | Search, Filter, Pagination, Book Cards with animations   |

---

## 💡 Future Plans
- [ ] Add multi-step book request system
- [ ] Charts (bar/pie) with filters
- [ ] Email templates with inline CSS
- [ ] PDF export of user borrow history
- [ ] Bookmark system for users

---

## 🤝 Contributing
Pull requests are welcome!  
Create an issue or suggestion before major PRs.  
Fork this repo and show off your creativity 🚀

---

## 📜 License
This project is open-source under the MIT License.

💥 Happy coding from **Satyam Pandey’s Library Squad!**
