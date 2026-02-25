# RedditPylon Backend

A robust backend service for the RedditPylon project, built with Node.js, Express, and TypeScript.

## 🚀 Technologies Used

* **Node.js & Express**: Core framework for building the REST API
* **TypeScript**: For static typing and enhanced developer experience
* **Redis (`ioredis`)**: In-memory data store for caching and pub/sub capabilities
* **Zod**: Schema declaration and validation library
* **Authentication**: `jsonwebtoken` (JWT) & `bcryptjs`
* **Middleware**: `cors`, `cookie-parser`, `dotenv`

## 📦 Prerequisites

Before you begin, ensure you have the following installed:
* [Node.js](https://nodejs.org/) (v16 or higher recommended)
* [Redis](https://redis.io/) (running locally or a remote instance)

## 🛠️ Installation & Setup

1. **Clone the repository** (if you haven't already):
   ```bash
   git clone <repository-url>
   cd redditPylon-backend
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Environment Configuration**:
   Create a `.env` file in the root directory and add the necessary environment variables. 
   ```env
   PORT=5000
   REDIS_URL=redis://localhost:6379
   JWT_SECRET=your_super_secret_jwt_key
   # Add any other required environment variables here
   ```

4. **Start the Development Server**:
   ```bash
   npm run dev
   ```
   *(Ensure you have a `dev` script using `ts-node-dev` or similar in your `package.json`!)*

## 📁 Project Structure

```text
src/
├── controllers/   # Route handler logic
├── routes/        # Express API route definitions
├── services/      # Core business logic and database/Redis interactions
├── utils/         # Helper functions
├── constant.ts    # Application-wide constants
└── index.ts       # Application entry point
```

## 🔐 Authentication Flow
This project uses standard JWT-based authentication. Passwords are securely hashed using `bcryptjs`. `cookie-parser` is available for handling HTTP-only cookies if needed for session or token management.

## ✔️ Validation
Input data validation is handled robustly throughout the application using **Zod**.

## 📝 Scripts

* `npm run test` - Run test suites (to be configured).

## 📄 License
ISC
