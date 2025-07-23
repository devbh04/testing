# CodeVibe - Leetcode Killer

## Description

CodeVibe is a web application designed to help users improve their coding skills through a variety of features, including coding challenges, discussion forums, personalized recommendations, and progress tracking. Built with Next.js, React, Tailwind CSS, and various UI libraries, CodeVibe aims to provide a comprehensive and engaging platform for coders of all levels.

## Key Features

*   **Next.js App Router:** Utilizes the latest Next.js App Router (`app/` directory) for efficient routing and server-side rendering.
*   **Automatic Code Updates:** Offers a smooth development experience with automatic code updates on file modification.
*   **Font Optimization:** Employs `next/font` for optimized font loading, including the Geist font.
*   **User Authentication:** Implements user registration and login functionality with secure API interactions.
*   **Coding Challenges:** Provides a code editor environment with support for multiple programming languages, test cases, and submission validation.
*   **AI-Powered Assistance:** Integrates with an AI bot to provide code explanations, recommendations, and chat-based assistance.
*   **Discussion Forums:** Enables users to engage in discussions, share knowledge, and ask questions.
*   **Personalized Recommendations:** Offers tailored content recommendations based on user understanding and preferences.
*   **Progress Tracking:** Tracks user progress, including solved problems, success rate, and global ranking.
*   **Dashboard:** Displays user activity, including contests, discussions, and comments.
*   **Modern UI:** Leverages Tailwind CSS and Radix UI for a responsive and accessible user interface.
*   **Animated Backgrounds:** Features visually appealing animated backgrounds using SVG and `framer-motion`.

## Project Structure

The project is organized into the following key directories and files:

*   **`app/`:**  The main application directory, utilizing the Next.js App Router.
    *   `app/page.tsx`: The main landing page component.
    *   `app/(root)/code-editor/[id]/page.tsx`: The code editor page, protected behind authentication.
    *   `app/discussion/page.tsx`: The discussion forum page.
    *   `app/dashboard/page.tsx`: The user dashboard page.
    *   `app/progress/page.tsx`: The user progress page.
    *   `app/api/v1/...`: API routes for backend functionality (authentication, data fetching, AI integration, etc.).
*   **`components/`:** Reusable React components.
    *   `components/ui/`: Styled UI components built on top of Radix UI.
        *   `components/ui/button.tsx`: Styled button component.
        *   `components/ui/dialog.tsx`: Styled dialog component.
        *   `components/ui/input.tsx`: Styled input component.
        *   `components/ui/label.tsx`: Styled label component.
        *   `components/ui/popover.tsx`: Styled popover component.
        *   `components/ui/textarea.tsx`: Styled textarea component.
        *   `components/ui/calendar.tsx`: Styled calendar component.
        *   `components/ui/command.tsx`: Styled command palette components.
    *   `components/shared/`: Shared components used across multiple pages.
        *   `components/shared/LeftDiv.tsx`: Displays challenge information.
        *   `components/shared/MiddleTopDiv.tsx`: Code editor interface.
        *   `components/shared/MiddleBottomDiv.tsx`: Test case display.
        *   `components/shared/RightDiv.tsx`: AI chat interface.
    *   `components/AppBar.js`: The application's navigation bar.
    *   `components/BackgroundLines.tsx`: Animated SVG background.
    *   `components/BoxesCore.tsx`: Animated grid of boxes.
    *   `components/DiscussionCard.tsx`: Displays a discussion post.
    *   `components/Footer.tsx`: The application's footer.
    *   `components/InfoCard.tsx`: Displays information cards.
    *   `components/ThreeDMarquee.tsx`: Animated 3D marquee of images.
*   **`lib/`:** Utility functions and constants.
    *   `lib/utils.ts`: Utility functions, including `cn` for class name merging.
    *   `lib/url.js`: Defines the base URL for API requests.
*   **`store/`:** Zustand stores for managing application state.
    *   `store/userStore.js`: Manages user authentication state.
    *   `store/codeEditorStore.js`: Manages code editor state.
    *   `store/testCasesStore.js`: Manages test case data.
*   **`next.config.js`:** Next.js configuration file.
*   **`postcss.config.js`:** PostCSS configuration file.
*   **`tailwind.config.js`:** Tailwind CSS configuration file.
*   **`tsconfig.json`:** TypeScript configuration file.

## Core Components Explained

*   **`Home` Component:** The main landing page, featuring a hero section, information cards, a 3D marquee, and background animations. Manages user authentication state.
*   **`Login` & `Register` Components:** Provide user authentication functionality using Radix UI components and a custom `useUserStore` hook.
*   **`CodeEditor` Component:** A code editor interface with language selection, test case execution, and AI assistance.
*   **`AppBar` Component:** The application's navigation bar, dynamically rendering links based on user authentication status.
*   **`BackgroundLines` Component:** A layout component that displays animated SVG lines as a background element.
*   **`ComboboxDemo` Component:** Implements a combobox for selecting a programming language.
*   **`Discussion` Component:** Fetches and displays discussion posts, allowing users to create new posts and comment on existing ones.
*   **`LeftDiv` Component:** Displays detailed information about a coding challenge.
*   **`RightDiv` Component:** A chat interface for interacting with an AI bot.
*   **`MiddleBottomDiv` Component:** Displays a list of test cases and details for the selected test case.
*   **`Footer` Component:** Renders the application's footer section.

## API Endpoints

*   `GET /api/v1/discussion`: Fetches existing discussion posts.
*   `POST /api/v1/discussion`: Creates a new discussion post.
*   `GET /api/v1/discussion/:postId/comments`: Fetches comments for a specific discussion post.
*   `POST /api/v1/discussion/:postId/comments`: Adds a new comment to a specific discussion post.
*   `DELETE /api/v1/discussion/:postId`: Deletes a discussion post.
*   `DELETE /api/v1/discussion/comments/:commentId`: Deletes a comment.
*   `POST /api/v1/auth/login`: Logs in a user.
*   `POST /api/v1/auth/register`: Registers a new user.
*   `GET /api/v1/users/:userId/activity`: Fetches user activity data.
*   `GET /api/v1/contests/:id`: Fetches contest details.
*   `POST /api/v1/gemini/evaluate`: Submits code for evaluation.
*   `POST /api/v1/gemini/chat`: Sends user input to the AI bot for processing.
*   `POST /api/v1/gemini/recommend`: Requests content recommendations based on user input.
*   `POST /api/v1/contests/submit`: Submits contest solution.

## State Management

*   **Zustand:** Used for managing global application state, including user authentication (`useUserStore`), code editor state (`useCodeEditorStore`), and test case data (`useTestCasesStore`).
*   **`useState`:** Used for managing component-specific state, such as form input values and UI visibility.
*   **`localStorage`:** Used for persisting user authentication data (user object and token) between sessions.

## Dependencies

*   **Next.js:** The React framework for building the application.
*   **React:** The core JavaScript library for building user interfaces.
*   **Tailwind CSS:** A utility-first CSS framework for styling the application.
*   **Radix UI:** A set of accessible UI primitives.
*   **clsx:** A utility for conditionally joining class names.
*   **tailwind-merge:** A utility for merging Tailwind CSS classes.
*   **framer-motion:** A library for creating animations.
*   **@monaco-editor/react:** A React component for the Monaco Editor (used in the code editor).
*   **zustand:** A minimalistic state management library.
*   **lucide-react:** A collection of beautiful icons.
*   **react-day-picker:** A date picker component.
*   **cmdk:** A headless command palette component.
*   **@lottiefiles/dotlottie-react:** A component for rendering Lottie animations.

## How to Run

1.  **Clone the repository:**

    ```bash
    git clone <repository_url>
    ```

2.  **Navigate to the project directory:**

    ```bash
    cd <project_directory>
    ```

3.  **Install dependencies:**

    ```bash
    npm install  # or yarn install, pnpm install, bun install
    ```

4.  **Run the development server:**

    ```bash
    npm run dev  # or yarn dev, pnpm dev, bun dev
    ```

5.  **Access the application:**

    Open `http://localhost:3000` in your browser.

6.  **Edit the homepage:**

    Modify `app/page.tsx` to change the homepage content.

## Deployment

*   **Recommended:** Deploy to [Vercel](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme)
*   [Next.js Deployment Documentation](https://nextjs.org/docs/app/building-your-application/deploying)

## Resources

*   [Next.js Documentation](https://nextjs.org/docs)
*   [Learn Next.js](https://nextjs.org/learn)
*   [Next.js GitHub Repository](https://github.com/vercel/next.js)
