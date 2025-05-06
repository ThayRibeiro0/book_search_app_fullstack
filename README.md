
# 📚 Book Search App

A fully functional full-stack MERN application originally built with a RESTful API and later refactored to use a GraphQL API with Apollo Server. It allows users to search for books using the Google Books API, save their favorite books, and manage them through a secure user dashboard.

## 🛠️ Tech Stack

**Front-End:**
- React.js (Vite)
- CSS
- Vite Proxy

**Back-End:**
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT Authentication
- dotenv for environment configuration

## Deployed:
[Check the live application here]([https://book-search-app-ft8h.onrender.com](https://book-search-app-fullstack.onrender.com/))


## Screenshot
  <img src="./client/public/Home.png" alt="React_Book_Search_Engine" width="600" height="300">

---

## 🚀 Features

- 🔍 Search books via Google Books API
- 💾 Save & delete favorite books
- 🔐 User authentication using JWT
- 👤 Personalized dashboard for each user
- 📱 Responsive UI for all screen sizes

---

## ⚙️ Installation

### 📦 Backend

```bash
cd server
npm install
npm run build
npm start
```

Make sure to include your MongoDB URI and JWT secret in `.env`:

```
MONGODB_URI=your_mongo_uri
JWT_SECRET=your_jwt_secret
```

### 💻 Frontend

```bash
cd client
npm install
npm run dev
```

Ensure your `vite.config.ts` (or `.js`) has the proxy configured:

```ts
server: {
  port: 10000,
  proxy: {
    '/api': {
      target: 'http://localhost:3001',
      changeOrigin: true
    }
  }
}
```

---

## 🌐 Deployment

### 🔧 Render (Server)

- Root Directory: `server/`
- Build Command: `cd client && npm install && npm run build`
- Start Command: `cd client/dist && npx serve -p 10000`

Make sure your server uses:

```ts
const PORT = parseInt(process.env.PORT || '10000', 10); // Use the default Render port
```

---

## 🧪 API Reference

### 🔑 Auth

- `POST /api/signup` – create account
- `POST /api/login` – authenticate user

### 📚 Books

- `GET /api/saved/search?query=...` – search books
- `POST /api/saved` – save book
- `GET /api/saved` – get saved books
- `DELETE /api/saved/:id` – delete book

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
