# Architecture Specification

**This document describes the overall architecture of this project:**

- The new-client (already known as bar-lobby) is only for the view and to trigger events.
- The logic and database is handled by the server (teiserver).
- For communication the new tachyon-protocol has to be used.
