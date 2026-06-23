# Testing Patterns and Conventions

## Overview
DevFlow AI uses a multi-layered testing strategy to ensure reliability and performance.

## Testing Stack
- **Unit Testing**: [Vitest](https://vitest.dev/)
- **E2E Testing**: [Playwright](https://playwright.dev/)
- **CI/CD**: GitHub Actions

## Structure
- Unit tests should be located next to the source code they test, with the `.test.ts` or `.spec.ts` extension.
- E2E tests are located in the `tests/e2e` directory.

## Running Tests
### Unit Tests
```bash
npm run test
```

### E2E Tests
```bash
npm run test:e2e
```

## Conventions
- Use `describe` blocks to group related tests.
- Use `it` or `test` for individual test cases.
- Mock external dependencies (APIs, databases) in unit tests.
- E2E tests should cover critical user journeys.
- All Pull Requests must pass the CI pipeline (lint, type-check, tests).
