# Web Based Code Editor - editorY 🚀

<div align="center">

[![Next.js](https://img.shields.io/badge/Next.js-14-black?style=for-the-badge&logo=next.js)](https://nextjs.org/)
[![Express.js](https://img.shields.io/badge/Express.js-4.19-green?style=for-the-badge&logo=express)](https://expressjs.com/)
[![Socket.IO](https://img.shields.io/badge/Socket.IO-4.7-white?style=for-the-badge&logo=socket.io)](https://socket.io/)
[![Cloudflare](https://img.shields.io/badge/Cloudflare-Workers-orange?style=for-the-badge&logo=cloudflare)](https://workers.cloudflare.com/)
[![Docker](https://img.shields.io/badge/Docker-Enabled-blue?style=for-the-badge&logo=docker)](https://www.docker.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)

A modern, real-time collaborative code editor built for teams who want to code together, anywhere. 🌎


</div>

## ✨ Features

- 🤝 **Real-Time Collaboration**
  - Multiple developers can code simultaneously
  - See live cursor positions and selections
  - Built with Liveblocks and Y.js for seamless synchronization

- 🤖 **AI-Powered Code Assistance**
  - Intelligent code suggestions
  - Code generation with simple prompts
  - Context-aware code completion

- 📂 **Advanced Project Management**
  - Intuitive file tree navigation
  - Drag-and-drop file organization
  - Multiple project templates (React, Node.js)

- 🖥️ **Integrated Development Environment**
  - Monaco Editor integration
  - Multiple terminal support
  - Live preview of changes
  - Customizable themes and settings

- 🔍 **Smart Features**
  - Global search across projects
  - File content search
  - Quick navigation shortcuts

- 🔒 **Security & Authentication**
  - Clerk-based authentication
  - Role-based access control
  - Secure data transmission

## 🏗️ Architecture

```mermaid
graph TD
    A[Client - Next.js] --> B[API Server - Express.js]
    B --> C[Database Worker]
    B --> D[Storage Worker]
    C --> E[SQLite Database]
    D --> F[Static Assets]
    A -->|WebSocket| B
    B -->|Real-time Events| A
    
```

## 🚀 Tech Stack

### Frontend
- **Next.js 14**
- **React 18**
- **Monaco Editor**
- **Liveblocks**
- **TailwindCSS**
- **Socket.IO Client**

### Backend
- **Express.js**
- **Socket.IO**
- **Node-PTY**
- **Cloudflare Workers**
- **Docker**

### Database & Storage
- **SQLite with Drizzle ORM**
- **Cloudflare Workers**
- **AWS ECS Integration**



## 🏃 Getting Started

### Prerequisites
Make sure you have the following installed:
- **Node.js ≥ 18**
- **Docker**
- **Git**

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/KoldAd1b/editorY
   cd editorY
   ```
   
2.  **Install dependencies**
    
    ```bash
    
	 # Install root dependencies
    npm install
    
    # Install client dependencies
    cd client && npm install
    
    # Install server dependencies
    cd ../server/server && npm install
    cd ../database && npm install
    cd ../storage && npm install` 


3.  **Set up environment variables**

  
    ``` bash
    
    `# Copy environment files
    cp .env.example .env
    cd client && cp .env.example .env
    cd ../server/server && cp .env.example .env
    cd ../database && cp .env.example .env
    cd ../storage && cp .env.example .env` 
    ```

### Start the Development Environment

#### Using Docker (recommended)

```bash
`docker-compose up` 
```

#### Or start services individually

Open separate terminals and run the following commands:

1.  **Terminal 1 - Client**
    ```bash 
    cd client && npm run dev
    ```
2.  **Terminal 2 - Main Server**
       
    ```bash 
    cd server/server && npm run dev
    ```
    
    
3.  **Terminal 3 - Database Service**
    
    ```bash 
    cd server/database && npm run dev
    ```
       
4.  **Terminal 4 - Storage Service**   

    ```bash 
    cd server/database && npm run dev
    ```
   
## 🌟 Key Features in Detail

### Real-Time Collaboration

-   Utilizes **Liveblocks** and **Y.js** for conflict-free real-time editing.
-   Supports multiple cursors and selections.
-   Real-time chat and presence indicators.

### Project Management

-   Create and manage multiple projects.
-   Organize files and folders with drag-and-drop.
-   Template-based project creation.

### Development Environment

-   Integrated terminal with full **PTY** support.
-   Multi-window support.
-   Live preview capabilities.
-   Custom theme support.

## 🔧 Architecture Details

### Microservices Architecture

-   **Client Service**: Next.js application handling UI/UX.
-   **API Server**: Express.js managing HTTP requests and WebSocket connections.
-   **Database Worker**: Cloudflare Worker handling database operations.
-   **Storage Worker**: Cloudflare Worker managing static assets and file storage.

### Real-Time Communication

-   **WebSocket** connections for real-time updates.
-   **Y.js** for conflict-free collaborative editing.
-   **Socket.IO** for bi-directional communication.

## 📫 Contact

Ahnaf Adib - [@KoldAd1b](https://github.com/KoldAd1b)
Email - [Gmail](https://mailto:ahnafadib7546@gmail.com)

Project Link: [https://github.com/KoldAd1b/editorY](https://github.com/KoldAd1b/editorY)

