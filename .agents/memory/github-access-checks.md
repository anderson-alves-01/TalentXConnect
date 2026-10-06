---
name: GitHub access checks
description: Distinguishing connection health from access to organization repositories.
---

A GitHub source-control connection reported as active and healthy, even with the repo scope, does not establish that workspace Git commands can access a particular organization repository.

**Why:** Connection health checks succeeded while repository fetch authentication failed. Treating connection health as proof of repository access would give the user incorrect assurances.

**How to apply:** Verify access with an actual request to the target repository before claiming that authentication is resolved or that a push can proceed.
