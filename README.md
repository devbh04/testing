# Coding Practice Platform

This project is a comprehensive coding practice platform built with Next.js, Express.js, and MongoDB.  It provides a user interface for practicing coding problems, taking quizzes, and engaging in discussions.  The backend handles user authentication, data persistence, and interaction with a generative AI (Google Gemini).

## Description

This platform offers a wide range of coding challenges categorized by subject, including algorithms, machine learning, databases, and system design. Users can track their progress, submit solutions, and receive feedback.  A robust discussion forum allows users to collaborate and learn from each other.  Integration with Google Gemini allows for code evaluation and personalized learning recommendations.

## Features

* **Interactive Coding Challenges:**  A diverse library of coding problems categorized by subject area (AI, Web Development, Algorithms, etc.).
* **Multiple-Choice Quizzes:**  Assess your knowledge with quizzes covering various programming topics.
* **User Authentication and Profiles:** Secure user accounts with login, registration, and profile management.
* **Discussion Forum:**  Engage in discussions with other users, ask questions, and share knowledge.
* **Contest Participation:** Participate in coding contests with clear problem statements, test cases, and submission tracking.
* **Google Gemini Integration:**  Utilize Google Gemini's generative AI capabilities for code evaluation, debugging assistance, and personalized learning recommendations.
* **Persistent User Data:** User progress, submissions, and activity are persistently stored and managed.
* **Admin Panel (Future Development):**  (Planned) Functionality to manage contests, quizzes, and user accounts.

## Project Structure

The project is structured into a frontend (Next.js) and a backend (Express.js) component.

**Frontend (Next.js):**

* `app/`: Next.js app directory containing pages and components.
* `app/page.tsx`: Main application page.
* `styles/`: CSS and styling files.
* `components/`: Reusable UI components.
* `utils/`: Utility functions (e.g., `cn` for class name combination).
* `store/`: Zustand stores for application state management (`useUserStore`, `useInternshipStore`, `useStore`).

**Backend (Express.js):**

* `server.js`: Main Express.js server file.
* `config/`: Configuration files (e.g., `.env`).
* `models/`: Mongoose models (`User`, `Contest`, `DiscussionPost`, `Comment`).
* `routes/`: Express.js routers (`v1Router`, `authRouter`, `contestRouter`, `discussionRouter`, `geminiRouter`).
* `middleware/`: Custom middleware functions.


## How to Run

**1. Backend:**

* Clone the repository.
* Navigate to the backend directory.
* Create a `.env` file and configure environment variables (MongoDB URI, API keys, etc.).
* Install dependencies: `npm install`
* Start the server: `npm start`

**2. Frontend:**

* Navigate to the frontend directory.
* Install dependencies: `npm install`
* Start the development server: `npm run dev`


## Technologies Used

* **Frontend:** Next.js, React, Zustand, Tailwind CSS, clsx, tailwind-merge, next/font
* **Backend:** Express.js, Mongoose, MongoDB, bcrypt, jsonwebtoken, dotenv, @google/generative-ai, cors
* **AI:** Google Gemini


## API Documentation

### `/api/v1`:

This route acts as a base for all API endpoints.  Sub-routers manage different sections of the API.

* **`/auth`:**  Handles user authentication (login, registration).
* **`/contests`:** Manages programming contests (creation, retrieval, submission).
* **`/discussions`:**  Handles discussion posts and comments.
* **`/gemini`:**  Provides interfaces to Google Gemini's AI capabilities (code evaluation, chat, recommendations).
* **`/users`:**  Retrieves user data and activity.


Detailed documentation for each router is provided below:

**`authRouter`:**

* `/login`: Authenticates users and returns JWT.
* `/register`: Registers new users.
* `/contests`: Retrieves a user's submitted contests (requires authentication).
* `/discussions`: Retrieves a user's discussions and comments (requires authentication).

**`contestRouter`:**

* `POST /`: Creates a new contest.
* `GET /`: Retrieves all contests.
* `GET /:id`: Retrieves a single contest by ID.
* `POST /submit`: Submits a contest solution.

**`discussionRouter`:**

* `GET /`: Retrieves all discussion posts.
* `POST /`: Creates a new discussion post.
* `GET /:postId/comments`: Retrieves comments for a post.
* `POST /:postId/comments`: Adds a new comment to a post.
* `DELETE /:postId`: Deletes a discussion post.
* `DELETE /comments/:commentId`: Deletes a comment.

**`geminiRouter`:**

* `POST /evaluate`: Evaluates user code using Gemini.
* `POST /chat`: Interacts with Gemini through a chat interface.
* `POST /recommend`: Gets YouTube video recommendations from Gemini.

Further details on each API endpoint are available in the respective router files.


## Contributing

Contributions are welcome! Please open an issue or submit a pull request.


## License

[Specify your license here]
