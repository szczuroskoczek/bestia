---
title: "FAQ"
tldr: "Frequently Asked Questions about BESTIA cover topics from schema evolution and migrations to deployment strategies and licensing."
---

# FAQ

## TL;DR

This FAQ addresses common concerns about BESTIA’s unified architecture, migration strategy, deployment options, and licensing.

### Q: What is BESTIA?

**A:** BESTIA is a unified backend engine that combines schema definitions, business logic, and persistent data into a single, portable file.

### Q: How does BESTIA handle schema changes?

**A:** BESTIA uses a versioned manifest and a combination of auto-migration and explicit migration advisories to update dynamic data while preserving data integrity.

### Q: How do I deploy BESTIA without losing data?

**A:** Deploy BESTIA with external persistent storage (e.g., Docker volumes) or use a hosted SaaS model to ensure that dynamic data is not overwritten during updates.

### Q: Can I run BESTIA in serverless environments?

**A:** Yes. BESTIA is designed to be agnostic and can be integrated into serverless architectures, with a central hosted service managing state and migrations.

### Q: What licensing does BESTIA use?

**A:** Currently, BESTIA is released for personal and experimental use under the PolyForm Noncommercial License 1.0.0. Commercial use is prohibited without explicit permission. (Future licensing options, including dual licensing, may be considered.)

### Q: What if I miss a migration step?

**A:** The BESTIA engine performs version checks on startup. If migrations are missing or out-of-sequence, it will either auto-migrate safe changes or require manual intervention, ensuring that data integrity is maintained.