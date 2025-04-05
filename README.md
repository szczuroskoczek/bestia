# BESTIA Monorepo

**BESTIA** – Backend Engine for Scalable, Transactional, Integrated Applications  
_A unified, agnostic backend engine that merges your application logic with persistent storage into a single, portable artifact._

---

## TL;DR

BESTIA is a modern backend engine designed to simplify application development by unifying database schema, business logic, and dynamic data into one deployable unit. This monorepo contains all components of BESTIA:
- **Core:** The shared libraries for storage, migration, and execution.
- **Compiler:** A Node.js tool that compiles TypeScript-decorated schemas into a BESTIA manifest (immutable definitions).
- **Engine:** The runtime that loads the manifest, applies migrations, and manages dynamic data (snapshots, logs, indexes).
- **Integrations & CLI:** Adapters and command-line tools for various environments (Node.js, Docker, SaaS, etc.).
- **Docs:** Comprehensive documentation and guides (hosted via GitHub Pages).

---

## Overview & Vision

BESTIA addresses a common pain point in modern application development—the separation between backend logic and database management. By unifying these layers into one portable file, BESTIA:
- **Simplifies Deployments:** One artifact for schema, logic, and persistent data.
- **Enhances Developer Productivity:** Define your data models, commands, and queries using TypeScript decorators.
- **Streamlines Migrations:** Built-in strategies automatically manage schema evolution while preserving data integrity.
- **Supports Multiple Environments:** Whether in a Docker container, serverless function, Node.js app, or IoT device, BESTIA adapts to your deployment needs.

---

## Repository Structure

```
bestia-monorepo/
├── docs/                   # Documentation: guides, architecture overviews, migration strategies, FAQs, etc.
├── packages/
│   ├── core/               # Shared libraries (storage engine, migration logic, command/query execution)
│   ├── compiler/           # Compiler that transforms TypeScript schemas (with decorators) into a BESTIA manifest
│   ├── engine/             # Runtime engine that loads the manifest, handles migrations, and persists dynamic data
│   ├── integrations/       # Environment-specific adapters (Node.js, Docker, SaaS, etc.)
│   └── cli/                # Command-line tools for building, migrating, deploying, etc.
├── .gitignore              # Common ignore patterns for Node.js projects
├── LICENSE                 # License file (see below)
└── README.md               # This file
```

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (version 14+ recommended)
- [Yarn](https://yarnpkg.com/) or [npm](https://www.npmjs.com/) (for managing packages)

### Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/bestia-monorepo.git
   cd bestia-monorepo
   ```

2. **Install Dependencies:**

   If using Yarn Workspaces:
   ```bash
   yarn install
   ```

   Or with npm:
   ```bash
   npm install
   ```

3. **Run the Compiler (Example):**

   Navigate to the `packages/compiler` directory and run:
   ```bash
   npm run build
   npm run compile
   ```
   This generates your BESTIA manifest (e.g., `.bestia-manifest`) based on your TypeScript schemas.

4. **Run the Engine (Example):**

   In the `packages/engine` directory:
   ```bash
   npm run start
   ```
   The engine will load the manifest, check for migrations, and start processing commands and queries.

---

## Documentation

All documentation is located in the `docs/` folder. To view the docs on GitHub Pages:

1. Go to the repository’s **Settings** on GitHub.
2. Scroll down to the **GitHub Pages** section.
3. Set the source to the `docs/` folder.
4. Access your docs via the provided URL.

Each documentation page starts with a TL;DR summary to provide a quick overview before diving into details.

---

## License

BESTIA is available for personal, experimental use only. All commercial use is prohibited without explicit written permission from the author. For now, this project is licensed under the [PolyForm Noncommercial License 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0/).

> **Note:** This license is not OSI-approved. After a successgul stable release, the license will be updated to an OSI-approved license.