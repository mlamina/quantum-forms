# Plan Code Change

Create a comprehensive planning document and GitHub issue for a proposed code change using systematic research and specification generation.

## Overview

This command analyzes a code change request, conducts research using subagents to understand requirements, creates a detailed specification with user stories, and generates a GitHub issue for tracking.

## Steps

### 1. Initial Analysis
1. Break down the change request into key components
2. Identify affected systems, files, and dependencies
3. Determine research areas needed for complete understanding

### 2. Research Phase
Use subagents to conduct specific research tasks:

**Codebase Analysis:**
- Search for existing related functionality
- Identify patterns and conventions to follow
- Map dependencies and integration points
- Review similar implementations for consistency

**Technical Requirements:**
- Analyze technical constraints and considerations
- Identify potential challenges or risks
- Research best practices for the proposed change
- Review testing requirements and strategies

**User Impact Assessment:**
- Understand user workflows affected
- Identify edge cases and error scenarios
- Consider backward compatibility requirements
- Assess performance implications

### 3. Specification Creation
Generate a comprehensive specification including:

**Technical Specification:**
- Detailed implementation approach
- Architecture decisions and rationale
- API changes or new endpoints
- Database schema modifications (if any)
- Security considerations

**User Stories:**
- Primary user workflows
- Edge case scenarios
- Error handling requirements
- Success criteria and acceptance tests

**Implementation Plan:**
- Break down into logical phases
- Identify dependencies between tasks
- Estimate complexity and effort
- Define testing strategy

### 4. GitHub Issue Creation
Create a GitHub issue with:
- Clear title summarizing the change
- Comprehensive description with context
- Technical specification details
- User stories and acceptance criteria
- Implementation plan with task breakdown
- Labels for categorization
- Milestone assignment (if applicable)

## Research Guidelines

**Subagent Tasks:**
- Keep research focused and specific
- Document findings clearly with file references
- Include code examples where relevant
- Note any blockers or dependencies discovered

**Documentation:**
- Reference specific files and line numbers
- Include relevant existing patterns
- Note any breaking changes required
- Document integration touchpoints

## Issue Template Structure

```markdown
## Overview
[Brief description of the change and its purpose]

## User Stories
- As a [user type], I want [functionality] so that [benefit]
- [Additional user stories...]

## Technical Specification
### Implementation Approach
[Detailed technical approach]

### Architecture Changes
[Any architectural modifications needed]

### Security Considerations
[Security implications and requirements]

## Implementation Plan
### Phase 1: [Description]
- [ ] Task 1
- [ ] Task 2

### Phase 2: [Description]
- [ ] Task 3
- [ ] Task 4

## Testing Strategy
[How the change will be tested]

## Dependencies
[External dependencies or blockers]

## Acceptance Criteria
- [ ] Criteria 1
- [ ] Criteria 2
```

## Notes

- Use multiple subagents for parallel research when possible
- Focus on understanding existing patterns before proposing new ones
- Always consider backward compatibility and migration strategies
- Include performance and security implications in all plans
- Link to relevant documentation or existing issues when applicable
- Tag appropriate team members for review when creating the issue

# The Code Change to Plan
Use the instructions above to create a plan for the following code change:
$ARGUMENTS