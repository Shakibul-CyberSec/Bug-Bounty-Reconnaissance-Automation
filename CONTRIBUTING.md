# Contributing to Bug Bounty Recon Pipeline

First off, thank you for considering contributing to this project! 🎉

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check existing issues. When creating a bug report, include:

- **Clear title and description**
- **Steps to reproduce** the issue
- **Expected behavior** vs actual behavior
- **System information** (OS, bash version, tool versions)
- **Log files** or error messages

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion:

- Use a **clear and descriptive title**
- Provide a **detailed description** of the proposed feature
- Explain **why this enhancement would be useful**
- Include **examples** if applicable

### Pull Requests

1. Fork the repository
2. Create a new branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Test thoroughly
5. Commit your changes (`git commit -m 'Add amazing feature'`)
6. Push to the branch (`git push origin feature/amazing-feature`)
7. Open a Pull Request

## Development Guidelines

### Bash Script Standards

- Use `set -euo pipefail` for error handling
- Quote all variables properly
- Avoid `eval` and dangerous constructs
- Use meaningful variable names
- Add comments for complex logic
- Follow existing code style

### Testing

- Test on Ubuntu 24.04 LTS minimum
- Test with various target types
- Verify resume functionality
- Check resource usage
- Test error conditions

### Documentation

- Update README.md if needed
- Add inline comments for complex code
- Update CHANGELOG.md
- Document new features/phases

### Commit Messages

- Use present tense ("Add feature" not "Added feature")
- Use imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit first line to 72 characters
- Reference issues and pull requests

Example:
```
Add parameter fuzzing phase

- Implement dalfox integration
- Add XSS detection
- Update documentation

Fixes #123
```

## Code of Conduct

### Our Pledge

We are committed to providing a welcoming and inspiring community for all.

### Our Standards

**Positive behavior includes:**
- Being respectful and inclusive
- Gracefully accepting constructive criticism
- Focusing on what's best for the community
- Showing empathy towards others

**Unacceptable behavior includes:**
- Trolling, insulting, or derogatory comments
- Public or private harassment
- Publishing others' private information
- Other unethical or unprofessional conduct

### Enforcement

Project maintainers have the right to remove, edit, or reject comments, commits, code, and other contributions that don't align with this Code of Conduct.

## Questions?

Feel free to open an issue with the `question` label or reach out to the maintainer.

---

Thank you for contributing! 🚀
