# ParentPal – Parenting Assistant Web Application

ParentPal is a full-stack parenting assistant application that helps parents track their children's daily routines, milestones, events, and wellness metrics. It also includes an AI-powered chat assistant for parenting advice.

## Tech Stack

### Frontend
- **React 19** with functional components and hooks
- **Tailwind CSS** for styling
- **React Router v7** for navigation
- **Axios** for API calls
- **Vite** as build tool

### Backend
- **Node.js** with Express.js
- **MongoDB** with Mongoose ODM
- **JWT** for authentication
- **Vercel AI SDK** with OpenRouter for AI chat

## Features

- 🔐 **Authentication** - User registration, login, account management
- 👶 **Child Profiles** - Add, edit, delete children with health info
- 📅 **Events** - Create and manage upcoming/past events
- ✅ **Daily Routines** - Plan and track daily routines for each child
- 🏆 **Milestones** - Record and celebrate child milestones
- 💬 **AI Chat** - Get parenting advice from an AI assistant
- 📊 **Wellness Tracking** - Track mood, sleep, water intake, screen time
- ⚙️ **Settings** - Account deactivation and deletion

## Project Structure

```
parentpal/
├── src/                    # Frontend React application
│   ├── components/         # Reusable UI components
│   ├── pages/              # Page components
│   ├── services/           # API service functions
│   ├── context/            # React context (Auth)
│   └── layouts/            # Layout components
├── backend/                # Backend Node.js application
│   └── src/
│       ├── controllers/    # Route handlers
│       ├── models/         # MongoDB schemas
│       ├── routes/         # API routes
│       ├── middleware/     # Auth middleware
│       ├── config/         # Database config
│       └── utils/          # Utility functions
└── public/                 # Static assets
```

## Getting Started

### Prerequisites
- Node.js 20.19+ or 22.12+
- MongoDB (local or Atlas) - optional, app uses in-memory DB as fallback

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/parentpal.git
   cd parentpal
   ```

2. **Install frontend dependencies**
   ```bash
   npm install
   ```

3. **Install backend dependencies**
   ```bash
   cd backend
   npm install
   ```

4. **Set up environment variables**
   
   Create `backend/.env` file:
   ```env
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   OPEN_ROUTER_API_KEY=your_openrouter_api_key
   OPEN_ROUTER_AI_MODEL=your_preferred_model
   ```

5. **Run the application**

   Start backend (from `backend` folder):
   ```bash
   npm run dev
   ```

   Start frontend (from root folder):
   ```bash
   npm run dev
   ```

6. **Access the app**
   - Frontend: http://localhost:5173
   - Backend API: http://localhost:5000

## API Endpoints

### Authentication
- `POST /api/auth/signup` - Register new user
- `POST /api/auth/login` - Login user
- `GET /api/auth/me` - Get current user

### Children
- `GET /api/children` - List all children
- `POST /api/children` - Create child
- `GET /api/children/:id` - Get child
- `PUT /api/children/:id` - Update child
- `DELETE /api/children/:id` - Delete child

### Events
- `GET /api/events/upcoming` - Get upcoming events
- `GET /api/events/past` - Get past events
- `POST /api/events` - Create event
- `PUT /api/events/:id` - Update event
- `DELETE /api/events/:id` - Delete event

### Routines
- `GET /api/routines/child/:childId` - Get routines by child
- `POST /api/routines` - Create routine
- `PUT /api/routines/:id` - Update routine
- `DELETE /api/routines/:id` - Delete routine

### Milestones
- `GET /api/milestones/child/:childId` - Get milestones by child
- `POST /api/milestones` - Create milestone
- `PUT /api/milestones/:id` - Update milestone
- `DELETE /api/milestones/:id` - Delete milestone

### Chat
- `POST /api/chat` - Send message to AI assistant (streaming)

## Environment Variables

| Variable | Description |
|----------|-------------|
| `MONGO_URI` | MongoDB connection string |
| `JWT_SECRET` | Secret key for JWT tokens |
| `OPEN_ROUTER_API_KEY` | OpenRouter API key for AI chat |
| `OPEN_ROUTER_AI_MODEL` | AI model to use (e.g., `openai/gpt-3.5-turbo`) |

## License

This project is created for educational purposes as a final year college project.

## Authors

- Built with ❤️ using React and Node.js
