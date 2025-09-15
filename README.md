# Todo Application

A simple todo application built with React frontend and Node.js backend.

## Project Structure

```
├── backend/                        # Node.js backend API
│   ├── server.js                   # Backend server
│   ├── package.json                # Backend dependencies
│   └── Dockerfile                  # Backend container
├── frontend/                       # React frontend application
│   ├── src/                        # Frontend source code
│   │   ├── App.js                  # Main todo app
│   │   └── index.js                # React entry point
│   ├── package.json                # Frontend dependencies
│   └── Dockerfile                  # Frontend container
├── k8s/                            # Kubernetes manifests
│   └── k8s-deployment.yaml         # Kubernetes deployment
├── ASSIGNMENT_INSTRUCTIONS.md      # Assignment instructions
└── README.md                       # This file
```

## Quick Start

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd devops-assignment
   ```

2. **Install dependencies**
   ```bash
   # Backend
   cd backend
   npm install
   
   # Frontend
   cd ../frontend
   npm install
   ```

3. **Run locally**
   ```bash
   # Backend (terminal 1)
   cd backend
   npm start
   
   # Frontend (terminal 2)
   cd frontend
   npm start
   ```

4. **Build Docker images**
   ```bash
   # Backend
   cd backend
   docker build -t todo-backend .
   
   # Frontend
   cd frontend
   docker build -t todo-frontend .
   ```

5. **Deploy to Kubernetes**
   ```bash
   kubectl apply -f k8s/k8s-deployment.yaml
   ```

## Application Features

- **Add todos**: Create new todo items
- **Mark complete**: Toggle todo completion status
- **Delete todos**: Remove todo items
- **Real-time updates**: Changes reflect immediately

## Technologies Used

- **Frontend**: React, Axios
- **Backend**: Node.js, Express
- **Containerization**: Docker
- **Orchestration**: Kubernetes

## Development

This is a simple todo application for learning purposes. The application uses in-memory storage for todos and provides a basic CRUD interface.

## License

MIT