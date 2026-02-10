# Creating GitHub Issues from Game V3 Documentation

This directory contains tools to help you create GitHub issues for all 14 Game V3 features.

## Option 1: Manual Copy/Paste (Recommended)

Use the **`docs/GITHUB_ISSUES.md`** file which contains all 14 issues formatted for easy copy/paste.

### Steps:
1. Open [`docs/GITHUB_ISSUES.md`](../docs/GITHUB_ISSUES.md)
2. For each issue, copy the **Title** and **Description** sections
3. Go to https://github.com/lluppesms/stickman/issues/new
4. Paste the title and description
5. Add the suggested labels
6. Click "Submit new issue"

**Advantages:**
- No setup required
- Full control over each issue
- Can review before creating
- Can customize as needed

## Option 2: GitHub CLI Script (Advanced)

Use the `create-github-issues.sh` script to create all issues automatically.

### Prerequisites:
```bash
# 1. Install GitHub CLI
# See: https://cli.github.com/

# 2. Authenticate with GitHub
gh auth login

# 3. Verify authentication
gh auth status
```

### Usage:
```bash
# Make the script executable (if not already)
chmod +x scripts/create-github-issues.sh

# Run the script
./scripts/create-github-issues.sh
```

**Note:** The current script is a template. You'll need to expand it with the full issue content from `docs/GITHUB_ISSUES.md` if you want to use automated creation.

## Option 3: GitHub Issue Templates (Future)

You could also create GitHub Issue Templates in `.github/ISSUE_TEMPLATE/` directory for ongoing use. This would make it easy for anyone to create properly formatted issues.

## Recommended Labels

Before creating issues, set up these labels in your repository:

| Label | Color | Description |
|-------|-------|-------------|
| `high-priority` | `#d73a4a` (red) | Critical features for V3 |
| `medium-priority` | `#fbca04` (yellow) | Important enhancements |
| `low-priority` | `#0075ca` (blue) | Nice-to-have features |
| `enhancement` | `#a2eeef` (light blue) | New feature or request |
| `audio` | `#7057ff` (purple) | Audio-related features |
| `visuals` | `#e99695` (pink) | Visual/graphics features |
| `gameplay` | `#ff9500` (orange) | Gameplay mechanics |
| `ui` | `#5319e7` (indigo) | User interface |
| `branding` | `#cccccc` (gray) | Branding and marketing |
| `experimental` | `#666666` (dark gray) | Experimental features |

## Additional Organization

### Create a Milestone
1. Go to https://github.com/lluppesms/stickman/milestones
2. Click "New milestone"
3. Title: "Game V3"
4. Description: "Features and improvements for version 3"
5. Assign all created issues to this milestone

### Create a Project Board (Optional)
1. Go to https://github.com/lluppesms/stickman/projects
2. Create a new project: "Game V3 Development"
3. Add columns: "To Do", "In Progress", "Testing", "Done"
4. Add all issues to the board

## Issue Summary

| Priority | Count | Issues |
|----------|-------|--------|
| High | 4 | Sound Effects, Animations, Age Progression, Difficulty Levels |
| Medium | 5 | Backgrounds, Age Buildings, Song Selection, Shop, Damage Numbers |
| Low | 5 | Weather, Title, Blocking, Birds, Marble Simulator |
| **Total** | **14** | **65-97 estimated hours** |

## Implementation Order

See [`docs/IMPLEMENTATION_GUIDE.md`](../docs/IMPLEMENTATION_GUIDE.md) for the recommended implementation sequence with 5 phases.

---

**Ready to create issues?** Start with [`docs/GITHUB_ISSUES.md`](../docs/GITHUB_ISSUES.md)
