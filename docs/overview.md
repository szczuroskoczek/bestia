---
title: "Overview & Vision"
tldr: "BESTIA unifies backend logic and persistent storage into a single, portable file, solving the disconnect between application code and database management."
---

# Overview & Vision

## TL;DR

BESTIA addresses a fundamental pain point in modern development: the separation of backend logic and database management. By merging them into one artifact—the BESTIA Manifest—BESTIA simplifies deployments, ensures consistency, and eases schema migrations across multiple environments.

## Why BESTIA?

- **Unified Architecture:** Eliminate the gap between application code and persistent data.
- **Portable & Agnostic:** Run in serverless environments, Docker containers, Node.js applications, IoT devices, or even on desktop.
- **Streamlined Development:** Define your data models and operations using TypeScript decorators.
- **Simplified Migrations:** Built-in strategies keep your data in sync as your schema evolves.

## Target Environments

- **Serverless/SaaS:** A hosted BESTIA service compiles your manifest from a Git repository and centrally manages persistent data.
- **Docker Containers:** BESTIA runs with external volumes to protect dynamic data.
- **Embedded/Node.js:** Direct integration provides low-latency access.
- **IoT & Future Browser Support:** A lightweight design ideal for resource-constrained devices.

[Learn More in Core Concepts](core-concepts.md)
