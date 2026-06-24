```markdown
# pycord Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill teaches the core development patterns, coding conventions, and common workflows used in the `pycord` Python codebase. It covers how to contribute features, fix bugs, manage dependencies, update documentation, and maintain code quality using established conventions and step-by-step workflows. This guide is ideal for new contributors or maintainers seeking to align with the project's standards.

## Coding Conventions

- **Language:** Python
- **Framework:** None detected
- **Commit Style:** [Conventional Commits](https://www.conventionalcommits.org/)
  - Prefixes: `chore`, `fix`, `feat`, `ci`, `docs`
  - Example: `fix: correct typo in event handler`
- **File Naming:** camelCase
  - Example: `myModule.py`, `eventHandler.py`
- **Import Style:** Relative imports
  - Example:
    ```python
    from .utils import parseMessage
    ```
- **Export Style:** Named exports (explicitly listing symbols in `__all__`)
  - Example:
    ```python
    __all__ = ['MyClass', 'my_function']
    ```

## Workflows

### Dependency Update
**Trigger:** When a new version of a dependency is released and needs to be updated in the project  
**Command:** `/update-dependency`

1. Edit the relevant requirements or config file (e.g., `requirements/dev.txt`, `pyproject.toml`) to update the dependency version.
2. Commit the change with a message referencing the dependency and new version.
   - Example commit: `chore: bump requests to 2.31.0`
3. Push your changes and open a pull request if needed.

---

### Feature Addition or Enhancement
**Trigger:** When developing a new feature or enhancing existing functionality  
**Command:** `/add-feature`

1. Implement the feature or enhancement in one or more source files (e.g., `discord/myFeature.py`).
2. Update `CHANGELOG.md` to document the new feature.
3. Commit the changes together.
   - Example commit: `feat: add support for ephemeral messages`
4. Push and open a pull request for review.

---

### Bugfix with Changelog
**Trigger:** When a bug is discovered and needs to be fixed with traceability  
**Command:** `/fix-bug`

1. Fix the bug in the relevant source file(s) (e.g., `discord/buggyModule.py`).
2. Update `CHANGELOG.md` to describe the fix.
3. Commit both changes together.
   - Example commit: `fix: resolve crash on reconnect`
4. Push and open a pull request.

---

### Pre-commit Autoupdate
**Trigger:** When pre-commit hooks have new versions available  
**Command:** `/pre-commit-update`

1. Run `pre-commit autoupdate` to update `.pre-commit-config.yaml`.
2. Apply any auto-formatting or linting fixes to code files (e.g., `discord/*.py`).
3. Commit the updated config and any code changes.
   - Example commit: `chore: update pre-commit hooks`
4. Push and open a pull request.

---

### Docs Localization Workflow
**Trigger:** When localization workflows or Crowdin GitHub Actions need to be updated  
**Command:** `/update-docs-localization`

1. Edit `.github/workflows/docs-localization-download.yml` and/or `docs-localization-upload.yml` to update the action version.
2. Commit the workflow file changes.
   - Example commit: `ci: update Crowdin GitHub Action to v3.2.1`
3. Push and open a pull request.

---

### Documentation Fix or Enhancement
**Trigger:** When documentation needs to be improved or fixed  
**Command:** `/fix-docs`

1. Edit documentation source files (e.g., `docs/conf.py`).
2. Commit the documentation changes.
   - Example commit: `docs: fix Sphinx build warning`
3. Push and open a pull request.

---

## Testing Patterns

- **Test File Pattern:** Files named with `*.test.*` (e.g., `messageHandler.test.py`)
- **Testing Framework:** Not explicitly detected; check project docs or `requirements/dev.txt` for specifics.
- **Test Example:**
  ```python
  def test_parse_message():
      assert parseMessage("hello") == "hello"
  ```
- **Location:** Typically alongside or near the modules being tested.

## Commands

| Command                  | Purpose                                                      |
|--------------------------|--------------------------------------------------------------|
| /update-dependency       | Update a dependency version in requirements or config files   |
| /add-feature             | Add a new feature or enhance existing functionality          |
| /fix-bug                 | Fix a bug and update the changelog                          |
| /pre-commit-update       | Update pre-commit hooks and apply formatting/linting fixes   |
| /update-docs-localization| Update docs localization workflows (Crowdin, GitHub Actions) |
| /fix-docs                | Fix or enhance documentation                                |
```
