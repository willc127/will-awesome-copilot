---
name: create-readme-instruction
description: "Create or update an agent instruction for writing project README files. Use when asked to create a README instruction, README guidelines, or a reusable rule set for README.md/readme.md files."
argument-hint: "Optional: instruction path, README filename patterns, or project-specific requirements"
user-invocable: true
---

# Create README Instructions

Create or update a workspace instruction that guides an AI agent when writing or maintaining a project's README. This skill produces the instruction file; it does not write the README itself.

## Procedure

1. Identify the workspace root and inspect its existing customization layout. Look for instruction files and follow the repository's established location and naming conventions. If none exist, use `.github/instructions/readme.instructions.md`.
2. Read the current README files and the small set of files that establish project facts, such as manifests, build configuration, CI workflows, and relevant documentation. Use these to identify which README patterns the instruction should cover and what must be verified before documenting.
3. Check for an existing README instruction at the intended path. Preserve useful guidance and update it in place rather than creating a duplicate. Ask a concise clarifying question only when the destination or requested scope cannot be resolved from the workspace and the user's request.
4. Write valid YAML frontmatter with a useful `description` and an `applyTo` pattern matching the intended README filenames. Keep project-specific facts out of reusable rules unless they are explicitly required; instead, instruct the agent to verify facts against the repository.
5. Include concise, actionable guidance appropriate to the project. Consider purpose and audience, architecture, prerequisites and runnable commands, environment-variable safety, existing content, and version or release references only where applicable. Explicitly forbid guessing unsupported facts or commands.
6. Save the instruction at the chosen path. Verify the frontmatter delimiters and YAML, confirm `applyTo` covers the intended files, and ensure every rule is relevant, non-duplicative, and supported by the repository's needs.

## Output

Create or update only the README-focused instruction file unless the user asks for additional changes. Report its path and summarize the README behaviors it covers.
