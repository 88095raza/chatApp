
# Project Title
Tlker a Real-Time Chat Application

A full-stack real-time chat application with user authentication, private and group messaging, and live updates using Socket.IO. Built using the MERN stack with Chakra UI for styling.
# 📁 Folder Structure
chatApp/

├── backend/ # Express server, API routes, MongoDB models
├── frontend/ # React app with Chakra UI  
  ├── .env # Environment variables   
└── README.md

## 🚀 Setup Instructions
### 1. Clone the repository

```bash
git clone https://github.com/your-username/chatApp.git
cd chatApp




## Installation
#Install Backend Dependencies

cd backend
npm install

# Install Frontend Dependencies
cd frontend
npm install

    
## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

PORT=5000
MONGO_URI=<your-mongodb-uri>
JWT_SECRET=<your-jwt-secret>
NODE_ENV=development

#Start Development Servers
# In one terminal
cd backend
npm run server

# In another terminal
cd frontend
npm start


🧱 Architecture Overview
Client (React + Chakra UI)

UI components for registration, login, chat list, messages.

Axios for HTTP requests.

Socket.IO-client for real-time communication.

Server (Express + MongoDB)

REST APIs for user, chat, and message management.

JWT for authentication.

Socket.IO for real-time events like typing and new messages.

Database (MongoDB Atlas)

Stores users, chats, and messages.


🛠️ Technologies Used
Frontend
React

Chakra UI

Axios

React Router

Socket.IO Client

Backend
Node.js

Express.js

MongoDB + Mongoose

JSON Web Tokens (JWT)

Socket.IO Server

Deployment
Render (Backend)

Netlify or Vercel (Frontend)

MongoDB Atlas (Database)

⚔️ Challenges Faced & Solutions
1. MongoDB Atlas IP Whitelist Issue
Problem: Connection refused due to IP not being whitelisted.

Solution: Added 0.0.0.0/0 in Atlas Network Access during development.

2. Socket.IO Not Receiving Messages
Problem: Event not reaching all connected users.

Solution: Ensured .join(room) was done correctly and socket.in(user._id).emit(...) used properly.

3. React and Package Version Conflicts
Problem: npm install errors due to mismatched React peer dependencies.

Solution: Used --legacy-peer-deps to force install. Upgraded conflicting packages where possible.

4. Submodule Issue in Git
Problem: Accidentally committed client/ as a git submodule.

Solution: Removed .gitmodules, .git/config entries, and re-added client/ as a normal directory.

Deployment link :https://talker-wo0x.onrender.com 
