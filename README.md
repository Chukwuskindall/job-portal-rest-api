Job Portal REST API - MERN
This project implements a RESTful API for a job portal using the MERN stack (MongoDB, Express, React, Node.js). The API allows for job posting, job searching, user authentication, and application management.

Table of Contents
Introduction
Features
Installation
Usage
API Endpoints
Project Structure
Introduction
The Job Portal REST API is designed to facilitate the management of job listings and applications. It includes functionalities for job seekers and employers, such as posting jobs, applying for jobs, and managing user profiles.

Features
User authentication (signup, login, logout)
Create, read, update, and delete job listings
Search for jobs
Apply for jobs
Manage user profiles
Installation
Clone the repository:
git clone https://github.com/Chukwuskindall/job-portal-rest-api-MERN.git
cd Job-Portal-RestApi-MERN
Install backend dependencies:
cd server
npm install
Install frontend dependencies:
cd ../client
npm install
Set up environment variables:
Create a .env file in the server directory and add your environment variables:

MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
Run the application:
Backend:
cd server
npm start
The backend server will start on http://localhost:5000.

Frontend:
cd ../client
npm start
The frontend will start on http://localhost:3000.

Usage
Open your web browser and navigate to http://localhost:3000.
Sign up or log in to your account.
Employers can post new job listings.
Job seekers can search for jobs and apply for them.
Manage job applications and user profiles through the respective interfaces.
API Endpoints
Auth
POST /api/auth/signup: Register a new user
POST /api/auth/login: Log in a user
POST /api/auth/logout: Log out a user
Jobs
GET /api/jobs: Retrieve all job listings
GET /api/jobs/:id: Retrieve a specific job listing
POST /api/jobs: Create a new job listing (authenticated users)
PUT /api/jobs/:id: Update a job listing (authenticated users)
DELETE /api/jobs/:id: Delete a job listing (authenticated users)
Users
GET /api/users/profile: Retrieve user profile (authenticated users)
PUT /api/users/profile: Update user profile (authenticated users)
Applications
POST /api/applications: Apply for a job (authenticated users)
GET /api/applications: Retrieve all applications (authenticated users)
Project Structure
Job-Portal-RestApi-MERN/
│
├── client/                  # Frontend code (React)
│   ├── public/              # Public files
│   ├── src/                 # Source files
│   │   ├── components/      # Reusable React components
│   │   ├── pages/           # React pages
│   │   ├── App.js           # Main React component
│   │   ├── index.js         # Entry point for React
│   └── package.json         # Frontend dependencies
│
├── server/                  # Backend code (Node.js, Express, MongoDB)
│   ├── controllers/         # Controller files for handling requests
│   ├── models/              # Database models
│   ├── routes/              # Route definitions
│   ├── middlewares/         # Middleware functions
│   ├── config/              # Configuration files
│   ├── .env                 # Environment variables
│   ├── server.js            # Main server file
│   └── package.json         # Backend dependencies
│
└── README.md                # Project README file
