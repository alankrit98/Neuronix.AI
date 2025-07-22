# Neuronix.AI - AI SaaS Platform

Neuronix.AI is a full-stack AI-powered SaaS platform built using the **PERN stack (PostgreSQL, Express.js, React, Node.js)**. It enables users to generate and manage AI-driven content with tools like background removal, text generation, image generation, and more.

> ⚡️ Empower users with the potential of AI directly through your browser.

---

## 📁 Project Structure

```bash
├── client/        # React frontend (Vite + Tailwind)
├── server/        # Node.js backend with Express and PostgreSQL
├── LICENSE        # MIT License
├── README.md      # Project documentation
```

---

## ⚙️ Features

- 🔐 Authentication (JWT-based)
- 👤 User profile and account management
- 🧠 AI Tools:
  - ✅ Background Remover
  - ✍️ Text Generator
  - 💬 Chatbot Interface
  - 💻 Code Assistant
- 📊 Dashboard with usage analytics
- 🗃️ Saved history for previous AI interactions
- 🎨 Responsive UI with TailwindCSS
- 🌍 Fully deployed ready (Docker / Railway / Render compatible)

---

## 🛠️ Tech Stack

### Frontend
- React (Vite)
- Tailwind CSS
- Zustand (State Management)
- Axios

### Backend
- Node.js
- Express.js
- PostgreSQL
- Prisma ORM

### AI & Tools
- OpenAI API
- Clipdrop API (for image generation and background removal)
- Cloudinary (optional for media storage)

---

## 🧪 Getting Started

### Prerequisites

- Node.js ≥ 18.x
- PostgreSQL installed and running
- OpenAI API Key
- Clipdrop API Key

### 1. Clone the Repository

```bash
git clone https://github.com/alankrit98/neuronix-ai.git
cd neuronix-ai
```

### 2. Setup Backend

```bash
cd server
cp .env.example .env      # Update your env with DB and API keys
npm install
npm run dev
```

### 3. Setup Frontend

```bash
cd client
cp .env.example .env      # Add your frontend env vars
npm install
npm run dev
```

---

## 🔐 Environment Variables

### Server (`/server/.env`)
```env
DATABASE_URL=postgresql://user:password@localhost:5432/yourdb
JWT_SECRET=your_jwt_secret
OPENAI_API_KEY=your_openai_key
CLIPDROP_API_KEY=your_removebg_key
```

### Client (`/client/.env`)
```env
VITE_BACKEND_URL=http://localhost:5000
VITE_OPENAI_API_KEY=your_openai_key
```

---

## 📦 API Routes

### `/api/auth`
- `POST /register`
- `POST /login`

### `/api/user`
- `GET /profile`
- `PUT /update`

### `/api/ai`
- `POST /text-generation`
- `POST /background-removal`
- `POST /chatbot`

---

## 🧑‍💻 Author

- **Alankrit Agarwal**  
  [GitHub](https://github.com/alankrit98) | [LinkedIn](https://linkedin.com/in/alankrit-agarwal)

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

---

## 📌 Future Enhancements

- ✅ Admin Panel for monitoring
- 📥 Subscription & Billing Integration
- 🌐 Multilingual AI Support
- 💾 Cloud Storage for History and Media
- 📱 Mobile App version

---

> _“Create amazing content with the power of AI — Neuronix.AI simplifies creativity.”_
