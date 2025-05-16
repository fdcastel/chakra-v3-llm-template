# Vite + React + TypeScript + Chakra UI v3 Project

This project is a modern web application boilerplate built with Vite, React, TypeScript, and Chakra UI version 3. It's structured to provide a fast development experience and a robust foundation for building accessible and performant user interfaces.

A key aspect of this project is its setup for working effectively with Large Language Models (LLMs) like GitHub Copilot, ensuring adherence to Chakra UI v3 conventions.

## Key Features & Technologies

*   **Build Tool**: [Vite](https://vitejs.dev/) - For fast HMR, optimized builds, and a modern development experience.
*   **UI Framework**: [React](https://reactjs.org/)
*   **Language**: [TypeScript](https://www.typescriptlang.org/) - For static typing and improved code quality.
*   **UI Components**: [Chakra UI v3](https://chakra-ui.com/docs/getting-started) - A comprehensive component library for building accessible React applications. This project is specifically configured to use **version 3**, which has significant differences from v2.
*   **Linting/Formatting**: (Assumed ESLint/Prettier, check `package.json` and `eslint.config.js` for specifics)

## Getting Started

### Prerequisites

*   Node.js (version specified in `package.json` or latest LTS)
*   npm, yarn, or pnpm

### Installation

1.  Clone the repository:
    ```bash
    git clone <repository-url>
    cd <project-directory>
    ```
2.  Install dependencies (choose your package manager):
    ```bash
    npm install
    # or
    yarn install
    # or
    pnpm install
    ```

### Development

To start the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

This will typically start the server on `http://localhost:5173` (or another port if 5173 is busy).

### Building for Production

To create an optimized production build:

```bash
npm run build
# or
yarn build
# or
pnpm build
```

The build artifacts will be located in the `dist/` directory.

## Project Structure Highlights

```
.
├── docs/                     # Documentation for LLMs (Chakra v3 guidance)
│   ├── llms-components.txt
│   ├── llms-styling.txt
│   ├── llms-theming.txt
│   ├── llms-v3-migration.txt
│   └── llms.txt
├── public/                   # Static assets
├── src/
│   ├── components/
│   │   └── ui/               # Chakra UI v3 specific components (e.g., Provider, ColorMode)
│   ├── App.tsx               # Main application component
│   └── main.tsx              # Application entry point
├── vite.config.ts            # Vite configuration
├── tsconfig.json             # TypeScript configuration
├── package.json              # Project dependencies and scripts
└── README.md                 # This file
```

## Chakra UI v3 Integration

This project is set up to use Chakra UI v3. Key aspects include:

*   **Custom Provider**: Check `src/components/ui/provider.tsx` for the Chakra UI v3 provider setup.
*   **Color Mode**: Managed via `src/components/ui/color-mode.tsx`.
*   **Version 3 Conventions**: It's crucial to follow Chakra UI v3 syntax and patterns. Version 2 syntax will likely lead to errors. Refer to the official Chakra UI v3 documentation and the files in the `docs/` directory.

## LLM and GitHub Copilot Guidance

To ensure that LLMs (like GitHub Copilot) generate code that is compatible with Chakra UI v3 and other project conventions, this project includes:

*   **`docs/` directory**: Contains text files (`llms-*.txt`) specifically formatted to guide LLMs on Chakra UI v3 usage, including migration details, component specifics, styling, and theming. These are based on the official Chakra UI documentation for LLMs.

When working with Copilot or other LLMs, it's recommended to:
1.  Keep the relevant files from the `docs/` directory open or reference them in your prompts.
2.  Always explicitly state the need for **Chakra UI v3** code in your prompts.
3.  Review and test generated code carefully for adherence to v3 patterns.
