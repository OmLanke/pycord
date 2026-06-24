---
name: feature-addition-or-enhancement
description: Workflow command scaffold for feature-addition-or-enhancement in pycord.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /feature-addition-or-enhancement

Use this workflow when working on **feature-addition-or-enhancement** in `pycord`.

## Goal

Add a new feature or enhance an existing one, typically involving code changes and updating the changelog.

## Common Files

- `CHANGELOG.md`
- `discord/**/*.py`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Implement the feature or enhancement in one or more source files.
- Update the CHANGELOG.md to document the new feature.
- Commit the changes together.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.