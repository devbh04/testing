# CodeVibe Project - A Platform for Opportunities

## Description

CodeVibe is a platform designed to connect users with various opportunities in the tech and related fields. It offers features for discovering and participating in internships, hackathons, mentorship programs, and courses. The platform aims to be a central hub for career development and networking.

## Key Features

*   **Development Server:** Starts a local development server at `http://localhost:3000` using `npm run dev`, `yarn dev`, `pnpm dev`, or `bun dev`.
*   **Live Reloading:** Changes to files are automatically reflected in the browser, facilitating rapid development.
*   **Font Optimization:** Utilizes `next/font` to automatically optimize and load fonts (e.g., Geist, Work Sans).
*   **Opportunity Discovery:** Provides categorized sections for internships, hackathons, mentorships, and courses.
*   **Search and Filtering:** Allows users to search and filter opportunities based on various criteria (e.g., title, skills, specialization).
*   **User Authentication:** Implements user authentication and authorization, including admin roles.
*   **User Profiles:** Allows users to view and edit their profile information.
*   **Opportunity Creation:** Enables recruiters and admins to create and manage opportunities (internships, hackathons, mentorships, courses).
*   **Registration and Enrollment:** Provides functionality for users to register for hackathons and enroll in courses.
*   **Data Persistence:** Uses localStorage for some client-side data persistence (e.g., user authentication).
*   **Admin Interface:** Provides an admin interface for managing users and content.

## Project Structure

The project is structured as a Next.js application, leveraging server-side rendering, client-side rendering, and API routes. Here's a breakdown of key components:

*   **`app/` directory:** Contains the application's route handlers, pages, and layouts.

    *   **`app/page.tsx`:** The main landing page of the application.
    *   **`app/layout.tsx`:** Defines the root layout of the application, including document language, font imports, metadata, and global styles.
    *   **`app/signin`:** Route for user sign-in.
    *   **`app/profile`:** Route for user profiles.
    *   **`app/blog`:** Route for blog posts.
    *   **`app/courses`:** Route for courses.
    *   **`app/hackathons`:** Route for hackathons.
    *   **`app/internships`:** Route for internships.
    *   **`app/mentorships`:** Route for mentorships.
    *   **`app/create`:** Route for creating new opportunities.
    *   **`app/admin`:** Route for admin panel.

*   **`components/` directory:** Contains reusable UI components.

    *   **`components/shared/`:** Contains components shared across the application.
        *   **`AppBar`:** The application's navigation bar.
        *   **`Footer`:** The application's footer.
        *   **`cards/`:** Contains card components for displaying opportunities.
            *   `CourseCard`
            *   `InternshipCard`
            *   `MentorCard`
            *   `HackathonCard`
        *   **`CarouselSliderCourse`:** A carousel slider for displaying courses.
        *   **`CarouselSliderIntern`:** A carousel slider for displaying internships.
        *   **`CarouselSliderMentor`:** A carousel slider for displaying mentors.
        *   **`CarouselSliderHackathon`:** A carousel slider for displaying hackathons.
    *   **`components/ui/`:** Contains UI components from a library like Shadcn UI.
        *   `Input`, `Button`, `Label`, `Textarea`, `Popover`, `Calendar`, `Select`, `AlertDialog`, etc.

*   **`lib/` directory:** Contains utility functions.

    *   **`lib/utils.ts`:** Contains utility functions, such as `cn` for conditionally joining class names.

*   **`store/` directory:** Contains Zustand stores for managing application state.

    *   **`store/signUpStore.ts`:** A Zustand store for managing user data.

*   **`utils/` directory:** Contains constants and helper functions.

    *   **`utils/constants.ts`:** Defines constant values, such as the base API URL (`BASE_URL`).

*   **`next.config.js`:** Configures the Next.js application.
*   **`public/` directory:** Contains static assets, such as images and fonts.

## How to Run

1.  **Clone the repository:**

    ```bash
    git clone <repository_url>
    cd <project_directory>
    ```

2.  **Install dependencies:**

    Choose your preferred package manager:

    ```bash
    npm install        # Using npm
    yarn install       # Using yarn
    pnpm install       # Using pnpm
    bun install        # Using bun
    ```

3.  **Configure Environment Variables:**

    Create a `.env.local` file in the root directory of the project.  Add any required environment variables, especially the `BASE_URL` pointing to your backend API.  Example:

    ```
    NEXT_PUBLIC_BASE_URL=http://localhost:8000  # Example - Replace with your actual backend URL
    ```

    *Note:  The examples provided in some of the component descriptions use `BASE_URL` directly.  In Next.js, to access environment variables in the browser, they should be prefixed with `NEXT_PUBLIC_`.  Adjust your code accordingly if necessary.*

4.  **Start the development server:**

    Choose your preferred package manager:

    ```bash
    npm run dev        # Using npm
    yarn dev       # Using yarn
    pnpm dev       # Using pnpm
    bun dev        # Using bun
    ```

5.  **Access the application:**

    Open your web browser and navigate to `http://localhost:3000`.

## Resources

*   **Next.js Documentation:** [https://nextjs.org/docs](https://nextjs.org/docs)
*   **Learn Next.js Tutorial:** [https://nextjs.org/learn](https://nextjs.org/learn)
*   **Next.js GitHub Repository:** [https://github.com/vercel/next.js](https://github.com/vercel/next.js)
*   **Vercel Deployment:** The recommended deployment platform is Vercel. See [https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) and the [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying).
