# README.md

## Description

This project is a full-stack application built with Next.js (frontend), Express.js (backend), and MongoDB (database).  It provides a platform for users to participate in programming contests, engage in discussions, and receive AI-powered assistance through Google Gemini's generative AI capabilities.  The frontend utilizes Tailwind CSS for styling and Zustand for state management. The backend uses Mongoose for database interactions and JWT for authentication.

## Features

**Frontend:**

* **Interactive Quiz:**  A multiple-choice quiz covering various programming subjects (AI, Web Development, Data Structures, Algorithms).
* **User Authentication:** Secure user login and registration.
* **Responsive Design:**  Optimized for various screen sizes.
* **Optimized Font Loading:** Uses `next/font` for efficient loading of the Geist font family.
* **Clean UI:** Uses Tailwind CSS for styling.

**Backend:**

* **RESTful API:**  Provides a robust API for interacting with contests, discussions, users, and the Gemini AI.
* **User Management:**  Handles user registration, login, and data persistence.
* **Contest Management:**  Allows creation, retrieval, and submission of solutions for programming contests.
* **Discussion Forum:**  Enables users to create and participate in discussions.
* **Google Gemini Integration:**  Leverages Gemini's capabilities for code evaluation, conversational coding assistance, and learning resource recommendation.
* **MongoDB Database:**  Stores user data, contest information, and discussion posts.
* **Robust Error Handling:**  Provides informative error messages for both client and server-side errors.
* **Authentication:** Secure authentication using JWT.
* **Data Validation:**  Input validation to prevent database errors.

## Project Structure

```
├── app/
│   ├── page.tsx
│   └── ...
├── public/
│   └── ...
├── next.config.js
├── package.json
├── server/
│   ├── index.js
│   ├── config.js
│   ├── models/
│   │   ├── User.js
│   │   ├── Contest.js
│   │   ├── DiscussionPost.js
│   │   └── Comment.js
│   ├── routes/
│   │   ├── v1/
│   │   │   └── v1Router.js
│   │   ├── authRouter.js
│   │   ├── contestRouter.js
│   │   ├── discussionRouter.js
│   │   └── geminiRouter.js
│   └── ...
└── ...
```

**Frontend (app/):** Contains Next.js pages and components.  `app/page.tsx` is the main page.

**Backend (server/):** Contains the Express.js server, database models, and API routes.  The `/v1` route is a versioned API.  Sub-routers handle specific functionality (authentication, contests, discussions, Gemini integration).

**Models (server/models/):**  Mongoose schemas for `User`, `Contest`, `DiscussionPost`, and `Comment`.

**Routes (server/routes/):**  Express routers organizing API endpoints.


## How to Run

**1. Frontend:**

* Clone the repository.
* Navigate to the project directory.
* Run `npm install` or `yarn install` or `pnpm install` or `bun install` to install dependencies.
* Run `npm run dev` or `yarn dev` or `pnpm dev` or `bun dev` to start the development server.  The application will be accessible at `http://localhost:3000`.

**2. Backend:**

* Ensure you have Node.js and MongoDB installed.
* Create a `.env` file in the `server` directory with the necessary environment variables (database connection string, API keys, etc.).  See `server/config.js` for details.
* Navigate to the `server` directory.
* Run `npm install` or `yarn install` or `pnpm install` or `bun install` to install backend dependencies.
* Run `node index.js` to start the server (default port 5000).

**Deployment:**  The application is designed for easy deployment to Vercel.


## Modules

### Next.js Configuration (`next.config.js`)

Exports a Next.js configuration object conforming to the `NextConfig` type.

### Configuration (`server/config.js`)

Defines the `BASE_URL` for the application, allowing for switching between production and development environments.  Defaults to `"https://ind1-backend-vercel.vercel.app"`.

### Coding Problems (`CodePS` -  Data Structure)

Exports a JavaScript object containing practice coding problems categorized by subject area.

### Quiz Data (Multiple Modules)

Exports JavaScript arrays containing multiple-choice quiz questions categorized by subject (AI, Web Development, Data Structures, Algorithms, Machine Learning, Database, System Design).

### `cn` Function (Utility)

Combines class names using `clsx` and `tailwind-merge` for efficient and type-safe class name generation in Tailwind CSS projects.

### `useUserStore` (Zustand Store)

A Zustand store managing user data, persisted using `zustand/middleware` in localStorage.

### `useInternshipStore` (Zustand Store)

A Zustand store managing internship data.  (Note:  This seems out of place given the overall project description.  Consider removing or clarifying its purpose within this application.)

### Express.js Server (`server/index.js`)

A Node.js application using Express.js to create a RESTful API, connecting to a MongoDB database.

### `v1Router` (`server/routes/v1/v1Router.js`)

An Express.js router aggregating routes for various application features (discussions, contests, Gemini, authentication, users) under the `/api/v1` path.

### Gemini Router API (`server/routes/geminiRouter.js`)

An Express.js router providing endpoints for interacting with Google Gemini's generative AI capabilities (`/evaluate`, `/chat`, `/recommend`).

### Authentication Router (`server/routes/authRouter.js`)

Handles user authentication and retrieval of user-specific data using bcrypt, JWT, and Mongoose models.

### User Model (`server/models/User.js`)

A Mongoose schema defining the `User` model with fields for user information, contest submissions, discussions, and comments.

### Discussion and Comment Models (`server/models/DiscussionPost.js`, `server/models/Comment.js`)

Mongoose models defining the schema for `DiscussionPost` and `Comment`, establishing a one-to-many relationship.

### Contest Model (`server/models/Contest.js`)

A Mongoose model for storing contest data.

### User Activity Route (`server/routes/userRouter.get('/:userId/activity')`)

Retrieves all activity for a given user ID, including contests, discussions, and comments.

### Contest Router (`server/routes/contestRouter.js`)

An Express.js router handling API requests related to programming contests (creation, retrieval, submission).

### Discussion Router (`server/routes/discussionRouter.js`)

An Express.js router for managing discussion posts and comments.
