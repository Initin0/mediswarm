# MediSwarm Prototype

> A decentralized AI-agent network for autonomous, privacy-preserving clinical trials.



## Table of Contents

- [About](#about)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Available Scripts](#available-scripts)
- [Configuration](#configuration)
  - [Vite](#vite)
  - [TypeScript](#typescript)
  - [Tailwind & PostCSS](#tailwind--postcss)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## About

MediSwarm is a **decentralized network** of React-based AI agents collaborating to design, manage, and execute clinical trials while ensuring patient privacy and data security. The platform leverages cutting-edge blockchain technology and AI-driven automation to revolutionize how clinical research is conducted.

### Key Concepts

- **Autonomous AI Agents**: Intelligent agents that can independently negotiate, collaborate, and execute tasks
- **Decentralized Architecture**: No single point of failure, ensuring robust and resilient operations
- **Privacy-First Design**: Patient data remains secure and private throughout the entire trial lifecycle
- **Blockchain Integration**: Immutable audit trails and transparent trial management

## Features

### 🤖 Agent-to-Agent Economy
AI agents negotiate resources, recruit participants, and process results autonomously, creating an efficient marketplace for clinical trial operations.

### 🔒 Privacy-Preserving Data Pipeline
- End-to-end encryption for all patient data
- OP_RETURN anchors on Bitcoin regtest for immutable auditability
- Zero-knowledge proofs for data verification without exposure
- HIPAA-compliant data handling

### 📊 Interactive Dashboard
- Real-time charts built with Recharts for trial metrics
- Live monitoring of agent activities and trial progress
- Comprehensive analytics and reporting tools
- Responsive design for desktop and mobile access

### 🌐 Decentralized Infrastructure
- Peer-to-peer communication between agents
- Fault-tolerant distributed system
- Scalable architecture supporting multiple concurrent trials

## Tech Stack

- **Framework:** React 18 with TypeScript
- **Router:** React Router DOM 6
- **Animations:** Framer Motion
- **Icons:** Lucide-React
- **Charts:** Recharts
- **Bundler:** Vite
- **Styling:** Tailwind CSS + PostCSS
- **Type Safety:** TypeScript
- **Testing:** Jest + React Testing Library (planned)
- **Blockchain:** Bitcoin regtest integration

## Installation

### Prerequisites

- Node.js 18+ and npm
- Git

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-org/mediswarm-prototype.git
   cd mediswarm-prototype
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env.local
   # Edit .env.local with your configuration
   ```

4. **Start development server**
   ```bash
   npm run dev
   ```

5. **Open your browser**
   Navigate to `http://localhost:5173`

## Available Scripts

In the project directory, you can run:

### `npm run dev`
Starts the Vite development server with hot module replacement.
- Local: `http://localhost:5173`
- Network: Available on your local network

### `npm run build`
Bundles the app for production to the `dist` folder.
- Optimizes the build for best performance
- Minifies and hashes filenames

### `npm run preview`
Preview the production build locally.
- Serves the built app from `dist` folder
- Useful for testing production builds

### `npm run lint`
Runs ESLint to check for code quality issues.

### `npm run type-check`
Runs TypeScript compiler to check for type errors.

These scripts rely on Vite's CLI tools and are configured in `package.json`.

## Configuration

### Vite

Configuration lives in `vite.config.ts`. Key features:
- React plugin for JSX support
- TypeScript path resolution
- Environment variable handling
- Development server configuration

```typescript
// Example vite.config.ts structure
export default defineConfig({
  plugins: [react()],
  resolve: {
    alias: {
      '@': path.resolve(__dirname, './src'),
    },
  },
})
```

### TypeScript

#### `tsconfig.app.json`
Configures compiler options for the application:
- Target: ES2020
- Strict type checking enabled
- JSX: react-jsx
- Module resolution: bundler

#### `tsconfig.node.json`
Used for Node.js-side configuration (Vite config, build scripts).

### Tailwind & PostCSS

#### `tailwind.config.js`
Defines custom design system:
- **Primary colors**: Medical-themed blue palette
- **Medical colors**: Healthcare-specific color scheme
- **Accent colors**: Highlight and interactive elements
- **Custom animations**: Float and glow effects for medical UI
- **Typography**: Medical documentation friendly fonts

#### `postcss.config.js`
PostCSS configuration:
- Tailwind CSS processing
- Autoprefixer for browser compatibility

## Project Structure

```
.
├── index.html                 # Entry HTML file
├── package.json              # Dependencies and scripts
├── vite.config.ts           # Vite bundler configuration
├── tsconfig.app.json        # TypeScript config for app
├── tsconfig.node.json       # TypeScript config for Node
├── postcss.config.js        # PostCSS configuration
├── tailwind.config.js       # Tailwind CSS configuration
├── .env.example            # Environment variables template
└── src/
    ├── assets/             # Static images, fonts, icons
    ├── components/         # Reusable UI components
    │   ├── ui/            # Basic UI components
    │   ├── charts/        # Chart components
    │   └── agents/        # Agent-specific components
    ├── pages/             # Top-level page views
    │   ├── Dashboard.tsx  # Main dashboard
    │   ├── Trials.tsx     # Clinical trials management
    │   └── Agents.tsx     # Agent network overview
    ├── routes/            # Route definitions & layout
    ├── hooks/             # Custom React hooks
    ├── utils/             # Utility functions
    ├── types/             # TypeScript type definitions
    ├── App.tsx            # Main App component
    └── main.tsx           # Application entry point
```

### Key Directories

- **`src/assets`** — Static resources (images, fonts, medical icons)
- **`src/components`** — Reusable React components organized by feature
- **`src/pages`** — Top-level page components for different app sections
- **`src/routes`** — React Router configuration and route guards
- **`src/hooks`** — Custom hooks for agent communication and data management
- **`src/utils`** — Utility functions for blockchain integration and data processing

## Contributing

We welcome contributions to MediSwarm!

### Development Workflow

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Make your changes and add tests
4. Commit your changes: `git commit -m 'Add amazing feature'`
5. Push to the branch: `git push origin feature/amazing-feature`
6. Open a Pull Request

### Code Style

- Follow the existing TypeScript and React patterns
- Use Tailwind CSS for styling
- Ensure all components are properly typed
- Add JSDoc comments for complex functions

## License

This project is licensed under the MIT License 

---



**Generated with ❤️ for the MediSwarm prototype**



