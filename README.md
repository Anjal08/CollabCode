# CollabCode 🚀
> AI-powered collaborative browser-based IDE with real-time collaboration,
> an autonomous AI pair programmer, and in-browser code execution.

[🌐 Live Demo](https://collab-code-jdojvutft-anjal08s-projects.vercel.app/) •
[💻 GitHub](https://github.com/Anjal08/CollabCode)

---
## 📸 Project Preview

### Landing Page

![CollabCode Landing Page](./Screenshots/landing-page.png)

### Project Dashboard

![CollabCode Dashboard](./Screenshots/dashboard.png)

### Collaborative IDE

![CollabCode IDE](./Screenshots/ai-code-editor.png)

### Real-Time Collaboration

![CollabCode Collaboration](./Screenshots/collaboration.png)

# 💡 What I Built

CollabCode was designed to bring the core tools developers use during
collaborative development into one browser-based environment.

The project combines real-time communication, AI-assisted development,
browser-based code execution, terminal access, and workspace management
into a single platform.

## 💡 Why CollabCode?

CollabCode brings collaborative development, AI-assisted coding,
and browser-based execution into a single development environment.

Instead of switching between an IDE, terminal, AI assistant, and
collaboration tools, developers can work within one browser-based workspace.

## ✨ Core Features

- 👥 **Real-Time Collaboration**
  Multiple developers can work in the same workspace using Socket.io.

- 🤖 **AI Pair Programmer**
  Groq/Llama 3 understands project context and can generate,
  modify, and manage code.

- 🌐 **In-Browser Code Execution**
  WebContainers provide a browser-based Node.js runtime.

- 💻 **Interactive Terminal**
  Execute commands and view real-time process output.

- 🗂️ **Integrated IDE**
  File explorer, code editor, terminal, AI assistant, and preview
  are combined into one workspace.

- 🔐 **Secure Authentication**
  JWT-based authentication with project and workspace management.

## 🏗️ Architecture

```text
                    ┌──────────────────────┐
                    │      React Client    │
                    │   Collaborative IDE  │
                    └──────────┬───────────┘
                               │
              ┌────────────────┼────────────────┐
              │                │                │
              ▼                ▼                ▼
        Socket.io          REST APIs       WebContainers
        Real-time          Node/Express     Browser Runtime
        Collaboration          │
                               ▼
                         ┌─────────────┐
                         │  MongoDB    │
                         └─────────────┘
                               │
                               ▼
                         ┌─────────────┐
                         │ Groq /      │
                         │ Llama 3     │
                         └─────────────┘
```

## 🛠️ Technology Stack

| Layer | Technologies |
|---|---|
| Frontend | React, Vite, Tailwind CSS |
| Real-Time | Socket.io |
| Backend | Node.js, Express.js |
| Database | MongoDB, Mongoose |
| AI | Groq SDK, Llama 3 |
| Runtime | WebContainers |
| Terminal | xterm.js |
| Authentication | JWT, bcrypt |

## 🚀 Getting Started

**Prerequisites:** Node.js (v18+)

```bash
# 1. Clone the repository
git clone https://github.com/Anjal08/CollabCode.git
cd CollabCode

# 2. Install dependencies for both frontend and backend
cd backend && npm install
cd ../frontend && npm install

# 3. Create .env files (see Environment Variables section below)

# 4. Start the development servers
# Open two terminals:
# Terminal 1:
cd backend && npm start
# Terminal 2:
cd frontend && npm run dev
```

## 💡 Usage Guide

1. **Create a Workspace**: Sign in and create a new project.
2. **Invite the Team**: Add other registered developers as collaborators to your project.
3. **Summon the AI**: Open the chat panel and type `@ai create an express server on port 3000`. Watch as the file tree automatically populates!
4. **Run Code**: Open the Terminal tab, type `npm install` and then `node index.js`. Your code is now running in the browser sandbox.

## ⚙️ Environment Variables

Create `.env` files in both the frontend and backend directories based on these templates:

### Backend (`/backend/.env`)
```env
PORT=3000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_super_secret_jwt_key
GROQ_API_KEY=your_groq_api_key_for_ai
```

### Frontend (`/frontend/.env`)
```env
VITE_API_URL=http://localhost:3000
```

## 📄 License
This project is licensed under the MIT License.
