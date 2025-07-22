# Next.js Application README

This project is a Next.js application built using `create-next-app`.  It includes several modules for managing configuration, data, and user interaction.

## Description

This application provides a foundation for building a web application using Next.js.  It features optimized font loading with `next/font` (Geist font), and utilizes several custom modules for managing configuration, data (including a multiple-choice quiz), user authentication, and internship data.

## Features

* **Next.js App:** Built using the latest Next.js framework.
* **Optimized Font Loading:** Uses `next/font` for efficient Geist font loading.
* **Custom Configuration:**  Includes a custom Next.js configuration (`next.config.js`).
* **API Integration (Implied):**  Uses a backend URL (`https://ind1-backend-vercel.vercel.app`), suggesting API integration.
* **Multiple-Choice Quiz Data:**  Provides a structured JSON data set for a multiple-choice quiz covering various programming topics.
* **User Management:**  Includes a Zustand store (`useUserStore`) for managing user data, including authentication and persistence via `localStorage`.
* **Internship Management:**  Includes a Zustand store (`useInternshipStore`) for managing internship data, allowing for creating and editing drafts.
* **Custom Class Name Utility (`cn` function):**  Simplifies class name management in React components using `clsx` and `tailwind-merge`.


## Project Structure

The project structure follows the Next.js App Router convention.  Key modules include:

* **`next.config.js`:** Custom Next.js configuration.
* **`data/quizData.js`:** Contains the multiple-choice quiz data.
* **`stores/useUserStore.js`:** Zustand store for user management.
* **`stores/useInternshipStore.js`:** Zustand store for internship management.
* **`utils/cn.js`:** Utility function for combining class names.
* **`app/page.tsx`:** Main application page.


## How to Run

1. **Clone the repository:** `git clone <repository_url>`
2. **Navigate to the project directory:** `cd <project_directory>`
3. **Install dependencies:** `npm install` or `yarn install` or `pnpm install` or `bun install`
4. **Start the development server:** `npm run dev` or `yarn dev` or `pnpm dev` or `bun dev`
5. **Access the application:** `http://localhost:3000`


## Deployment

Deploy your application easily using Vercel:

[Vercel Deployment](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme)

See Next.js deployment documentation for more details:

[Next.js Deployment Documentation](https://nextjs.org/docs/app/building-your-application/deploying)


## Learning Resources

* **Next.js Documentation:** [https://nextjs.org/docs](https://nextjs.org/docs)
* **Next.js Learn:** [https://nextjs.org/learn](https://nextjs.org/learn)
* **Next.js GitHub:** [https://github.com/vercel/next.js](https://github.com/vercel/next.js)


## Module Details

### `next.config.js`

This module exports a Next.js configuration object (`nextConfig`) with details omitted for brevity.  It provides custom configuration for the application.

### `data/quizData.js`

This module exports a constant `CodePS`, a JavaScript object containing coding practice problems categorized by subject area.  Each subject (e.g., "AI", "Web Development") maps to an array of strings describing coding problems.  Topics include file handling, data structures, algorithms, machine learning, database operations, and system design.  Additionally, it contains a nested JSON array (`quiz`) representing a multiple-choice quiz with categories, questions, options, and correctness indicators.

### `stores/useUserStore.js`

A Zustand store managing user data, persisted using `zustand/middleware`.  It provides actions to add, update, and remove users, and manages the currently logged-in user.  Data is persisted in `localStorage`.

### `stores/useInternshipStore.js`

A Zustand store for managing internships.  It allows adding internships, managing a current draft, and updating the draft.

### `utils/cn.js`

This module exports the `cn` function, which combines class names using `clsx` and `tailwind-merge`.  It accepts a variable number of class names or class name generating functions.


This README provides a comprehensive overview of the Next.js application and its constituent modules.  Further details can be found within the individual module files.
