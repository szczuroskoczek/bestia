---
title: "FAQ"
tldr: "This FAQ addresses common questions about BESTIA’s unified architecture, migration strategy, deployment options, and licensing."
---

# FAQ

## TL;DR

This FAQ answers common questions about BESTIA’s design, including how it unifies schema and dynamic data, manages migrations, and supports multiple deployment environments.

### Q: What is BESTIA?

**A:** BESTIA is a unified backend engine that combines your schema, business logic, and persistent data into a single deployable artifact.

### Q: How does BESTIA handle schema changes?

**A:** BESTIA uses a versioned manifest and applies migrations—either auto-migrated for simple changes or via explicit migration advisories for complex updates—to ensure that dynamic data remains consistent with the schema.

### Q: How do I deploy BESTIA without losing data?

**A:** By separating the immutable manifest from the dynamic data and using persistent storage (like Docker volumes or external storage in serverless setups), you ensure that data is preserved across deployments. The engine automatically runs migrations on startup.

### Q: What are Queries and Actions in BESTIA?

**A:** Queries are read-only operations for retrieving data. Actions are operations that modify state.

### Q: What licensing does BESTIA use?

**A:** Currently, BESTIA is licensed for personal and experimental use under the PolyForm Noncommercial License 1.0.0. Commercial use is prohibited without explicit permission.
