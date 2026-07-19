```markdown
# codex Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill provides a comprehensive guide to the development patterns and workflows used in the `codex` TypeScript repository. It covers coding conventions, commit styles, testing patterns, and step-by-step instructions for common workflows such as adding production readiness controls. This guide is intended to help new and existing contributors maintain consistency and quality across the codebase.

## Coding Conventions

### File Naming
- Use **snake_case** for all file names.
  - Example:  
    ```
    user_profile.ts
    api_utils.test.ts
    ```

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { fetchData } from './api_utils';
    ```

### Export Style
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // In user_profile.ts
    export function getUserProfile(id: string) { ... }

    // In another file
    import { getUserProfile } from './user_profile';
    ```

### Commit Patterns
- Follow **conventional commit** style.
- Use the `chore` prefix for maintenance or non-feature commits.
- Keep commit messages concise (average ~62 characters).
  - Example:
    ```
    chore: update dependencies and fix minor lint issues
    ```

## Workflows

### Add Production Readiness Control
**Trigger:** When you need to introduce or update production readiness documentation or controls for the project or its components.  
**Command:** `/add-production-readiness`

1. **Identify** documentation or control files that require production readiness information.
2. **Edit or create** the relevant markdown files, such as:
    - `AGENTS.md`
    - `CLAUDE.md`
    - `.github/PRODUCTION_READINESS.md`
    - `.github/pull_request_template.md`
3. **Add or update** sections related to production readiness controls.
4. **Commit** each file addition or update with a descriptive message, following the conventional commit style.
    - Example:
      ```
      chore: add production readiness checklist to CLAUDE.md
      ```
5. **Push** your changes and open a pull request for review.

## Testing Patterns

- Test files follow the `*.test.*` naming convention.
  - Example:  
    ```
    api_utils.test.ts
    ```
- The specific testing framework is not detected; check existing test files for patterns.
- Place test files alongside the modules they test or in a dedicated test directory, as per project structure.

## Commands

| Command                      | Purpose                                                      |
|------------------------------|--------------------------------------------------------------|
| /add-production-readiness    | Add or update production readiness documentation or controls |
```
