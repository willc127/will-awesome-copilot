---
description: "Use when creating or updating a project README.md: document its purpose, architecture, setup and run commands, and version tags using verified repository information."
applyTo: "**/README.md, **/readme.md"
---

# Project README Guidelines

- Before writing, inspect the project files and existing documentation to verify its purpose, architecture, prerequisites, scripts, and supported workflows. Do not infer details that the repository does not establish.
- Explain the project's purpose near the top of the README, including who or what it serves when that is clear from the codebase.
- Document the architecture at a useful level: identify the main components or directories and explain their responsibilities and important interactions. Keep diagrams or directory trees accurate and focused.
- Provide the prerequisites and exact commands needed to install dependencies, configure required environment values, and run the project. Include relevant test, build, or lint commands when defined by the project. Never invent commands or expose secrets; refer to environment variable names and describe how to obtain their values safely.
- Prefer a visible version badge linked to the matching release or Git tag when the repository provides a reliable version source, such as release tags, package metadata, or an existing release process. Never guess or fabricate a version; if no version is defined, omit the badge rather than presenting an unsupported value.
- When updating a README, preserve accurate and useful existing information, correct stale details, and avoid duplicating content already maintained elsewhere in the repository.
- Keep instructions concise and runnable. Verify documented paths, links, commands, and version references against the current repository before finishing.
