# 🌾 Krishi Samadhan — Agricultural AI Assistant

A full-stack MERN application providing multilingual agricultural intelligence to Indian farmers, powered by the Anthropic Claude API.

## ✨ Features

- 🌍 **10 Indian Languages** — Hindi, Marathi, Punjabi, Telugu, Tamil, Kannada, Gujarati, Bengali, Odia, Malayalam
- 🤖 **Claude AI** — Expert agricultural advice on crops, soil, pests, weather, schemes
- 📷 **Image Analysis** — Upload crop/plant photos for disease & pest identification
- 🎙️ **Voice Input** — Speak in your language using browser Speech Recognition
- 📍 **Location-aware** — Region-specific advice based on your district/state
- 💬 **Conversation History** — Saved per-user chat sessions in MongoDB
- 🔐 **JWT Auth** — Secure user registration and login

## 🛠️ Tech Stack

| Layer    | Technology                        |
|----------|-----------------------------------|
| Frontend | React 18, Tailwind CSS, Axios     |
| Backend  | Node.js, Express.js               |
| Database | MongoDB + Mongoose                |
| AI       | Anthropic Claude API (claude-sonnet-4-6) |
| Auth     | JWT + bcrypt                      |

## 📁 Project Structure

```
krishi-samadhan/
├── server/                  # Express backend
│   ├── models/              # Mongoose schemas
│   ├── routes/              # API routes
│   ├── controllers/         # Route handlers
│   ├── middleware/          # Auth middleware
│   ├── server.js            # Entry point
│   └── .env.example         # Environment variables template
├── client/                  # React frontend
│   ├── public/
│   └── src/
│       ├── components/      # Reusable UI components
│       ├── pages/           # Page-level components
│       ├── context/         # React Context (Auth, Chat)
│       ├── hooks/           # Custom hooks
│       └── utils/           # API helpers
└── package.json             # Root scripts
```

## 🚀 Getting Started

### Prerequisites
- Node.js v18+
- MongoDB (local or MongoDB Atlas)
- Anthropic API key

### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/krishi-samadhan.git
cd krishi-samadhan
```

### 2. Install dependencies
```bash
npm run install-all
```

### 3. Configure environment variables

```bash
cp server/.env.example server/.env
```

Edit `server/.env`:
```
MONGODB_URI=mongodb://localhost:27017/krishi-samadhan
ANTHROPIC_API_KEY=your_anthropic_api_key_here
JWT_SECRET=your_super_secret_jwt_key
PORT=5000
```

### 4. Run development servers
```bash
npm run dev
```

- Frontend: http://localhost:3000
- Backend API: http://localhost:5000

## 🌐 API Endpoints

| Method | Endpoint                    | Description                  |
|--------|-----------------------------|------------------------------|
| POST   | `/api/auth/register`        | Register new user            |
| POST   | `/api/auth/login`           | Login user                   |
| POST   | `/api/chat/message`         | Send message to AI           |
| GET    | `/api/chat/history/:userId` | Get conversation history     |
| DELETE | `/api/chat/history/:userId` | Clear conversation history   |

## 🌾 Supported Crops & Topics

- **Crops**: Wheat, Rice, Cotton, Sugarcane, Tomato, Potato, Onion, Pulses, Oilseeds
- **Topics**: Fertilizers, Pesticides, Irrigation, Soil Health, Market Prices, Government Schemes
- **Schemes**: PM-KISAN, PMFBY, Soil Health Card, e-NAM, MSP

## 📄 License

MIT License — free to use and modify.

---
Built with ❤️ for Indian Farmers | Powered by Anthropic Claude AI
