# Repository Guidelines

## Project Structure & Module Organization

This repository is currently empty. When adding code, keep the layout predictable and grouped by responsibility. Use `src/` for application source, `tests/` for automated tests, `docs/` for contributor-facing documentation, and `assets/` for static files such as images, fixtures, or sample data.

Example layout:

```text
src/
tests/
docs/
assets/
```

Keep modules small and cohesive. Place shared helpers in a clearly named utility module rather than duplicating logic across feature folders.

## Build, Test, and Development Commands

No build or test tooling is defined yet. Add commands to this section when package files or task runners are introduced.

Common examples:

```sh
npm install        # Install JavaScript dependencies
npm test           # Run JavaScript tests
pytest             # Run Python tests
make build         # Build using a Makefile target
```

Prefer documenting commands that work from the repository root. If setup requires environment variables, include a minimal example in `.env.example` rather than committing secrets.

## Coding Style & Naming Conventions

Follow the conventions of the language and framework introduced to the repository. Use consistent indentation across each language, descriptive file names, and clear module boundaries.

Recommended defaults:

- Use `snake_case` for Python files and functions.
- Use `camelCase` for JavaScript or TypeScript variables and functions.
- Use `PascalCase` for classes, React components, and exported types.
- Keep configuration files at the repository root when they apply project-wide.

Add formatter and linter commands here once tools such as Prettier, ESLint, Ruff, Black, or gofmt are configured.

## Testing Guidelines

Place tests under `tests/` or beside source files using the project’s framework conventions. Name tests after the behavior under test, not implementation details.

Examples:

- Python: `tests/test_user_service.py`
- JavaScript/TypeScript: `user-service.test.ts`

Each feature should include coverage for expected behavior and important failure cases. Document any integration test prerequisites, such as databases or external services.

## Commit & Pull Request Guidelines

No Git history is available in this directory, so no existing commit convention can be inferred. Until one is established, use concise imperative commit messages, for example `Add user settings validation`.

Pull requests should include a short summary, test results, and any relevant screenshots or logs for user-facing changes. Link related issues when available and call out migrations, configuration changes, or operational risks.

## Security & Configuration Tips

Do not commit secrets, local credentials, generated private keys, or machine-specific configuration. Use ignored local environment files for private values and provide safe examples through `.env.example` or documentation.
