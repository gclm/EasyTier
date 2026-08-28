```markdown
# EasyTier Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill provides guidance on contributing to the EasyTier Rust codebase. It covers the project's coding conventions, commit message patterns, and testing practices. By following these patterns, you can ensure consistency and maintainability across the codebase.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `easyTierManager.rs`, `tierConfig.rs`

### Import Style
- Use **relative imports** within the codebase.
  - Example:
    ```rust
    use crate::tierConfig::TierConfig;
    ```

### Export Style
- Use **named exports** for modules and functions.
  - Example:
    ```rust
    pub fn calculateTier() { ... }
    ```

### Commit Messages
- Follow **conventional commit** format.
- Supported prefixes: `fix`, `feat`
- Example:
  ```
  feat: add support for dynamic tier adjustment
  fix: resolve panic on empty tier list
  ```

## Workflows

### Feature Development
**Trigger:** When adding a new feature  
**Command:** `/feature`

1. Create a new branch for your feature.
2. Implement the feature using camelCase file naming and relative imports.
3. Write or update tests in corresponding `*.test.*` files.
4. Commit changes with a `feat:` prefix and descriptive message.
5. Open a pull request for review.

### Bug Fixing
**Trigger:** When fixing a bug  
**Command:** `/fix`

1. Create a new branch for the bug fix.
2. Apply the fix, maintaining code style conventions.
3. Update or add tests in `*.test.*` files to cover the fix.
4. Commit with a `fix:` prefix and clear description.
5. Open a pull request for review.

## Testing Patterns

- Test files follow the `*.test.*` naming pattern.
  - Example: `tierManager.test.rs`
- The testing framework is not specified; use Rust's built-in test module unless otherwise noted.
- Example test:
  ```rust
  #[cfg(test)]
  mod tests {
      use super::*;

      #[test]
      fn test_calculate_tier() {
          assert_eq!(calculateTier(5), "Silver");
      }
  }
  ```

## Commands
| Command    | Purpose                                   |
|------------|-------------------------------------------|
| /feature   | Start a new feature development workflow  |
| /fix       | Start a bug fixing workflow               |
```
