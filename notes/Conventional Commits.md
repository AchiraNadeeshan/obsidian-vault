#git #github #programming #commit 

# Conventional Commits

## Introduction

Conventional Commits is a standardized format for writing commit messages. It helps maintain a consistent and structured history in a codebase, making it easier for developers to understand changes, generate changelogs, and automate versioning.

## Commit Message Structure

A commit message follows this structure:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

### Elements:

1. **Type**: Specifies the purpose of the commit (e.g., `feat`, `fix`).
    
2. **Scope (Optional)**: Indicates the part of the codebase affected.
    
3. **Description**: A brief summary in the imperative mood.
    
4. **Body (Optional)**: Provides additional details about the change.
    
5. **Footer (Optional)**: Includes breaking changes or issue references.
    

### Example 1: Footer-Only Breaking Change Notation
```
feat(auth): add OAuth2 support for authentication

Implemented OAuth2 authentication flow, allowing users to log in using third-party providers.
This improves security and provides a more seamless user experience.

BREAKING CHANGE: The previous authentication system has been removed. 
Users must migrate to the new OAuth2-based authentication flow.

Closes #123, #456
```

### Example 2: Inline Breaking Change Notation
```
feat(auth)!: add OAuth2 support for authentication

Implemented OAuth2 authentication flow, allowing users to log in using third-party providers.
This improves security and provides a more seamless user experience.

BREAKING CHANGE: The previous authentication system has been removed. 
Users must migrate to the new OAuth2-based authentication flow.

Closes #123, #456
```

## Common Commit Types

- **feat**: Introduces a new feature.
    
- **fix**: Fixes a bug.
    
- **docs**: Updates documentation.
    
- **style**: Code style changes (no logic changes).
    
- **refactor**: Code restructuring without altering behavior.
    
- **perf**: Performance improvements.
    
- **test**: Adds or updates tests.
    
- **build**: Modifies build tools or dependencies.
    
- **ci**: Updates continuous integration settings.
    
- **chore**: Miscellaneous tasks (e.g., dependency updates).
    
- **revert**: Reverts a previous commit.
    

## Breaking Changes

Breaking changes require special notation:

```
feat!: introduce new authentication system

BREAKING CHANGE: The authentication system has been redesigned.
```

Alternatively, breaking changes can be indicated in the footer:

```
feat: allow provided config object to extend other configs

BREAKING CHANGE: `extends` key in config file is now used for extending other config files.
```

## Semantic Versioning Relation

Conventional Commits align closely with [Semantic Versioning](https://semver.org/), allowing automated versioning updates based on commit messages:

- **MAJOR (x.0.0)**: Incremented for breaking changes (`feat!`, `fix!`, etc.).
    
- **MINOR (0.x.0)**: Incremented for new features (`feat`).
    
- **PATCH (0.0.x)**: Incremented for bug fixes (`fix`).
    

This structured approach ensures that version numbers reflect the nature of changes, helping teams maintain backward compatibility and predictability.

## Examples

### Basic Commit

```
feat(user): add user profile page
```

### Commit with Scope

```
fix(parser): resolve issue with space handling
```

### Commit with Breaking Change

```
chore!: drop support for Node 6

BREAKING CHANGE: Uses JavaScript features not available in Node 6.
```

### Commit Reverting a Change

```
revert: let us never again speak of the noodle incident

Refs: 676104e, a215868
```

## Benefits of Conventional Commits

- **Automates changelog generation**.
    
- **Facilitates semantic versioning**.
    
- **Improves collaboration and transparency**.
    
- **Simplifies build and deployment processes**.
    
- **Enhances project contribution by maintaining structured history**.
    

## Summary

Conventional Commits provide a clear and efficient way to track changes, ensuring consistency and clarity in project management. By following this format, teams can maintain better commit hygiene, improve automation, and simplify versioning and changelog management.