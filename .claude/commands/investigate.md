# Investigate Issue

Use the zen tracer MCP tool to systematically investigate an issue or observation through structured code analysis and tracing.

## Overview

This command provides a methodical approach to investigating bugs, performance issues, unexpected behavior, or code observations using the zen tracer tool's step-by-step workflow with expert analysis.

## Investigation Process

### 1. Issue Characterization
- Clearly define the issue or observation
- Identify symptoms and expected vs actual behavior
- Gather relevant context (error messages, logs, user reports)
- Determine the scope and impact of the issue

### 2. Zen Tracer Investigation
Use the `mcp__zen__tracer` tool with the following approach:

**Trace Mode Selection:**
- `precision`: For method/function execution flow analysis
- `dependencies`: For class/module structural relationships
- `ask`: Let the tool recommend the best mode

**Investigation Strategy:**
- Start with step 1: describe investigation plan and target
- Use systematic code examination between each step
- Document findings with concrete evidence
- Build comprehensive understanding through iterations
- Follow the tool's required_actions for investigation guidance

### 3. Evidence Collection
During each investigation step:
- Examine relevant files and code paths
- Trace execution flows and call chains
- Map dependencies and relationships
- Document unexpected behaviors or patterns
- Note potential root causes

### 4. Analysis and Conclusions
- Synthesize findings from all investigation steps
- Identify root cause(s) based on evidence
- Assess impact and severity
- Recommend next steps or solutions

## Zen Tracer Usage Guidelines

**Initial Setup:**
```
target_description: "Detailed description of what to investigate and WHY"
trace_mode: "ask" | "precision" | "dependencies"
step: "Investigation plan and target analysis"
```

**Step-by-Step Process:**
1. **Plan**: Describe investigation approach and target
2. **Investigate**: Use tools to examine code, trace flows, analyze patterns
3. **Document**: Record findings with file references and evidence
4. **Iterate**: Continue until root cause is identified
5. **Conclude**: Synthesize findings and recommend actions

**Key Parameters:**
- `confidence`: Track investigation confidence (exploring → low → medium → high → very_high → certain)
- `files_checked`: Document all examined files
- `findings`: Record concrete evidence and insights
- `relevant_files`: Identify files directly related to the issue

## Investigation Types

**Bug Investigation:**
- Trace execution path leading to the bug
- Identify where expected vs actual behavior diverges
- Map call chains and data flow
- Examine error handling and edge cases

**Performance Investigation:**
- Analyze execution bottlenecks
- Trace resource usage patterns
- Identify inefficient algorithms or queries
- Map dependency loading and initialization

**Behavior Investigation:**
- Understand unexpected feature behavior
- Trace user workflow through code
- Identify configuration or state issues
- Map integration points and data flow

**Code Structure Investigation:**
- Understand complex architectural patterns
- Map module dependencies and relationships
- Trace inheritance and composition patterns
- Identify design pattern implementations

## Best Practices

**Investigation Focus:**
- Start broad, then narrow down based on evidence
- Follow the data and code execution paths
- Don't assume - verify with concrete evidence
- Document negative findings (what's NOT the cause)

**Evidence Documentation:**
- Include specific file paths and line numbers
- Reference actual code snippets and behavior
- Note configuration values and environment factors
- Track timeline of events or execution sequence

**Systematic Approach:**
- Use the zen tracer's step-by-step methodology
- Allow investigation between each step
- Build understanding incrementally
- Validate hypotheses with code examination

## Command Structure

```bash
/investigate "description of issue or observation to investigate"
```

**Examples:**
```bash
/investigate "Users report coaching session reminders are not being sent"
/investigate "Dashboard loading is slow for users with many clients"
/investigate "Email campaigns showing incorrect subject lines"
/investigate "Authentication flow redirecting to wrong page after login"
```

## Notes

- The zen tracer enforces investigation between steps - use this structure
- Focus on concrete evidence over speculation
- Document both positive and negative findings
- Use multiple investigation rounds if needed for complex issues
- Consider both technical and business logic perspectives
- Always conclude with actionable recommendations

# The Issue to Investigate
Use the zen tracer tool following the instructions above to investigate the following issue or observation:
$ARGUMENTS