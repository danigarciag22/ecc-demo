```markdown
# ecc-demo Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns used in the `ecc-demo` TypeScript repository. It covers file naming conventions, import/export styles, commit message practices, and testing patterns. While no specific framework is detected, the repository follows clear conventions for organizing and writing code, making it easy to maintain and scale.

## Coding Conventions

### File Naming
- Use **PascalCase** for file names.
  - Example: `UserProfile.ts`, `OrderManager.ts`

### Import Style
- Use **relative imports** for referencing other modules.
  - Example:
    ```typescript
    import { UserService } from './UserService';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // In UserService.ts
    export function getUser() { ... }
    export const USER_ROLE = 'admin';
    ```

### Commit Messages
- Commit messages are **freeform** (no strict prefix), with an average length of 34 characters.
  - Example: `Add user authentication logic`

## Workflows

### Adding a New Module
**Trigger:** When you need to add a new feature or component.
**Command:** `/add-module`

1. Create a new file using PascalCase (e.g., `NewFeature.ts`).
2. Use named exports for all functions, classes, or constants.
3. Import dependencies using relative paths.
4. Write corresponding tests in a `.test.ts` file.

### Refactoring Existing Code
**Trigger:** When improving or restructuring code.
**Command:** `/refactor`

1. Identify the target file(s) to refactor.
2. Maintain PascalCase naming for files.
3. Ensure all imports remain relative.
4. Update exports to remain named.
5. Run tests to verify changes.

### Writing Tests
**Trigger:** When adding or updating features.
**Command:** `/write-test`

1. Create a test file with the pattern `*.test.ts` (e.g., `UserService.test.ts`).
2. Write tests using the project's preferred (unknown) testing framework.
3. Ensure all new code is covered by tests.
4. Run the test suite to confirm correctness.

## Testing Patterns

- Test files use the pattern `*.test.ts`.
- The testing framework is not specified; follow typical TypeScript testing practices.
- Example test file:
  ```typescript
  // UserService.test.ts
  import { getUser } from './UserService';

  test('should return user data', () => {
    const user = getUser('123');
    expect(user).toBeDefined();
  });
  ```

## Commands
| Command        | Purpose                                   |
|----------------|-------------------------------------------|
| /add-module    | Scaffold a new module/component           |
| /refactor      | Refactor existing code                    |
| /write-test    | Create and run tests for a module         |
```
