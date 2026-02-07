# Contributing to Suraksha Kavach

Thank you for your interest in contributing to Suraksha Kavach, a women's safety application.

## Project Overview

Suraksha Kavach is an emergency response application aligned with UN SDG 5 (Gender Equality).
This project aims to provide reliable, accessible safety tools for individuals in emergency situations.

## How to Contribute

### Reporting Issues

If you encounter a bug or have a feature request:

1. Check if the issue already exists in the issue tracker
2. If not, create a new issue with:
   - Clear, descriptive title
   - Detailed description of the problem or feature
   - Steps to reproduce (for bugs)
   - Expected vs actual behavior
   - Device/Android version information
   - Screenshots if applicable

### Submitting Code

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature-name`)
3. Make your changes following our coding standards
4. Write/update tests as needed
5. Ensure all tests pass
6. Commit with clear, descriptive messages
7. Push to your fork
8. Submit a pull request

### Coding Standards

#### Kotlin Style Guide

- Follow [Kotlin Coding Conventions](https://kotlinlang.org/docs/coding-conventions.html)
- Use meaningful variable and function names
- Keep functions small and focused
- Document public APIs with KDoc
- Include copyright headers in all source files

#### Code Documentation

All classes, functions, and properties should include:
```kotlin
/**
 * Brief description of the component.
 * 
 * Detailed explanation if needed, including:
 * - Purpose and usage
 * - Important notes or warnings
 * - Examples if helpful
 * 
 * @param paramName Description of parameter
 * @return Description of return value
 * @throws ExceptionType When this exception is thrown
 */
```

#### Copyright Headers

All source files must include:
```kotlin
/*
 * Copyright (c) 2026 Megha Dey. All rights reserved.
 *
 * Licensed under the Apache License, Version 2.0 (the "License");
 * you may not use this file except in compliance with the License.
 */
```

### Testing

- Write unit tests for new functionality
- Ensure existing tests continue to pass
- Test on multiple Android versions (API 24-34)
- Test on different device sizes and configurations

### Commit Messages

Use clear, descriptive commit messages:

```
Add emergency contact validation

- Implement phone number format validation
- Add name length constraints
- Update error messaging

Fixes #123
```

### Pull Request Guidelines

- Reference related issues
- Provide clear description of changes
- Include screenshots for UI changes
- Ensure all checks pass
- Respond to review feedback promptly

## Development Setup

1. Install Android Studio Hedgehog (2023.1.1) or later
2. Clone the repository
3. Open project in Android Studio
4. Sync Gradle files
5. Run on emulator or physical device (API 24+)

## Code Review Process

1. All submissions require review
2. Maintainers will provide feedback
3. Address feedback in your branch
4. Once approved, changes will be merged

## Areas for Contribution

### High Priority
- Internationalization (i18n) support
- Accessibility improvements
- Performance optimization
- Test coverage expansion

### Medium Priority
- UI/UX enhancements
- Additional safety features
- Documentation improvements
- Code quality improvements

### Low Priority
- Code style consistency
- Minor bug fixes
- Dependency updates

## Security

If you discover a security vulnerability:
1. **Do not** create a public issue
2. Email project maintainers directly
3. Provide detailed information
4. Allow time for patch development before disclosure

## Recognition

Contributors will be acknowledged in:
- Project README
- Release notes
- Contributors list

## Questions?

- Review existing documentation
- Check closed issues for similar questions
- Open a discussion thread

## License

By contributing, you agree that your contributions will be licensed under
the Apache License 2.0.

---

**Suraksha Kavach - Women's Safety Application**  
Copyright © 2026 Megha Dey. All Rights Reserved.

Thank you for helping make the digital world safer!
