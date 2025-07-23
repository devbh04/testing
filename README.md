
# CodeVibe: A Code Editing and Learning Environment

## 1. Project Title & Description

CodeVibe is a Next.js application designed to provide a comprehensive code editing and learning environment. It empowers users to practice coding, learn new concepts, and collaborate with others. The application features a code editor, user authentication, progress tracking, and interactive learning tools.

## 2. Features

*   **Code Editor:** A Monaco Editor-powered code editor with language selection, font size adjustment, code execution, and submission capabilities.
*   **User Authentication:** Secure user registration, login, and logout functionality, ensuring personalized progress tracking and access control.
*   **Progress Tracking:** User dashboards displaying activity, contests, discussions, and comments, allowing users to monitor their learning journey.
*   **AI Coding Assistant:** Integration with an AI bot for coding assistance, providing hints, test cases, and explanations to aid users in problem-solving.
*   **Content Recommendations:**  Suggests video tutorials based on user-selected understanding level and search terms, facilitating targeted learning.
*   **Discussion Forum:** Enables users to create and participate in discussions, fostering a collaborative learning environment.
*   **Contest Platform:** A platform for participating in coding contests, providing a competitive and engaging learning experience.
*   **Test Case Management:** Displays test cases, their results (pass/fail), and input/output details, allowing users to debug their code effectively.
*   **Responsive UI:** A user-friendly interface built with Radix UI for accessible components and Tailwind CSS for styling, ensuring a consistent experience across devices.
*   **Animated Background:** Dynamically animated backgrounds using `framer-motion` add visual appeal.

## 3. Architecture & Structure

The CodeVibe application follows a modular architecture, leveraging Next.js's features and industry-standard libraries.

*   **Framework:** Next.js - Provides server-side rendering, routing, and API endpoints.
*   **UI Library:** React - For building reusable UI components.
*   **Styling:** Tailwind CSS - A utility-first CSS framework for rapid and consistent styling.
*   **UI Components:** Radix UI - A set of unstyled, accessible React components. Shadcn UI is used with the "new-york" theme, further enhancing the visual appeal.
*   **State Management:** Zustand - For managing application state, particularly user authentication, test cases, and code editor state.
*   **Code Editor:** Monaco Editor - A powerful and versatile code editor component.
*   **Animation:** framer-motion - Used for adding animations and transitions to the UI.
*   **Image Processing:** sharp - For efficient image processing.
*   **Data Fetching:**  The application interacts with a backend API (deployed on Render) for data fetching and submission, including comments, discussions, user activity, coding problems, and chat interactions. API calls leverage asynchronous data fetching with loading and error state handling.
*   **Authentication:** Uses `localStorage` for storing authentication tokens.
*   **Directory Structure:**
    *   `components/`: Contains reusable UI components.
    *   `pages/`: Defines the application's routes and page layouts.
    *   `styles/`: Contains global styles and Tailwind CSS configurations.
    *   `utils/`: Contains utility functions, such as CSS class name merging.
    *   `store/`: Contains Zustand stores for managing application state (e.g., user authentication, code editor state, test cases).
    *   `ui/`: Contains styled components, often wrappers around Radix UI primitives.

## 4. Installation & Setup

1.  **Clone the repository:**

    ```bash
    git clone <repository_url>
    cd codevibe
    ```

2.  **Install dependencies:**

    ```bash
    npm install  # or yarn install or pnpm install
    ```

3.  **Configure environment variables:**

    *   Create a `.env.local` file in the project root.
    *   Add the necessary environment variables (see Configuration section below).

4.  **Run the development server:**

    ```bash
    npm run dev  # or yarn dev or pnpm dev
    ```

    This will start the Next.js development server, typically at `http://localhost:3000`.

## 5. Usage

1.  **Access the application:** Open your browser and navigate to the development server address (e.g., `http://localhost:3000`).

2.  **Login/Register:**  Use the login/registration form on the homepage to create an account or log in.

3.  **Code Editor:**  Navigate to the code editor page (requires authentication).  Select a language, write your code, and execute it.

4.  **Explore Features:**  Explore the discussion forum, content recommendations, and user dashboard to utilize the application's learning resources.

## 6. API/Endpoints

The application interacts with a backend API deployed on Render. The base URL is defined in `url.js`:

```javascript
// url.js
export const BASE_URL = "https://your-backend-api.onrender.com"; // Replace with your actual backend URL
```

Key API endpoints include:

*   **Authentication:** `/api/auth/register`, `/api/auth/login`, `/api/auth/logout`
*   **Discussions:** `/api/discussions`, `/api/discussions/:id/comments`
*   **Contests:** `/api/contests`
*   **User Profile:** `/api/users/:id`
*   **AI Chat:** `/api/chat`
*   **Content Recommendations:** `/api/recommendations`

## 7. Configuration

The application uses environment variables for configuration. Create a `.env.local` file in the project root and define the following variables:

*   `NEXT_PUBLIC_BACKEND_URL`: The URL of the backend API (e.g., `https://your-backend-api.onrender.com`).
*   `NEXT_PUBLIC_API_KEY`: API Key for accessing the backend API
*   `DATABASE_URL`: (If applicable) The URL of your database.
*   `NEXTAUTH_SECRET`: (If applicable) Secret for NextAuth.js authentication.
*   Any other environment variables required by your backend API.

## 8. Contributing

We welcome contributions to CodeVibe! To contribute:

1.  Fork the repository.

2.  Create a new branch for your feature or bug fix:

    ```bash
    git checkout -b feature/your-feature-name
    ```

3.  Make your changes and commit them with descriptive commit messages.

4.  Push your changes to your forked repository.

5.  Submit a pull request to the main repository.

Please follow these guidelines:

*   Write clear and concise code.
*   Add comments to explain complex logic.
*   Write unit tests for your changes.
*   Follow the project's coding style.
*   Ensure your changes do not break existing functionality.

We appreciate your contributions!
