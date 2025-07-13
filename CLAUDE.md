# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Python Project Template

This is a template repository for Python-based projects with standardized tooling and development practices.

## Quick Start Commands

```bash
# Initial setup with Poetry
poetry install

# Run tests
poetry run pytest

# Run tests with coverage
poetry run pytest --cov=.

# Lint code
poetry run ruff check .

# Format code
poetry run ruff format .

# Type checking
poetry run mypy .
```

## Environment Variables

Common environment variables for Python projects:
- `DEBUG`: Set to 'true' for development mode
- `SECRET_KEY`: Application secret key for security
- `DATABASE_URL`: Database connection string

## Development Guidelines

### Code Quality Standards
- Use Poetry for dependency management
- Follow PEP 8 style guidelines with Ruff
- Include type hints and use mypy for type checking
- Maintain test coverage with pytest
- Use pytest fixtures for test data

### Testing Strategy
```bash
# Run all tests
poetry run pytest

# Run specific test file
poetry run pytest tests/test_example.py

# Run tests with coverage report
poetry run pytest --cov=. --cov-report=html
```

### Project Structure
```
├── src/                    # Source code
│   └── package_name/       # Main package
├── tests/                  # Test files
├── docs/                   # Documentation
├── pyproject.toml          # Poetry configuration
├── README.md               # Project documentation
└── .env.example           # Environment variables template
```

## Common Development Tasks

### Adding New Dependencies
```bash
# Add production dependency
poetry add package_name

# Add development dependency
poetry add --group dev package_name
```

## Git & Deployment Best Practices
- Never commit secrets or API keys
- Use environment variables for configuration
- Include comprehensive test coverage
- Run linting and tests before commits

## Claude Code Specific Guidelines

### File Operations
- Prefer editing existing files over creating new ones
- Never create documentation files unless explicitly requested
- Always run tests and linting after code changes

### GitHub Integration
- Use GitHub MCP server for issue management
- Always start GitHub issue titles with an emoji
- Include hyperlinks when creating issues

### Command Configuration
- All Claude Code commands are defined in `.claude/commands/`
- Hooks for automation are in `.claude/hooks/`
- Settings are configured in `.claude/settings.local.json`

## Troubleshooting

### Common Issues
- **Import errors**: Check package installation with `poetry show`
- **Test failures**: Run `poetry run pytest -v` for verbose output
- **Linting errors**: Use `poetry run ruff check --fix .` for auto-fixes
- **Type errors**: Run `poetry run mypy .` for detailed type checking

### Development Environment
- Use virtual environments (Poetry handles this automatically)
- Keep dependencies up to date with `poetry update`
- Use `.env` files for local configuration (never commit these)

## Project Specifics

### Quantum Forms Project Structure
- This project is implemented as a single page in index.html
- All data for the page is stored in a single JSON file under @quantum_curriculum_complete.json