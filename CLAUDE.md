# CLAUDE.md

This file provides guidance to AI assistants (Claude and others) working on the **jirman** repository. Keep this document updated as the project evolves.

---

## Project Overview

- **Repository**: `jirman-ludek/jirman`
- **Status**: Project initialization phase — no source files exist yet.
- **Purpose**: _(To be defined once project goals are established.)_

> **Note for AI assistants**: This repository was empty at the time this file was created. As files and structure are added, update the relevant sections below to reflect the actual codebase.

---

## Repository Structure

```
jirman/
└── CLAUDE.md          # This file — AI assistant guidance
```

_Update this tree as the project structure is established._

---

## Development Setup

### Prerequisites

_(List required runtimes, tools, and versions once the stack is chosen, e.g.:)_

```
Node.js >= 20
Python >= 3.11
Go >= 1.22
Docker >= 24
```

### Initial Setup

```bash
# Clone the repository
git clone <repo-url>
cd jirman

# Install dependencies
# (fill in the correct command once the stack is chosen)
# npm install | pip install -r requirements.txt | go mod download
```

### Environment Variables

Copy the example environment file and fill in values:

```bash
cp .env.example .env
```

_(Document required environment variables here when they are defined.)_

---

## Common Commands

Fill in the correct commands once the toolchain is established.

| Task | Command |
|------|---------|
| Install dependencies | `<fill in>` |
| Start dev server | `<fill in>` |
| Run tests | `<fill in>` |
| Run linter | `<fill in>` |
| Format code | `<fill in>` |
| Build for production | `<fill in>` |
| Database migrations | `<fill in>` |

---

## Git Workflow

### Branch Naming

| Type | Pattern | Example |
|------|---------|---------|
| Feature | `feature/<short-description>` | `feature/user-authentication` |
| Bug fix | `fix/<short-description>` | `fix/login-redirect-loop` |
| Chore / tooling | `chore/<short-description>` | `chore/update-dependencies` |
| AI-assisted work | `claude/<task-id>` | `claude/claude-md-mm6kvbjsthtqau95-qKJHN` |

### Commit Messages

Follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <short description>

[optional body]

[optional footer]
```

**Types**: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`, `perf`, `ci`

**Examples**:
```
feat(auth): add JWT-based login endpoint
fix(api): handle empty payload in POST /items
docs: update CLAUDE.md with dev setup instructions
```

### Pull Request Process

1. Branch off `main` (or the designated base branch).
2. Make focused, atomic commits.
3. Open a PR with a clear title and description.
4. Ensure all CI checks pass before requesting review.
5. Squash-merge into `main` after approval.

---

## Code Style & Conventions

_(Fill in once the language/framework is chosen.)_

### General Rules

- Prefer clarity over cleverness.
- Keep functions small and single-purpose.
- Write tests alongside new functionality.
- Do not commit secrets, credentials, or `.env` files.

### Language-Specific

_(Add sections as the tech stack is defined, e.g.:)_

#### TypeScript / JavaScript
```
- ESLint + Prettier enforced via pre-commit hooks
- Strict TypeScript mode enabled
- Prefer named exports over default exports
```

#### Python
```
- Black + isort for formatting
- Ruff for linting
- Type hints required for public functions
```

#### Go
```
- gofmt for formatting
- golangci-lint for linting
- Errors wrapped with context: fmt.Errorf("doing X: %w", err)
```

---

## Testing

_(Fill in once a testing framework is chosen.)_

- Write tests for all new features and bug fixes.
- Aim for meaningful coverage, not 100% line coverage at the expense of test quality.
- Unit tests should be fast and not require external services.
- Integration/e2e tests may use Docker Compose to spin up dependencies.

---

## CI / CD

_(Document the CI pipeline once it is configured.)_

Expected pipeline stages:
1. Lint
2. Type-check
3. Unit tests
4. Integration tests
5. Build
6. Deploy (on merge to `main`)

---

## Architecture Notes

_(Document key architectural decisions here as they are made.)_

Use this section to record important design choices, trade-offs considered, and the reasoning behind them. This helps future contributors (human and AI) understand *why* the code is structured the way it is.

Example format:
```
### ADR-001: Choice of database
Date: YYYY-MM-DD
Decision: Use PostgreSQL
Reason: Strong JSONB support, mature ecosystem, familiar to the team.
Alternatives considered: MySQL, MongoDB
```

---

## AI Assistant Guidelines

When working in this repository, AI assistants should:

1. **Read before writing** — always read existing files before modifying them.
2. **Stay focused** — only make changes directly related to the task at hand. Avoid refactoring unrelated code.
3. **Keep it simple** — prefer the simplest solution that satisfies requirements. Avoid over-engineering.
4. **No secrets** — never commit credentials, API keys, or sensitive data.
5. **Test your changes** — run the test suite after making changes and fix any failures before committing.
6. **Update docs** — if a change affects the project structure, commands, or conventions, update this CLAUDE.md accordingly.
7. **Commit clearly** — use Conventional Commits format (see Git Workflow above).
8. **Branch discipline** — develop on the designated branch and push only to that branch unless explicitly permitted otherwise.
9. **Ask when uncertain** — if a requirement is ambiguous or a decision has significant consequences, surface the uncertainty rather than guessing.
10. **No backwards-compat hacks** — do not add shims, re-exports, or compatibility layers for removed code. Delete unused code cleanly.

---

## Updating This File

This document should be kept current. When you make a change that affects:

- Project structure → update the **Repository Structure** section.
- Toolchain / commands → update **Common Commands**.
- Code conventions → update **Code Style & Conventions**.
- Architecture decisions → add an entry to **Architecture Notes**.

Treat CLAUDE.md as living documentation.
