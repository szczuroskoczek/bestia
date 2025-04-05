---
title: "Migrations"
tldr: "BESTIA manages schema evolution by combining auto-migration for simple changes with explicit migration advisories for complex updates, ensuring data integrity."
---

# Migrations

## TL;DR

As your application evolves, BESTIA ensures that your dynamic data stays consistent with your schema. Simple changes can be auto-migrated, while complex changes (such as changing password storage from plain text to hashed) require explicit migration advisories. Each migration step is versioned and applied sequentially.

## The Challenge of Schema Evolution

- **Immutable History vs. Evolving Schema:**  
  Historical mutations may no longer be valid if the schema changes. BESTIA handles this by using snapshots as the true baseline, and migration advisories update dynamic data accordingly.
  
- **Versioning:**  
  Each compiled manifest contains a version identifier. The engine compares this against the version stored with your dynamic data to decide if migrations are needed.

## Migration Strategies

1. **Auto-Migration:**  
   For non-breaking changes (e.g., adding a new column with a default value), BESTIA automatically updates the dynamic data.

2. **Explicit Migration Advisories:**  
   For breaking changes, such as:
   - Changing a password field from plain text to hashed values.
   - Renaming or removing columns.
   The developer writes a migration script (e.g., `src/beast/evolution/1.2.2.js`) that transforms the old data to match the new schema.

3. **New Baseline on Breaking Changes:**  
   In cases where migration is too complex, BESTIA can archive old logs and create a new snapshot baseline, marking a fresh start while preserving audit trails.

## Developer Workflow

- **During Development:**  
  Build your manifest using the BESTIA compiler. As changes occur, maintain a migration folder (`src/beast/evolution/`) with versioned scripts.
  
- **In Production:**  
  When a new manifest is deployed, the engine detects a version mismatch and applies pending migrations sequentially before going live.

[Learn About Deployment](deployment.md)