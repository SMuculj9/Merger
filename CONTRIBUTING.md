# Contributing to Bundus DNA Platform

Thank you for your interest in contributing to the Bundus DNA Platform! This document provides guidelines and instructions for contributing.

## Code of Conduct

Be respectful, inclusive, and professional in all interactions.

## Getting Started

1. Fork the repository
2. Clone your fork locally
3. Create a feature branch: `git checkout -b feature/your-feature-name`
4. Make your changes
5. Commit with clear messages: `git commit -m "Add feature: description"`
6. Push to your fork: `git push origin feature/your-feature-name`
7. Create a Pull Request

## Development Setup

```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Run tests
npm run test

# Run linter
npm run lint
```

## Code Standards

### TypeScript/JavaScript
- Use TypeScript for new code
- Follow ESLint configuration
- Format code with Prettier
- Use meaningful variable names
- Write JSDoc comments for functions

### React Components
- Use functional components with hooks
- Include `data-testid` attributes on interactive elements
- Follow the component naming conventions
- Keep components focused and single-responsibility

### CSS/Tailwind
- Use Tailwind utility classes
- Follow the design guidelines
- Maintain color consistency
- Test responsive designs (mobile, tablet, desktop)

### Python
- Follow PEP 8 style guide
- Use type hints
- Include docstrings
- Write unit tests

## Testing Requirements

- All interactive elements must have `data-testid` attributes
- Unit tests required for new functions
- Component tests required for new React components
- E2E tests for critical user flows
- Minimum 80% code coverage

## Design Guidelines Compliance

- Follow the established design system
- Use only approved colors from design_guidelines.json
- Maintain consistent typography (Chivo, IBM Plex Sans, IBM Plex Mono)
- Implement "Control Room" dense grid layouts
- No glassmorphism on dashboards

## Commit Messages

Use clear, descriptive commit messages:

```
[type]: Brief description

Optional longer explanation with details about:
- What changed
- Why it changed
- Any breaking changes

type: feat (feature), fix (bug fix), docs, style, refactor, test, chore
```

Examples:
```
feat: Add chromosome ideogram visualization
fix: Correct ancestry map color scheme
docs: Update authentication guide
```

## Pull Request Process

1. Update README.md with any new features or changes
2. Update CHANGELOG.md
3. Ensure all tests pass: `npm run test`
4. Ensure code is formatted: `npm run format`
5. Request review from maintainers
6. Address review feedback
7. Squash commits if requested
8. Maintainer merges when approved

## Reporting Issues

When reporting bugs, include:
- Clear description of the issue
- Steps to reproduce
- Expected behavior
- Actual behavior
- Screenshots/videos if applicable
- Environment (OS, browser, versions)

## Feature Requests

When suggesting features:
- Describe the use case
- Explain the expected behavior
- Provide examples if possible
- Consider design and performance implications

## Documentation

- Update docs for any new features
- Keep README.md current
- Add comments to complex code
- Update API documentation
- Include examples in docstrings

## Need Help?

- Check existing issues and discussions
- Review documentation
- Ask in pull request comments
- Contact maintainers

---

Thank you for contributing to the Bundus DNA Platform!