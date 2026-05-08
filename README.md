# Simple App

A simple Node.js + Express application with Docker and GitHub Actions CI/CD.

## Local Development

### Setup

```bash
npm install
npm start
```

The app will run on `http://localhost:3000`

## API Endpoints

- `GET /` - Returns welcome message
- `GET /health` - Health check endpoint
- `GET /api/users` - Get all users
- `POST /api/users` - Create new user

## Docker

```bash
docker build -t simple-app:latest .
docker run -p 3000:3000 simple-app:latest
```

## GitHub Actions CI/CD

1. Push code to main branch
2. Workflow builds and tests Docker image
3. Creates approval issue
4. Comment `/approve` to deploy
5. Image pushed to Docker Hub and GitHub Container Registry

# Fix permissions
