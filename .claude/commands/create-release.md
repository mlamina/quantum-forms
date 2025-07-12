# Create New Release

Generate a new release entry for the JourneyLoop release management system based on recent development work.

## Overview

This command will analyze recent git commits, create a new release entry in `releases.yaml`, and generate a beautiful HTML template for the release page.

## Steps

### 1. Find Latest Release Date
```bash
# Read the current releases.yaml to find the most recent release date
cat releases.yaml | head -20
```
- Look for the most recent `date:` field in the first release entry
- Note this date as the starting point for commit analysis

### 2. Analyze Recent Commits
1. get a list of all commits since the last release date:
```bash
git --no-pager log --since="YYYY-MM-DD"  --oneline --date=short --pretty=format:"%h %ad %s"
```
2. Find the commits that are relevant to the release:
   - Look for commits that mention new features, improvements, or bug fixes
   - Focus on commits that solve specific coaching pain points or add significant value
   - (if any) Consider the additional instructions I gave you to identify the relevant commits
3. Use a subagent to read the full commit messages of your identified commits to get a full picture of the changes

### 3. Create Release Entry
Add a new release to the top of `releases.yaml`:

```yaml
releases:
  - id: "YYYY-MM-DD-descriptive-name"
    date: "YYYY-MM-DD"  # Today's date
    title: "Problem-Focused Benefit Title (e.g., 'Spend Less Time on Admin, More Time Coaching')"
    description: "X new tools that help you [solve problem] - included free with your JourneyLoop subscription"
    template: "YYYY-MM-DD-descriptive-name.html"
    email:
      subject: "Save [Specific Benefit] with JourneyLoop's New Features"
      preview_text: "Your clients deserve your full attention. These tools help you deliver it."
      key_updates:
        - title: "Solution-Focused Feature Name"
          description: "Start with pain point. [Problem statement]. Then solution with specific benefit and time savings."
          image: null
          emoji: "📊"
        - title: "Automation-Focused Feature Name"
          description: "Stop manual work. [What automation replaces]. [Specific outcome for coaches]."
          image: null
          emoji: "⚡"
        - title: "Scenario-Based Feature Name"
          description: "[Specific scenario coaches face]? No problem. [How feature solves it] - [benefit statement]."
          image: null
          emoji: "📱"
```

**Value-Oriented Language Guidelines:**
- **Title**: Lead with the problem/benefit, not the feature (e.g., "Save Time" not "New Dashboard")
- **Subject**: Quantify the benefit (e.g., "Save 50% Prep Time" not "New Features")
- **Descriptions**: Follow this formula:
  1. **Pain Point**: "No more scrambling..." / "Stop manually..." / "[Scenario]? No problem."
  2. **Solution**: What the feature does in simple terms
  3. **Specific Benefit**: "Coaches report saving X minutes" / "Zero manual work" / "24/7 access"
- **Focus on time savings, reduced manual work, and specific scenarios coaches face**
- **Use concrete metrics**: "30 minutes per day" not "50% faster"
- **Address real coaching pain points**: session prep, homework creation, emergency access

### 4. Create HTML Template
Create `/templates/releases/YYYY-MM-DD-descriptive-name.html`:

**Reference the Previous Release:**
- Look the latest existing release template in `/templates/releases/`
- Use it as inspiration for structure, styling, and content organization
- Follow the same design patterns and section layouts

**Basic Structure:**
```html
{% extends "releases/release_detail_base.html" %}

{% block release_content %}
  <!-- Create sections that showcase your key features -->
  <!-- Use the previous release template as a style guide -->
  <!-- Focus on coach benefits and user experience improvements -->
  <!-- Include compelling visuals and clear value propositions -->
{% endblock %}
```

**Guidelines:**
- Always extend `releases/release_detail_base.html` (handles hero, navigation, social sharing)
- Use the same gradient color schemes and section styling as the previous release
- Include FontAwesome icons that match the content
- Add `btn` class to all button links for proper styling
- Focus on creating compelling narratives around the features
- Use metrics and specific benefits where available

### 5. Important Guidelines

**Content Focus:**
- Lead with problems coaches face, then present solutions
- Use pain-point language: "No more...", "Stop manually...", "Emergency scenario?"
- Highlight time savings and automation benefits
- Include specific metrics: "30 minutes saved per day", "Zero manual work", "24/7 access"
- Focus on coaching workflow improvements, not technical features

**Design Consistency:**
- Always extend `releases/release_detail_base.html`
- Use gradient backgrounds and consistent color schemes
- Include FontAwesome icons for visual appeal
- Maintain responsive design patterns
- Always add `btn` class to all button links
- **IMPORTANT**: Use Django allauth login URL: `{% url 'account_login' %}` for CTA buttons

**SEO & Social:**
- Meta tags are handled automatically by the base template
- Social sharing URLs use `settings.SITE_URL` dynamically
- Canonical URLs are generated automatically


## Notes

- Focus on 3 key updates maximum to avoid overwhelming coaches
- Each update should solve a real coaching pain point with measurable benefits
- Use value-oriented language following the CRM copywriting model:
  - Start with the problem: "Budget overspend isn't good for sustainable growth"
  - Present the solution: "So here are 6 extra tools you get for free"
  - Use specific scenarios: "Do you have a few client calls today?"
  - Include concrete benefits: "30 minutes saved per day", "Zero manual work"
- Test the release page on mobile devices
- Always include quantified benefits and time savings

## Additional Instructions
$ARGUMENTS