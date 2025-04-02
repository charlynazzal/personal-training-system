# Smart Programming System for Personal Trainers

An AI-powered workout program generation system that helps personal trainers create customized workouts for their clients.

## Features

- **Client Management**: Store and manage detailed client profiles
- **Exercise Library**: Comprehensive database of exercises with details and instructions
- **Program Creation**: Create custom workout programs from scratch or templates
- **AI-Powered Generation**: Generate personalized workout programs using Claude AI
- **Progress Tracking**: Track client progress and workout compliance

## Tech Stack

- **Frontend**: React with Tailwind CSS
- **Backend**: Node.js with Express
- **Database**: MongoDB
- **Authentication**: JWT-based auth
- **AI**: Claude API integration

## Directory Structure

```
personal-training-system/
├── client/                  # React frontend
│   ├── public/              # Static files
│   └── src/                 # React source code
│       ├── assets/          # Images, fonts, etc.
│       ├── components/      # Reusable UI components
│       ├── context/         # React context providers
│       ├── hooks/           # Custom React hooks
│       ├── layouts/         # Layout components
│       ├── pages/           # Page components
│       ├── services/        # API services
│       └── utils/           # Utility functions
├── server/                  # Node.js/Express backend
│   ├── config/              # Configuration files
│   ├── controllers/         # API controllers
│   ├── middleware/          # Express middleware
│   ├── models/              # MongoDB models
│   ├── routes/              # API routes
│   ├── services/            # Business logic services
│   │   └── claude/          # Claude AI integration
│   └── utils/               # Utility functions
```

## Getting Started

### Prerequisites

- Node.js (v14+)
- MongoDB

### Installation

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/personal-training-system.git
   cd personal-training-system
   ```

2. Install backend dependencies:
   ```
   cd server
   npm install
   ```

3. Install frontend dependencies:
   ```
   cd ../client
   npm install
   ```

4. Create a `.env` file in the server directory with your environment variables:
   ```
   NODE_ENV=development
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/personal-training-system
   JWT_SECRET=your_jwt_secret_key_here
   JWT_EXPIRES_IN=90d
   CLAUDE_API_KEY=your_anthropic_api_key_here
   ```

5. Start the development servers:
   ```
   # In the server directory
   npm run dev
   
   # In the client directory (in a separate terminal)
   npm start
   ```

6. The frontend will be available at http://localhost:3000 and the backend at http://localhost:5000

## API Endpoints

- **Authentication**
  - `POST /api/users/signup` - Register a new user
  - `POST /api/users/login` - Login user
  
- **Clients**
  - `GET /api/clients` - Get all clients
  - `POST /api/clients` - Create a new client
  - `GET /api/clients/:id` - Get a specific client
  - `PATCH /api/clients/:id` - Update a client
  - `DELETE /api/clients/:id` - Delete a client
  
- **Programs**
  - `GET /api/programs` - Get all programs
  - `POST /api/programs` - Create a new program
  - `GET /api/programs/:id` - Get a specific program
  - `PATCH /api/programs/:id` - Update a program
  - `DELETE /api/programs/:id` - Delete a program
  - `POST /api/programs/generate` - Generate a program using AI
  
- **Exercises**
  - `GET /api/exercises` - Get all exercises
  - `POST /api/exercises` - Create a new exercise
  - `GET /api/exercises/:id` - Get a specific exercise
  - `PATCH /api/exercises/:id` - Update an exercise
  - `DELETE /api/exercises/:id` - Delete an exercise 
