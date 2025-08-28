# Contributing Guidelines

Thank you for your interest in contributing to the Sign Board Detection project! We welcome contributions from the community to help improve the application and make road sign detection more accessible.

## Code of Conduct

Please note that this project is released with a Contributor Code of Conduct. By participating in this project you agree to abide by its terms:

- Be respectful and inclusive
- Be collaborative and helpful
- Focus on what is best for the community
- Show empathy towards other community members

## How to Contribute

### Reporting Bugs

Before submitting a bug report, please check if the issue has already been reported. If not, create a new issue with:

1. A clear and descriptive title
2. Steps to reproduce the issue
3. Expected vs. actual behavior
4. Screenshots or videos if applicable
5. Device information and Android version
6. App version where the bug occurred

### Suggesting Enhancements

Feature requests are welcome! Please create an issue with:

1. A clear and descriptive title
2. Detailed explanation of the proposed feature
3. Use cases for the feature
4. Potential implementation approaches (if you have ideas)

### Code Contributions

#### Development Workflow

1. Fork the repository
2. Clone your fork:
   ```bash
   git clone https://github.com/yourusername/road-sign-detection.git
   ```
3. Create a feature branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
4. Make your changes
5. Write or update tests as needed
6. Ensure your code follows the style guidelines
7. Commit your changes:
   ```bash
   git commit -m "Add feature: brief description"
   ```
8. Push to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```
9. Create a Pull Request

#### Pull Request Guidelines

- Keep PRs focused on a single feature or bug fix
- Write a clear description of the changes
- Reference any related issues
- Ensure all tests pass
- Update documentation as needed
- Follow the existing code style

### Style Guidelines

#### Kotlin Coding Standards

- Follow [Kotlin Coding Conventions](https://kotlinlang.org/docs/coding-conventions.html)
- Use descriptive variable and function names
- Keep functions small and focused
- Use extension functions appropriately
- Leverage Kotlin's null safety features

#### Android Development Best Practices

- Follow Material Design guidelines
- Implement proper lifecycle management
- Handle permissions correctly
- Optimize for different screen sizes
- Ensure accessibility compliance

#### Code Structure

- Organize code into logical packages
- Use meaningful class and method names
- Comment complex logic
- Remove unused imports and code
- Maintain consistent indentation

### Testing

#### Types of Tests

1. **Unit Tests**: Test individual components in isolation
2. **Instrumented Tests**: Test UI components and integration
3. **Performance Tests**: Ensure optimal performance

#### Writing Tests

- Place unit tests in `src/test/`
- Place instrumented tests in `src/androidTest/`
- Use descriptive test method names
- Follow the AAA pattern (Arrange, Act, Assert)
- Test both positive and negative cases

### Documentation

When adding new features or modifying existing ones:

1. Update README.md if needed
2. Add or modify documentation in the docs/ directory
3. Update code comments for complex logic
4. Add Javadoc/KDoc for public APIs

## Development Setup

See [Getting Started Guide](GETTING_STARTED.md) for detailed setup instructions.

## Code Review Process

All submissions require review. We use GitHub pull requests for this process. After submitting a PR:

1. A maintainer will review your code
2. Feedback will be provided
3. Address any requested changes
4. Once approved, your code will be merged

## Community

- Join our discussions in the Issues section
- Help answer questions from other developers
- Share your experiences and use cases
- Contribute to documentation improvements

## Recognition

Contributors will be recognized in:

- Release notes
- Contributor list in documentation
- GitHub contributors graph

Thank you for helping make Sign Board Detection better!