# reflect

Groom and optimize CLAUDE.md files in the root directory and all direct (first-level) subdirectories according to Claude Code best practices, using parallel subagents for efficient processing.

## Overview

This command analyzes and improves CLAUDE.md files across the project structure to ensure they follow best practices for Claude Code integration. It uses parallel subagents to process multiple directories simultaneously, making the grooming process efficient and comprehensive.

## Process

### 1. Directory Discovery
- Scan the root directory for existing CLAUDE.md file
- Identify all direct (first-level) subdirectories
- Filter subdirectories that contain meaningful code (exclude data/, media/, node_modules/, etc.)

### 2. Parallel Subagent Processing
Launch parallel subagents to process each directory:
- **Root directory**: Analyze and improve the main CLAUDE.md file
- **Each subdirectory**: Analyze existing CLAUDE.md or create new ones where beneficial

### 3. CLAUDE.md Content Analysis
Each subagent evaluates and improves:
- **Common bash commands** specific to the directory/app
- **Core files and utility functions** within the scope
- **Code style guidelines** relevant to the component
- **Testing instructions** for the specific module
- **Directory-specific warnings** or unexpected behaviors
- **Integration points** with other parts of the system

### 4. Best Practices Implementation
Apply Claude Code best practices:
- Keep content concise and human-readable
- Use clear, actionable language
- Include emphasis ("IMPORTANT", "YOU MUST") for critical instructions
- Structure with headers and bullet points
- Focus on information Claude needs to work effectively
- Remove outdated or redundant information

## Subagent Instructions

Each subagent should:

1. **Analyze the directory structure and purpose**
2. **Read existing CLAUDE.md file (if present)**
3. **Identify key files, patterns, and workflows**
4. **Determine directory-specific requirements**
5. **Create or improve CLAUDE.md content following best practices**
6. **Ensure consistency with project-wide conventions**

### Directory-Specific Focus Areas

**Root Directory (`/`):**
- Overall project setup and environment
- Main development workflows
- Cross-app dependencies and relationships
- Global configuration and settings

**Django Apps (`coaching/`, `podcasts/`, `client_portal/`, etc.):**
- App-specific models and business logic
- Testing patterns and commands
- API endpoints and views structure
- Template and static file organization

**Core Infrastructure (`core/`):**
- Django settings and configuration
- Middleware and global utilities
- Environment-specific setup

**Release Management (`releases/`):**
- Release process and workflows
- Email subscription management
- Deployment procedures

## Command Execution

```bash
/reflect
```

## Implementation Strategy

The command will:

1. **Use TodoWrite** to track progress across all subagents
2. **Launch parallel Task subagents** for each directory
3. **Coordinate subagent completion** before finalizing
4. **Provide summary** of changes made across all directories

### Subagent Task Template

Each subagent receives:
```
Analyze and improve the CLAUDE.md file for directory: {directory_path}

Directory purpose: {inferred_purpose}
Existing CLAUDE.md: {exists/does_not_exist}

Instructions:
1. Understand the directory's role in the project
2. Identify key files, patterns, and workflows
3. Create or improve CLAUDE.md following best practices
4. Ensure content is concise, actionable, and Claude-specific
5. Include directory-specific bash commands, code patterns, and warnings
6. Maintain consistency with project conventions
```

## Quality Criteria

Each CLAUDE.md file should:
- **Be immediately actionable** for Claude Code
- **Include relevant bash commands** with clear descriptions
- **Document code style and patterns** specific to the directory
- **Provide testing guidance** when applicable
- **Warn about directory-specific gotchas** or unexpected behaviors
- **Reference integration points** with other parts of the system
- **Follow consistent formatting** and structure

## Expected Outcomes

After running `/reflect`:
- All relevant directories have optimized CLAUDE.md files
- Content follows Claude Code best practices
- Directory-specific guidance is clear and actionable
- Cross-directory consistency is maintained
- Claude's effectiveness in each part of the codebase is improved

## Notes

- Focus on directories with substantial code, not just data or configuration
- Ensure each CLAUDE.md provides value specific to its directory context
- Maintain consistency with the project's overall development patterns
- Include references to the main project CLAUDE.md where appropriate
- Consider the directory's role in the larger application architecture

# Directory Analysis and Grooming Task

Use the instructions above to analyze and improve CLAUDE.md files across the project structure using parallel subagents for efficient processing.