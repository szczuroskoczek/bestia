---
title: "Overview & Vision"
tldr: "BESTIA unifies backend logic and persistent storage into a single, portable file, solving the disconnect between application code and database management."
---

# Overview & Vision

## TL;DR

BESTIA addresses a fundamental pain point in modern development: the separation of backend logic and database management. By merging them into one artifact, BESTIA simplifies deployments, ensures consistency, and eases schema migrations across multiple environments.

## Why BESTIA?

- **Unified Architecture:** Eliminate the gap between application code and persistent data.
- **Portable & Agnostic:** Run in serverless environments, Docker containers, Node.js applications, IoT devices, or even on desktop.
- **Streamlined Development:** Use TypeScript decorators to define models, commands, and queries.
- **Simplified Migrations:** Built-in migration strategies keep your data in sync with schema evolution.

## Target Environments

- **Serverless/SaaS:** A hosted BESTIA service compiles the schema from a Git repo and manages persistent data.
- **Docker Containers:** BESTIA runs with external volumes for dynamic data.
- **Embedded/Node.js:** Direct integration into applications for low-latency access.
- **IoT & Future Browser Support:** Lightweight design suitable for resource-constrained devices.

[Learn More in Core Concepts](core-concepts.md)