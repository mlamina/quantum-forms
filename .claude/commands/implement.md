# Implement Feature

Execute a planned feature implementation based on a GitHub issue specification, following the project's established patterns and guidelines.

## Overview

This command implements a feature that has been planned and documented in a GitHub issue, using the TodoWrite tool for task management and following the codebase's existing conventions and patterns.

## Implementation Process

### 1. Issue Analysis
- Retrieve and review the GitHub issue specification
- Understand the technical requirements and user stories
- Identify the implementation plan and task breakdown
- Review acceptance criteria and testing requirements

### 2. Task Planning with TodoWrite
Use the TodoWrite tool to create a comprehensive task list:
- Break down the implementation into specific, actionable tasks
- Include setup, development, testing, and verification steps
- Mark dependencies between tasks
- Track progress throughout implementation

### 3. Codebase Understanding
Before implementing:
- Search for existing related functionality and patterns
- Understand the project's conventions and structure
- Identify integration points and dependencies
- Review similar implementations for consistency

### 4. Branch Creation and Setup
Before implementation:
- Create a new feature branch with descriptive name
- Push branch to remote for tracking
- Set up branch for atomic commits throughout implementation

### 5. Implementation Execution
Follow the established development workflow:
- Implement features following existing code patterns
- Use established libraries and utilities
- Follow naming conventions and code style
- Ensure security best practices
- Make atomic commits for each logical change
- Push commits regularly so progress can be tracked on GitHub

### 6. Testing and Verification
- Write tests following the project's testing patterns
- Run existing test suites to ensure no regressions
- Verify acceptance criteria are met
- Test edge cases and error scenarios

### 7. Code Quality Checks
Run project-specific quality checks:
- Lint and typecheck commands (if available)
- Build processes to ensure compilation
- Format code according to project standards
- Ensure all TodoWrite tasks are completed

## Git Workflow and Branch Management

**Branch Creation:**
```bash
# Create feature branch with descriptive name based on issue
git checkout -b feature/issue-123-add-email-notifications
git push -u origin feature/issue-123-add-email-notifications
```

**Atomic Commits:**
- Make small, logical commits for each change
- Use descriptive commit messages referencing the issue
- Push commits regularly for progress tracking
- Format: `feat: add email notification system (#123)`

**Example Commit Flow:**
```bash
# After each logical change
git add .
git commit -m "feat: add email notification models (#123)"
git push

# Continue for each atomic change
git commit -m "feat: implement email sending service (#123)"
git push

git commit -m "test: add email notification tests (#123)"
git push
```

## GitHub Integration

**Issue Retrieval:**
```bash
# Use GitHub MCP to fetch issue details
mcp__github__get_issue(owner="arc-eng", repo="podcast", issue_number=X)
```

**Implementation Tracking:**
- Reference the GitHub issue in commits using (#issue_number)
- Update issue with implementation progress
- Create pull request when implementation is complete
- Link pull requests to the original issue

## TodoWrite Integration

**Task Management:**
- Create comprehensive task lists at the start
- Mark tasks as in_progress when starting work
- Complete tasks immediately when finished
- Add new tasks if discovered during implementation

**Example Task Structure:**
```
1. Analyze GitHub issue requirements
2. Create feature branch and push to remote
3. Research existing patterns in codebase
4. Set up database migrations (if needed)
5. Implement core functionality (commit and push)
6. Add error handling and validation (commit and push)
7. Write unit tests (commit and push)
8. Write integration tests (commit and push)
9. Update documentation (commit and push)
10. Run quality checks
11. Create pull request
12. Verify acceptance criteria
```

## Development Guidelines

**Code Conventions:**
- Follow existing patterns and conventions
- Use established libraries and utilities
- Maintain consistent naming and structure
- Add proper error handling and validation

**UI Development (if applicable):**
- Use `page-loader` class for buttons that trigger long page loads
- Add `btn` class to all buttons for proper styling
- Build CSS with: `npx tailwindcss -i ./static/css/tailwind.css -o ./static/css/output.css --minify`
- Always include `static/css/output.css` in commits

**Security Considerations:**
- Never expose or log secrets and keys
- Follow authentication and authorization patterns
- Validate all user inputs
- Use secure coding practices

## Testing Strategy

**Test Discovery:**
- Check README or search codebase for testing approach
- Never assume specific test framework or scripts
- Ask user for test commands if unclear

**Test Coverage:**
- Unit tests for core functionality
- Integration tests for system interactions
- Edge case and error scenario testing
- Regression testing of existing functionality

## Quality Assurance

**Pre-Commit Checks:**
- Run lint commands: `npm run lint`, `ruff`, etc.
- Run typecheck commands: `npm run typecheck`, `mypy`, etc.
- Ensure all tests pass
- Verify build processes complete successfully

**Code Review Preparation:**
- Ensure code follows project patterns
- Add appropriate comments for complex logic
- Update relevant documentation
- Verify all acceptance criteria are met

## Command Structure

```bash
/implement "GitHub issue URL or description"
```

**Examples:**
```bash
/implement "https://github.com/arc-eng/podcast/issues/123"
/implement "Issue #456: Add email notification system"
/implement "Implement coaching session reminder feature as planned in issue #789"
```

## Best Practices

**Implementation Approach:**
- Start with understanding existing patterns
- Implement incrementally with frequent testing
- Use TodoWrite to track all tasks
- Follow the project's established conventions

**Quality Focus:**
- Test thoroughly before marking tasks complete
- Run quality checks throughout development
- Ensure backward compatibility
- Document any breaking changes

**Integration Awareness:**
- Consider impact on existing functionality
- Test integration points carefully
- Update related documentation
- Coordinate with dependent systems

## Notes

- Always use TodoWrite tool for task management
- Create feature branch at start of implementation
- Make atomic commits with descriptive messages referencing issue number
- Push commits regularly so progress can be tracked on GitHub
- Run lint/typecheck commands before completion
- Include `static/css/output.css` in commits for UI changes
- Reference GitHub issues in the `arc-eng/podcast` repository
- Ask for test commands if testing approach is unclear
- Create pull request when implementation is complete
- Mark all TodoWrite tasks as completed when finished

# The Implementation to Execute
Use the instructions above to implement the following feature or GitHub issue:
$ARGUMENTS