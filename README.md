# QuickBlog 📝

A full-stack AI-powered blogging platform built with **React**, **Node.js**, **Express**, **MongoDB**, and **Groq AI**.

![GitHub repo size](https://img.shields.io/github/repo-size/ShrayansKumar/QuickBlog)
![GitHub last commit](https://img.shields.io/github/last-commit/ShrayansKumar/QuickBlog)
![License](https://img.shields.io/badge/license-MIT-green)

---

## 🚀 Features

- 📰 Create, edit, and publish blog posts
- 🤖 AI-powered blog content generation using **Groq AI**
- 🔐 Admin authentication with **JWT**
- 🖼️ Image upload via **Multer**
- 💬 Comment system
- 🌐 Full REST API backend
- 📱 Responsive React frontend

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React, Vite, Tailwind CSS |
| Backend | Node.js, Express.js |
| Database | MongoDB Atlas, Mongoose |
| Auth | JWT (JSON Web Tokens) |
| AI | Groq AI API |
| Image Upload | Multer |
| Deployment | Render (backend), Vercel (frontend) |

---

## 📁 Project Structure

QuickBlog/

├── client/                 # React frontend (Vite)

│   ├── public/

│   └── src/

│       ├── components/

│       ├── pages/

│       └── App.jsx

│

└── server/                 # Express backend

├── configs/            # DB & AI config

├── controllers/        # Route logic

├── middleware/         # Auth, Multer

├── models/             # Mongoose schemas

├── routes/             # API routes

└── server.js

---

## ⚙️ Getting Started

### Prerequisites
- Node.js v18+
- MongoDB Atlas account
- Groq API key → [console.groq.com](https://console.groq.com)

---

### 1. Clone the repo

```bash
git clone https://github.com/ShrayansKumar/QuickBlog.git
cd QuickBlog
```

---

### 2. Setup Server

```bash
cd server
npm install
```

Create `server/.env`:
```env
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
GROQ_API_KEY=your_groq_api_key
ADMIN_EMAIL=your_admin_email
ADMIN_PASSWORD=your_admin_password
```

```bash
npm run server
```

---

### 3. Setup Client

```bash
cd client
npm install
```

Create `client/.env`:
```env
VITE_BASE_URL=http://localhost:3000
```

```bash
npm run dev
```

---

## 📡 API Endpoints

### Blog Routes `/api/blog`

| Method | Endpoint | Auth | Description |
|--------|----------|------|-------------|
| GET | `/all` | ❌ | Get all blogs |
| GET | `/:blogId` | ❌ | Get blog by ID |
| POST | `/add` | ✅ | Add new blog (with image) |
| POST | `/delete` | ✅ | Delete a blog |
| POST | `/toggle-publish` | ✅ | Toggle publish status |
| POST | `/add-comment` | ❌ | Add a comment |
| POST | `/comments` | ❌ | Get blog comments |
| POST | `/generate` | ✅ | Generate AI content via Groq |

---

## 🌍 Deployment

### Backend → Render
- Connect GitHub repo on [render.com](https://render.com)
- Set environment variables in Render dashboard
- Auto-deploys on every push to `main`

### Frontend → Vercel
- Connect GitHub repo on [vercel.com](https://vercel.com)
- Set `VITE_BASE_URL` to your Render backend URL
- Auto-deploys on every push to `main`

---

## 🔐 Environment Variables

| Variable | Description |
|----------|-------------|
| `MONGODB_URI` | MongoDB Atlas connection string |
| `JWT_SECRET` | Secret key for JWT signing |
| `GROQ_API_KEY` | Groq AI API key |
| `ADMIN_EMAIL` | Admin login email |
| `ADMIN_PASSWORD` | Admin login password |
| `VITE_BASE_URL` | Backend API URL (client side) |

---

## 👨‍💻 Author

**Shrayans Kumar**
- GitHub: [@ShrayansKumar](https://github.com/ShrayansKumar)

---

## 📄 License

This project is licensed under the **MIT License**.