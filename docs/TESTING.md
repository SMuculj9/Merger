# Bundus DNA Platform - Testing Guide

## Overview

The Bundus DNA Platform implements comprehensive testing across multiple layers: unit tests, component tests, integration tests, and end-to-end tests.

## Testing Philosophy

### Core Principles

1. **Test-Driven Development**: Write tests before implementation
2. **Accessibility Testing**: Ensure all features work for all users
3. **Data Integrity**: Verify genetic data processing accuracy
4. **User Workflows**: Test complete user journeys
5. **Performance**: Ensure tests don't hide performance issues

## Testing Stack

### Unit Testing
- **Framework**: Jest
- **Coverage Target**: 80% minimum
- **Location**: `__tests__` directories or `.test.ts(x)` files

### Component Testing
- **Framework**: React Testing Library
- **Focus**: User behavior, not implementation details

### Integration Testing
- **Framework**: Jest with @testing-library/react
- **Focus**: Component interactions and data flow
- **Location**: `tests/integration/`

### End-to-End Testing
- **Framework**: Cypress or Playwright
- **Focus**: Complete user journeys
- **Location**: `tests/e2e/`

## Running Tests

```bash
npm test
npm run test:watch
npm test -- --coverage
npm run test:e2e
```

## Coverage Requirements

- **Statements**: ≥80%
- **Branches**: ≥75%
- **Functions**: ≥80%
- **Lines**: ≥80%

## Critical: data-testid Attributes

ALL interactive and informational elements MUST include `data-testid` attributes in kebab-case:

```jsx
<button data-testid="upload-dna-button">Upload DNA</button>
<input data-testid="trait-search-input" />
<div data-testid="chromosome-ideogram" />
```

---

**Last Updated**: June 5, 2026
**Version**: 1.0
