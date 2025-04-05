---
title: "Deployment & Operations"
tldr: "Deploy BESTIA across various environments by separating immutable schema from dynamic data, using persistent volumes and automatic migrations to ensure continuity."
---

# Deployment & Operations

## TL;DR

BESTIA is designed for flexible deployment:
- **Docker & Serverless:** Use external persistent storage (volumes) to retain dynamic data.
- **Node.js & Embedded Systems:** Integrate the engine as a module that manages migrations and dynamic data.
- **SaaS Model:** A hosted BESTIA service compiles the manifest from your Git repo and manages migration centrally.

## Deployment Scenarios

### Docker Deployment

- Package the BESTIA engine in a Docker container.
- Mount a persistent volume (e.g., `/var/lib/bestia_data`) to store snapshots, logs, and indexes.
- On container startup, the engine reads the new manifest, compares versions, and runs migrations if necessary.

### Serverless / SaaS Deployment

- Use a hosted BESTIA service that automatically compiles the manifest from your Git repository.
- The service manages dynamic data centrally, applying migrations and ensuring data consistency across deployments.

### Node.js Integration

- Integrate the BESTIA engine directly into your application.
- Use provided middleware or adapters to expose RESTful endpoints for commands and queries.

### IoT / Embedded Deployments

- Bundle the BESTIA engine with your application (e.g., an Electron app or firmware for IoT).
- Save dynamic data in a user-specific location or device storage, ensuring updates preserve the existing data.

## Operational Considerations

- **Atomic Migrations:** Ensure migrations run atomically to prevent data corruption.
- **Monitoring & Logging:** BESTIA logs all operations and migration steps for auditing and troubleshooting.
- **Rollback Strategies:** Provide mechanisms to revert to previous snapshots if a migration fails.

[Read FAQ](faq.md)