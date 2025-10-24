# Neuronix.AI - AI SaaS Platform

Neuronix.AI is a full-stack AI-powered SaaS platform built using the **PERN stack (PostgreSQL, Express.js, React, Node.js)**. It is a onestop solution which enables users to generate and manage AI-driven content with tools like background removal, text generation, image generation, resume review and more.

> ⚡️ Empower users with the potential of AI directly through your browser.

---

## 📁 Project Structure

```bash
Neuronix.AI/
|   ## Client Directory
├── client/                     # Frontend (React + Vite)
│   ├── node_modules/           # Node dependencies
│   ├── public/                 # Static assets (favicon, etc.)
│   ├── src/                    # Source code
│   │   ├── assets/             # Image and SVG assets
│   │   ├── components/         # Reusable components
│   │   ├── pages/              # Pages for routing
│   │   ├── App.jsx             # App shell
│   │   ├── index.css           # Global styles
│   │   └── main.jsx            # Entry point
│   ├── .env                    # Environment variables
│   ├── .gitignore
│   ├── eslint.config.js
│   ├── index.html
│   ├── package.json
│   ├── package-lock.json
│   └── vite.config.js          # Vite configuration
|
|   ## Server Directory
├── server/
├── node_modules/
├── config/                     # Configuration files
├── controllers/                # Route logic handlers
├── middlewares/               # Express middlewares
├── routes/                    # Route definitions
├── .env
├── package.json
├── package-lock.json
└── server.js                   # Server entry point
```

---

## ⚙️ Features

- 🔐 Authentication (Clerk-based)
- 👤 User profile and account management(Clerk-based)
- 🧠 AI Tools:
  - ✅ Background & Object Remover
  - ✍️ Article & Title Generator
  - 📸 Image Generator
  - 📄 Resume Review
- 📊 Dashboard with usage analytics
- 💲Subscription based features
- 🗃️ Saved history for previous AI interactions
- 🎨 Responsive UI with TailwindCSS

---

## 🛠️ Tech Stack

### Frontend
- React (Vite)
- Tailwind CSS
- Axios

### Backend
- Node.js
- Express.js
- PostgreSQL(Neon)

### AI & Tools
- Gemini API
- Clipdrop API (for image generation and background removal)
- Cloudinary (optional for media storage)

### Subscription and Authentication
- Clerk

---

## 🧪 Getting Started

### Prerequisites

- Node.js ≥ 18.x
- PostgreSQL Database(e.g.; Neon)
- Gemini API Key
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
npm run server

*localhost: 3000*
```

### 3. Setup Frontend

```bash
cd client
cp .env.example .env      # Add your frontend env vars
npm install
npm run dev

*localhost: 5173*
```

---

## 🔐 Environment Variables

### Server (`/server/.env`)
```env
DATABASE_URL = 'postgresql://user:password@localhost:5432/yourdb'
CLERK_PUBLISHABLE_KEY=clerk_public_api_key
CLERK_SECRET_KEY=clerk_secret_key
GEMINI_API_KEY = your_gemini_api_key
CLIPDROP_API_KEY = you_clipdrop_api_key
CLOUDINARY_CLOUD_NAME = your_cloud_name
CLOUDINARY_API_KEY = cloudinary_public_key
CLOUDINARY_API_SECRET = cloudinary_secret_key
```

### Client (`/client/.env`)
```env
VITE_BASE_URL=http://localhost:3000
VITE_CLERK_PUBLISHABLE_KEY=clerk_api_key
```

---

## 📦 API Endpoints

### 👤 User Routes (`/api/user`)
| Method | Endpoint                      | Middleware | Description                      |
|--------|-------------------------------|------------|----------------------------------|
| GET    | `/get-user-creations`         | `auth`     | Get user's own creations         |
| GET    | `/get-published-creations`    | `auth`     | Get all published creations      |
| POST   | `/toggle-like-creations`      | `auth`     | Toggle like/unlike on a creation |

### 🤖 AI Routes (`/api/ai`)
| Method | Endpoint                      | Middleware             | Description                                 |
|--------|-------------------------------|------------------------|---------------------------------------------|
| POST   | `/generate-article`           | `auth`                 | Generate an article using AI                |
| POST   | `/generate-blog-title`        | `auth`                 | Generate a blog title using AI              |
| POST   | `/generate-image`             | `auth`                 | Generate an image using AI                  |
| POST   | `/remove-image-background`    | `upload.single('image'), auth` | Remove background from uploaded image |
| POST   | `/remove-image-object`        | `upload.single('image'), auth` | Remove object from uploaded image     |
| POST   | `/resume-review`              | `upload.single('resume'), auth` | Review uploaded resume using AI       |

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 📌 Future Enhancements

- 🌐 Multilingual AI Support
- 💾 Cloud Storage for History and Media
- 📱 Mobile App version

---

## 🙌 Contributing

Feel free to fork the repository and submit pull requests.

> _“Create amazing content with the power of AI — Neuronix.AI simplifies creativity.”_
