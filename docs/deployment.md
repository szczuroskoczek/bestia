---
title: "Deployment & Operations"
tldr: "Deploy BESTIA across various environments by separating immutable schema from dynamic data, using persistent volumes and automated migrations to ensure continuity."
---

# Deployment & Operations

## TL;DR

BESTIA is designed for flexible deployment:

- **Docker & Serverless:** Use external persistent storage (e.g., Docker volumes) to protect dynamic data.
- **Node.js & Embedded:** Integrate the engine as a module that handles migrations and state management.
- **SaaS Model:** A hosted BESTIA service compiles your manifest from your Git repository and centrally manages migrations and dynamic data.

## Deployment Scenarios

### Docker Deployment

- Package the BESTIA Engine in a Docker container.
- Mount a persistent volume (e.g., `/var/lib/bestia_data`) for dynamic data.
- On startup, the engine loads the new manifest, checks version differences, and runs migrations as needed.

### Serverless / SaaS Deployment

- Use a hosted BESTIA service that compiles the manifest from your Git repo.
- The service manages dynamic data centrally, applying migrations automatically.

### Node.js Integration

- Integrate the BESTIA Engine as a module in your application.
- Use middleware or adapters to expose RESTful endpoints for operations.

### IoT / Embedded Deployments

- Bundle the BESTIA Engine with your application (e.g., an Electron app or firmware).
- Persist dynamic data in a device-specific or user-specific storage location.

## Operational Considerations

- **Atomic Migrations:** Ensure migration steps are executed atomically to prevent data corruption.
- **Monitoring & Logging:** BESTIA logs all operations and migration steps for auditing and troubleshooting.
- **Rollback Strategies:** Provide mechanisms to revert to previous snapshots if a migration fails.

[Read FAQ](faq.md)
