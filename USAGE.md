# Usage Guide for Effective Rust Skill

## Overview

The `effective-rust.skill` file is designed for use with Claude Code to provide contextual Rust best practices and guidance. The skill uses progressive loading, meaning Claude will only load the relevant resources when needed.

## Progressive Loading

The skill description clearly states when to load it:
> Load when working with Rust code, reviewing Rust implementations, or seeking guidance on Rust best practices and idiomatic patterns.

Each resource within the skill has its own description that helps Claude determine if it should be loaded:

### Resource Loading Triggers

- **types**: Load when working with Rust types, designing APIs, or implementing error handling
- **traits**: Load when implementing traits, designing abstractions, or working with smart pointers and RAII patterns
- **concepts**: Load when debugging borrow checker errors, working with complex lifetime scenarios, or designing concurrent systems
- **dependencies**: Load when adding dependencies, optimizing build times, or reviewing crate dependencies
- **tooling**: Load when setting up Rust projects, establishing code quality standards, or configuring CI/CD
- **error-handling**: Load when implementing error handling, designing error types, or working with Result types
- **performance**: Load when optimizing performance, profiling code, or investigating performance issues
- **concurrency**: Load when implementing concurrent code, working with async Rust, or debugging race conditions

## Example Scenarios

### Scenario 1: Implementing a New Feature
When you're implementing a new Rust feature, Claude might load:
- `types` - for proper type design
- `error-handling` - for handling errors idiomatically
- `tooling` - for ensuring code quality with Clippy and tests

### Scenario 2: Performance Optimization
When optimizing code, Claude might load:
- `performance` - for profiling and optimization techniques
- `concurrency` - if parallelization is relevant

### Scenario 3: Code Review
When reviewing Rust code, Claude might load:
- All resources as needed based on the code being reviewed
- `tooling` - to ensure proper Clippy and rustfmt usage
- `traits` - to verify proper trait implementation

## Skill Structure Benefits

1. **Clear Boundaries**: Each resource clearly defines its scope
2. **Efficient Loading**: Only relevant content is loaded
3. **Comprehensive Coverage**: Covers all major aspects of Rust best practices
4. **Actionable Guidance**: Includes code examples and specific recommendations
5. **Tool Integration**: References standard Rust tools (Clippy, rustfmt, cargo)

## Extending the Skill

To add new resources:

1. Add a new resource to the `resources` array
2. Include a clear `name` identifier
3. Write a detailed `description` with:
   - What the resource covers
   - When it should be loaded
   - Clear boundaries of its scope
4. Provide comprehensive `content` with examples

## File Format

The skill file uses YAML format with this structure:

```yaml
name: skill-identifier
description: |
  Overall skill description
  Scope and boundaries
  When to load this skill

resources:
  - name: resource-name
    description: |
      Resource description
      Load when: specific scenarios
    content: |
      # Resource content in Markdown
      Detailed information with examples
```

This format allows Claude Code to make informed decisions about when to load the skill and which resources are most relevant for the current task.
