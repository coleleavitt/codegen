```markdown
# codegen Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `codegen` TypeScript repository. You'll learn how to structure files, write imports and exports, follow commit message conventions, and understand the project's approach to testing. The guide also provides suggested commands for common workflows to streamline your development process.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `myModule.ts`, `userService.ts`

### Import Style
- Use **relative imports** for referencing other modules.
  - Example:
    ```typescript
    import { myFunction } from './utils';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // utils.ts
    export function myFunction() { /* ... */ }
    ```

### Commit Messages
- Use the `feat` prefix for new features.
- Commit messages are concise, averaging around 33 characters.
  - Example: `feat: add user authentication`

## Workflows

### Adding a New Feature
**Trigger:** When implementing a new feature or module  
**Command:** `/add-feature`

1. Create a new file using camelCase naming.
2. Implement the feature using TypeScript.
3. Use relative imports to include dependencies.
4. Export functions or classes using named exports.
5. Write a commit message starting with `feat:`.
6. If applicable, add or update corresponding test files.

### Refactoring Code
**Trigger:** When improving or restructuring existing code  
**Command:** `/refactor`

1. Identify the code to refactor.
2. Update the code while maintaining camelCase file naming.
3. Adjust imports/exports as needed, keeping them relative and named.
4. Update or add tests if necessary.
5. Commit changes with a clear message (e.g., `refactor: improve utility functions`).

## Testing Patterns

- Test files follow the `*.test.*` naming pattern.
  - Example: `utils.test.ts`
- The testing framework is not explicitly specified; check existing test files for patterns.
- Place test files alongside or near the modules they test.

  ```typescript
  // utils.test.ts
  import { myFunction } from './utils';

  test('myFunction returns correct value', () => {
    expect(myFunction()).toBe(/* expected value */);
  });
  ```

## Commands
| Command        | Purpose                                           |
|----------------|---------------------------------------------------|
| /add-feature   | Guide for adding a new feature or module          |
| /refactor      | Steps for refactoring existing code               |
```
