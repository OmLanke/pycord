---
name: dependency-update
description: Workflow command scaffold for dependency-update in pycord.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /dependency-update

Use this workflow when working on **dependency-update** in `pycord`.

## Goal

Update the version of a dependency in requirements or config files, typically via automated tools like dependabot.

## Common Files

- `requirements/dev.txt`
- `requirements/speed.txt`
- `pyproject.toml`
- `.pre-commit-config.yaml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit the relevant requirements or config file to update the dependency version.
- Commit the change with a message referencing the dependency and new version.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.