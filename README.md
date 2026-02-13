# 🚀 Service Overview

This repository runs two services:

- ***Python FastAPI server*** in `python-server` on port **8000**
- ***Node/Express server*** in `my-express-app` on port **8001**

## 📁 Project Structure

```
python-server/
├── src/
│   ├── __init__.py       # Package marker
│   └── main.py           # FastAPI server implementation
├── requirements.txt      # Python dependencies
└── Dockerfile            # Container image configuration

my-express-app/
├── src/
│   └── app.js            # Express application with route handlers
├── package.json          # Project metadata and dependencies
├── nodemon.json          # Nodemon configuration
├── Dockerfile            # Container image configuration
└── docker-compose.yml    # Multi-container orchestration
```

### Key Components

**`python-server/src/main.py`**
- ***Core FastAPI server*** implementation
- Handles task addition and retrieval operations

**`my-express-app/src/app.js`**
- ***Core Express.js server*** implementation
- Mirrors the task addition and retrieval routes
- RESTful API endpoint definitions and middleware setup

**`my-express-app/package.json`**
- ***Project metadata and npm dependencies***
- Defines scripts for development and production
- Ensures consistent environment setup across installations

**`my-express-app/nodemon.json`**
- Watches the source directory for changes
- Restarts the server automatically during development

**`my-express-app/Dockerfile`**
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
- ***Python 3.9+*** (for local development)
- Ports 8000 and 8001 available on your system

### Installation & Setup

Install Node dependencies locally:

```bash
cd my-express-app
npm install

Install Python dependencies locally:

```bash
cd python-server
pip install -r requirements.txt
```
```

### Running the Servers

Execute the following command to build and start the application:

```bash
docker compose up
```

This command will:
1. Build the FastAPI and Express Docker images
2. Start all services defined in `docker-compose.yml`
3. Launch the servers on `http://localhost:8000` and `http://localhost:8001`

For local development without Docker:

```bash
cd my-express-app
npm start

In another terminal:

```bash
cd python-server
uvicorn src.main:app --reload --host 0.0.0.0 --port 8000
```
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

---

