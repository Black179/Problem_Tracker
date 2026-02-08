# MongoDB Setup Instructions

## Option 1: MongoDB Atlas (Recommended - Free Cloud Database)

1. Go to https://www.mongodb.com/atlas/database
2. Sign up for a free account
3. Create a new cluster (free tier)
4. Create a database user with username and password
5. Get your connection string from Atlas dashboard
6. Replace the connection string in your .env file

Example .env file:
```
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/problem-tracker?retryWrites=true&w=majority
PORT=8080
JWT_SECRET=your-super-secret-key-change-this-in-production
```

## Option 2: Install MongoDB Locally

1. Download MongoDB Community Server from https://www.mongodb.com/try/download/community
2. Install MongoDB on Windows
3. Start MongoDB service
4. Use local connection string: mongodb://localhost:27017/problem-tracker

## Option 3: Use Docker (if you have Docker installed)

```bash
docker run -d -p 27017:27017 --name mongodb mongo:latest
```

Then use: mongodb://localhost:27017/problem-tracker

## Current Status

The server is configured to use MongoDB but needs a valid MONGODB_URI.
Please set up one of the options above and create a .env file in the backend directory.
