# Git Ignore Strategy

## Key Principles

- Patterns are recursive by default
- Avoid inline comments in `.gitignore`
- Keep rules minimal and explicit
- Never rely on `.gitignore` for already-tracked files

## Common Patterns

| Pattern        | Meaning |
|----------------|--------|
| target/        | Ignore Rust build artifacts |
| node_modules/  | Ignore Node dependencies |
| *.log          | Ignore logs anywhere |

## Gotchas

- `.gitignore` does NOT remove tracked files
- Use `git rm --cached` to untrack
- Use `git check-ignore -v <file>` to debug

## Environment Files

- `.env` → ignored
- `.env.example` → should be committed
