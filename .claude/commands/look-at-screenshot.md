# Look at Screenshot

Analyze the most recent screenshot on the desktop and provide insights based on specific instructions.

## Overview

This command lists PNG files on the desktop sorted by modification time (newest first), reads the latest screenshot file, and analyzes it according to the provided context or instructions.

## Process

### 1. List Desktop Screenshots
- Use LS tool to list PNG files in the desktop directory
- Sort by modification time (newest first)
- Identify the most recent screenshot

### 2. Read Screenshot
- Use Read tool to view the latest PNG file
- Load the image for visual analysis

### 3. Analyze Content
- Examine the screenshot based on provided arguments
- Focus on specific elements, issues, or questions mentioned
- Provide relevant insights and observations

## Implementation Steps

1. **Find Desktop Directory**: List PNG files in `/Users/mlamina/Desktop/`
2. **Identify Latest**: Select the most recently modified PNG file
3. **Load Image**: Read the screenshot file for analysis
4. **Analyze**: Examine the content based on the provided context
5. **Report**: Provide focused insights and observations

## Command Structure

```bash
/look-at-screenshot "specific instructions or context for analysis"
```

**Examples:**
```bash
/look-at-screenshot "Check for any UI bugs or layout issues"
/look-at-screenshot "Analyze the error message and suggest fixes"
/look-at-screenshot "Review the design and provide feedback"
/look-at-screenshot "Identify any accessibility concerns"
```

## Analysis Focus Areas

**UI/UX Analysis:**
- Layout and design issues
- Visual bugs or inconsistencies
- User experience problems
- Accessibility concerns

**Error Analysis:**
- Error messages and their context
- Stack traces and debugging information
- Console outputs and logs
- System status indicators

**Design Review:**
- Visual design quality
- Brand consistency
- Typography and spacing
- Color usage and contrast

**Content Review:**
- Text accuracy and clarity
- Information architecture
- Content organization
- Missing or incorrect data

## Technical Implementation

```bash
# List PNG files sorted by modification time
ls -lt ~/Desktop/*.png | head -10

# Read the most recent screenshot
# (This will be handled by the Read tool with the identified file path)
```

## Best Practices

**Image Analysis:**
- Focus on the specific aspects mentioned in arguments
- Provide actionable insights and recommendations
- Consider both technical and user experience perspectives
- Identify both issues and positive elements

**Reporting:**
- Be concise but thorough in observations
- Prioritize findings by severity or importance
- Suggest specific improvements when possible
- Reference specific UI elements or areas

## Notes

- Only analyzes PNG files on the desktop
- Always reads the most recent file by modification time
- Analysis is guided by the specific instructions provided in arguments
- Useful for quick UI reviews, error analysis, and design feedback

# The Screenshot Analysis to Perform

Analyze the most recent desktop screenshot:
$ARGUMENTS