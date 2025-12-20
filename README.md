# dlawskillz

Shared Claude Code skills and commands for all projects.

## Installation

Add this marketplace to your project's `.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "dlawskillz": {
      "source": {
        "source": "github",
        "repo": "YOUR_USERNAME/dlawskillz"
      }
    }
  },
  "enabledPlugins": {
    "core@dlawskillz": true
  }
}
```

## Available Plugins

### core

Core workflow skills and commands.

#### Commands (user-invoked with `/command`)
- `/catchup` - Read project context (designs, docs, implementation notes, TODO)
- `/pr` - Run tests and create a PR
- `/session-notes` - Generate implementation notes for the session
- `/summaryplan` - Show open TODO items
- `/task` - Break down and plan a task

#### Skills (auto-invoked by Claude)
- `stage` - Stage branch in GitHub with PR
- `feature` - Create a new feature branch

## Adding New Skills

1. Create a new directory under `plugins/core/skills/your-skill/`
2. Add a `SKILL.md` file with frontmatter:

```yaml
---
name: your-skill
description: Brief description for when Claude should use this
---
# your-skill

## Instructions
...

## Examples
...
```

## Adding New Commands

Add a markdown file to `plugins/core/commands/your-command.md`
