# Rust Skills for Claude Code

This repository contains Claude Code skills for Rust development, based on best practices from "Effective Rust" by David Drysdale.

## Skills

### effective-rust.skill

A comprehensive skill that provides expert guidance on Rust programming patterns, idiomatic code, and best practices. The skill is organized into multiple resources for progressive loading, allowing Claude to load only the relevant sections when needed.

#### Resources:

1. **types** - Type system usage, Option/Result transforms, error types, and type conversions
2. **traits** - Standard traits, Drop for RAII, Deref vs AsRef, and borrowing patterns
3. **concepts** - Lifetimes, borrow checker, and state management
4. **dependencies** - Dependency graph management and avoiding feature creep
5. **tooling** - Clippy, rustfmt, and testing practices
6. **error-handling** - Advanced error handling patterns and libraries
7. **performance** - Profiling, benchmarking, and optimization techniques
8. **concurrency** - Threading, async/await, and synchronization primitives

#### When to Use:

Load this skill when:
- Working on Rust projects
- Reviewing Rust code implementations
- Seeking guidance on Rust best practices
- Debugging borrow checker errors
- Optimizing Rust code performance
- Implementing concurrent or async code

Each resource has a clear description of its scope and when it should be loaded, enabling progressive loading for efficient context management.

## Skill Format

The skill follows the Claude Code skill format with:
- Clear `name` identifier
- Detailed `description` with functionality and boundaries
- `resources` array with individual chapters/topics
- Each resource has its own `name`, `description`, and `content`
- Descriptions clearly state when each resource should be loaded

This structure enables Claude to determine whether to load the skill and which specific resources are relevant for the current task.