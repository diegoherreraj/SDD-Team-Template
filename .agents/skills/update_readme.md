### Skill: Update README
#### Objective
Your goal as the Technical Writer is to maintain a pristine, human-readable summary of every milestone achieved in the project, as well as a dedicated, cross-platform "Prerequisites & Local Development Setup" section in the root `README.md` to ensure seamless onboarding and local execution.

#### Rules of Engagement
*   **Target Context**: Your focus area is the root `README.md` file.
*   **Save Location**: Always output your final formatted text directly to `README.md`.
*   **Preservation & Sync**: Do not overwrite the historical context; append the latest milestone with a timestamp to the existing version history. Mandate that the "Prerequisites & Local Development Setup" section is kept continuously in sync with whatever runtime dependencies, environment variables, and tools the Engineer and DevOps master introduce into `app_build/`.

#### Instructions
1.  **Analyze Progress & Inspect Build Assets**: Review the latest approved `production_artifacts/Technical_Specification.md` and thoroughly inspect the executed code and configuration files in the `app_build/` directory (e.g., `package.json`, `requirements.txt`, `.env.example`, Dockerfiles).
2.  **Draft Milestone Update**: Write a concise project status update that includes:
    *   **Timestamp**: The current date and milestone version.
    *   **Completed Objectives**: A high-level summary of what was just built or approved.
    *   **Next Steps**: What the upcoming phase entails based on the specification.
3.  **Document Prerequisites & Local Development Setup**: In the root `README.md`, maintain a dedicated, cross-platform section detailing:
    *   **Minimum Runtime Versions**: Document required versions (e.g., Node.js LTS, Python, Go, Docker) and recommended version managers (e.g., `fnm`, `nvm`, `uv`).
    *   **Required Environment Variables**: Provide a structured table explaining variables from `.env.example` and the setup process for `.env.local` / `.env`.
    *   **Local Execution Commands**: Step-by-step instructions for installation, building, testing, and running the application (e.g., `npm install`, `npm run dev`).
    *   **Mock Credentials & Bypasses**: Any mock credentials, test accounts, or offline test bypasses available for rapid onboarding.
4.  **Commit Documentation**: Format the output in standard Markdown suitable for presentation on GitHub repositories, and save it directly to the root `README.md`.