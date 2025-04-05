# BESTIA Monorepo

**BESTIA – Backend Engine for Scalable, Transactional, Integrated Applications**

BESTIA is a unified, agnostic backend engine that merges your application’s schema, business logic, and persistent data into a single, portable artifact. It’s designed to simplify deployment across Node.js, Docker, serverless platforms, IoT devices, and eventually desktop/browser environments.

---

## TL;DR

- **Unified Architecture:** One file (the BESTIA Manifest) holds your immutable schema/logic; dynamic data (snapshots, logs, indexes) is persisted separately.
- **Multiple Deployments:** Use BESTIA as a hosted SaaS, Docker container, embedded Node.js module, or on IoT devices.
- **Seamless Migrations:** Built-in strategies automatically evolve your schema without manual intervention for common changes.
- **Developer-Centric:** Leverage TypeScript decorators to define models and operations (Queries and Actions) in an intuitive, type-safe way.

---

## Repository Structure

```
bestia-monorepo/
├── docs/                   # Documentation files (this site)
├── packages/
│   ├── core/               # Shared libraries: storage engine, migration logic, operation execution
│   ├── compiler/           # Compiler that transforms your TypeScript-decorated schemas into a BESTIA Manifest
│   ├── engine/             # Runtime engine that loads the manifest, applies migrations, and persists dynamic data
│   ├── integrations/       # Adapters for Node.js, Docker, SaaS, etc.
│   └── cli/                # Command-line tools for building, migrating, deploying, etc.
├── .gitignore              # Git ignore patterns
├── LICENSE                 # Licensing information
└── README.md               # This file
```

---

## Getting Started

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/bestia-monorepo.git
   cd bestia-monorepo
   ```

2. **Install Dependencies:**  
   Use Yarn or npm with workspaces if desired.

   ```bash
   yarn install
   ```

   or

   ```bash
   npm install
   ```

3. **Build & Run Examples:**

   - Run the compiler (in `packages/compiler`) to generate the BESTIA Manifest (e.g., `.bestia-manifest`).
   - Start the engine (in `packages/engine`) to load the manifest, apply migrations, and serve operations.

4. **Documentation:**  
   See the `docs/` folder for detailed guides.

---

## License

BESTIA is available for personal and experimental use only. All commercial use is prohibited without explicit written permission. Currently, BESTIA is licensed under the [PolyForm Noncommercial License 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0/).  
_Note: This license is not OSI-approved; dual licensing may be considered in the future._

---

## Contributing

Contributions are welcome while BESTIA is in its experimental phase. Please see [docs/CONTRIBUTING.md](./docs/CONTRIBUTING.md) for guidelines.

---

## Roadmap

- Enhance core storage performance and migration automation.
- Expand integrations for serverless, Docker, and IoT.
- Improve developer tools and documentation.
- Explore future browser/desktop deployments.

For detailed updates, see [docs/roadmap.md](./docs/roadmap.md).

---

_Unleash the power of unified backend development with BESTIA!_
