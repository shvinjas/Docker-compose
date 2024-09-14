# Docker Compose Project - API & Blog
This project sets up two services:

API (running on port 4000)
Blog (running on port 3000)
The Blog fetches data from the API running on localhost:4000.

### Prerequisites
Ensure you have the following installed:

Docker
Docker Compose

### Directory Structure
.
├── api
│   ├── Dockerfile
│   ├── package.json
│   └── app.js
└── myblog
    ├── Dockerfile
    ├── package.json
    └── index.js
├── docker-compose.yml
└── README.md

### API
The API service is a Node.js application that provides data for the blog. It runs on localhost:4000.

### Dockerfile:
Builds a Node.js app.
Installs dependencies using npm install.
Starts the API server using npm start.

### Blog
The Blog service is another Node.js application that fetches data from the API running on localhost:4000.

### Dockerfile:
Builds a Node.js app.
Installs dependencies using npm install.
Starts the blog app on localhost:3000.

### Docker Compose Setup
docker-compose.yml
This file defines the two services: api and myblog. The API runs on port 4000, and the Blog runs on port 3000. The Blog fetches data from the API through http://localhost:4000.
