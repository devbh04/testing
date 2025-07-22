# Next.js Project

## Description

This project is a Next.js application initialized with `create-next-app`. It serves as a foundation for building web applications with Next.js, demonstrating a basic setup, and providing resources for further development, learning, and deployment. It also includes example configurations, API endpoint definitions, and state management implementations to showcase common patterns used in larger Next.js applications.

## Features

*   **Next.js Core:**
    *   Initialized with `create-next-app`.
    *   Demonstrates fundamental Next.js concepts.
*   **Development Server:** Starts a local development server at `http://localhost:3000` using `npm run dev`, `yarn dev`, `pnpm dev`, or `bun dev`.
*   **Live Reloading:**  `app/page.tsx` auto-updates in the browser upon file changes, providing a rapid development experience.
*   **Font Optimization:**  Utilizes `next/font` to automatically optimize and load the Geist font family, improving website performance and aesthetics.
*   **API Configuration:** Defines a base URL for API requests, currently configured for the production (Vercel) backend.
*   **Problem Statements:** Includes a structured object (`CodePS`) containing categorized coding problem statements across various computer science domains.
*   **Quiz Data:** Provides a `quiz` array, representing a quiz structure with categories, questions, and options, suitable for building interactive quiz applications.
*   **CSS Class Name Utility:**  A `cn` utility function using `clsx` and `tailwind-merge` to combine and resolve CSS class names, particularly useful with Tailwind CSS.
*   **User State Management:** Implements a Zustand store (`useUserStore`) for managing user data and authentication state, persisting data to localStorage.
*   **Internship State Management:**  A Zustand store (`useInternshipStore`) manages internship data and a draft object for creating/editing internships.

## Project Structure

.
├── app/
│   └── page.tsx           # Example Next.js page
├── config.js              # API base URL configuration
├── CodePS.js              # Categorized coding problem statements
├── quiz.js                # Quiz data structure
├── lib/
│   └── utils.ts         # Utility functions (e.g., cn for CSS class names)
├── store/
│   ├── userStore.ts       # Zustand store for user data
│   └── internshipStore.ts # Zustand store for internship data
├── next.config.js         # Next.js configuration file
├── package.json           # Project dependencies and scripts
├── README.md              # This file
└── ...

**Key Files and Directories:**

*   `app/`: Contains the Next.js application pages and components.
*   `config.js`: Defines the `BASE_URL` for API requests.
*   `CodePS.js`:  Holds the categorized coding problem statements.
*   `quiz.js`:  Defines the quiz data structure.
*   `lib/utils.ts`: Contains utility functions like `cn` for handling CSS class names.
*   `store/`: Contains Zustand stores for state management (user and internship data).
*   `next.config.js`:  The Next.js configuration file.
*   `package.json`: Lists project dependencies and defines npm scripts.

## How to Run

1.  **Install Dependencies:**

    ```bash
    npm install  # Or yarn install, pnpm install, bun install
    ```

2.  **Run the Development Server:**

    ```bash
    npm run dev  # Or yarn dev, pnpm dev, bun dev
    ```

    This will start the development server at `http://localhost:3000`.

3.  **Explore the Application:**

    Open your browser and navigate to `http://localhost:3000` to view the application.  Changes made to the code will automatically reload in the browser.

## Resources

*   [Next.js Documentation](https://nextjs.org/docs)
*   [Learn Next.js Tutorial](https://nextjs.org/learn)
*   [Next.js GitHub Repository](https://github.com/vercel/next.js)

## Deployment

*   Recommended deployment platform: [Vercel](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme)
*   [Next.js Deployment Documentation](https://nextjs.org/docs/app/building-your-application/deploying)
