# 🚀 Node Server

A modern ***Express.js*** server implementation designed to manage tasks efficiently. This project demonstrates best practices in API development with containerized deployment and comprehensive Node.js tooling.

## 📁 Project Structure

```
node-server/
├── src/
│   ├── index.js          # Express application with route handlers
│   ├── routes/           # API route definitions
│   └── middleware/       # Custom middleware functions
├── package.json          # Project metadata and dependencies
├── package-lock.json     # Locked dependency versions
├── Dockerfile           # Container image configuration
└── docker-compose.yml   # Multi-container orchestration
```

### Key Components

**`node-server/src/index.js`**
- ***Core Express.js server*** implementation
- Handles task addition and retrieval operations
- RESTful API endpoint definitions and middleware setup

**`node-server/src/routes/`**
- Modular route handlers for tasks
- Clean separation of concerns
- Scalable endpoint management

**`node-server/src/middleware/`**
- Custom middleware for error handling
- Request validation and logging

**`node-server/package.json`**
- ***Project metadata and npm dependencies***
- Defines scripts for development and production
- Ensures consistent environment setup across installations

**`node-server/Dockerfile`**
- Builds optimized Docker image for the Express server
- Copies source code and installs Node dependencies via npm
- Configures container startup command

**`docker-compose.yml`**
- Orchestrates multi-container deployments
- Defines service configurations and inter-service dependencies

## 🚀 Getting Started

### Prerequisites
- ***Docker and Docker Compose*** installed
- ***Node.js 18+*** (for local development)
- Port 3000 available on your system

### Installation & Setup

Install dependencies locally:

```bash
cd node-server
npm install
```

### Running the Server

Execute the following command to build and start the application:

```bash
docker compose up
```

This command will:
1. Build the Express Docker image
2. Start all services defined in `docker-compose.yml`
3. Launch the server on `http://localhost:3000`

For local development without Docker:

```bash
npm run dev
```

---

## 🔌 API Routes

### Add a Task
**Endpoint:** `POST /tasks`
- **Purpose:** Creates and adds a new task to the task list
- **Request Body:** Task details in ***JSON format***
- **Response:** Confirmation of task creation with task ID

### Retrieve Tasks
**Endpoint:** `GET /tasks`
- **Purpose:** Fetches the complete task list
- **Response:** ***Array of all stored tasks***

### Update a Task
**Endpoint:** `PUT /tasks/:id`
- **Purpose:** Updates an existing task
- **Request Body:** Updated task details
- **Response:** Updated task object

### Delete a Task
**Endpoint:** `DELETE /tasks/:id`
- **Purpose:** Removes a task from the list
- **Response:** Confirmation of deletion

---

