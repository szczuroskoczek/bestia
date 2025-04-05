---
title: "Migrations"
tldr: "BESTIA manages schema evolution with automated migration for simple changes and explicit advisories for complex updates, ensuring data integrity across versions."
---

# Migrations

## TL;DR

As your application evolves, BESTIA ensures that your dynamic data remains consistent with your schema. For straightforward changes, BESTIA automatically updates data. For complex changes—such as converting plain-text passwords to hashed values—developers provide explicit migration advisories. Each migration step is versioned and applied sequentially.

## The Challenge of Schema Evolution

- **Immutable History vs. Evolving Schema:**  
  Historical operations may become invalid if the schema changes. BESTIA uses snapshots as the true baseline and applies migration advisories to update dynamic data.

- **Versioning:**  
  Each BESTIA Manifest carries a version identifier. The engine compares this with the version stored with your dynamic data to determine if migrations are necessary.

## Migration Strategies

1. **Auto-Migration:**  
   For non-breaking changes (e.g., adding a new field with a default value), BESTIA automatically updates dynamic data.

2. **Explicit Migration Advisories:**  
   For breaking changes, such as:

   - Renaming or removing fields.
   - Transforming data (e.g., converting plain passwords to hashed passwords).

   Developers write migration scripts (e.g., in `src/bestia/evolution/1.2.2.js`) that detail the transformation from the old schema to the new one.

3. **New Baseline Creation:**  
   When migrations are too complex, BESTIA can archive old logs and create a new snapshot baseline while preserving the audit trail.

## Developer Workflow

- **During Development:**  
  Build your manifest using the BESTIA Compiler. Maintain a migration folder (`src/bestia/evolution/`) with versioned migration scripts.
- **In Production:**  
  On deployment, the engine detects a version mismatch and sequentially applies pending migrations to update the dynamic data before going live.

[Learn About Deployment](deployment.md)
