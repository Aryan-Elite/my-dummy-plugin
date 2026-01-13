# My Dummy Plugin

A sample Claude Code plugin demonstrating skills and commands for learning purposes.

## Contents

This plugin includes:

### 1. Task Helper Skill
- **Location:** `skills/task-helper/SKILL.md`
- **Purpose:** Helps break down complex tasks into manageable steps
- **Trigger:** Automatically activates when users need to organize multi-step projects

### 2. Hello Command
- **Location:** `commands/hello.md`
- **Usage:** `/my-dummy-plugin:hello [name]`
- **Purpose:** Greets the user with a motivational quote

## Plugin Structure

```
my-dummy-plugin/
├── .claude-plugin/
│   └── plugin.json          # Plugin metadata (ONLY file in .claude-plugin/)
├── commands/
│   └── hello.md            # Slash command
├── skills/
│   └── task-helper/
│       └── SKILL.md        # Skill definition
└── README.md               # This file
```

## Installation from GitHub

Users can install this plugin directly from GitHub:

```bash
# Step 1: Add the GitHub repository as a marketplace
/plugin marketplace add Aryan-Elite/my-dummy-plugin

# Step 2: Install the plugin
/plugin install my-dummy-plugin

# Step 3: Verify installation
/plugin list
```

### Using the Plugin

After installation:

```bash
# Use the hello command (namespaced by plugin name)
/my-dummy-plugin:hello
/my-dummy-plugin:hello YourName

# The task-helper skill activates automatically when you ask for help organizing tasks
```

## Testing Locally

Test this plugin before pushing to GitHub:

```bash
# From the parent directory
claude --plugin-dir ./my-dummy-plugin

# Or add as a local marketplace
/plugin marketplace add ./my-dummy-plugin

# Then install
/plugin install my-dummy-plugin
```

## For Plugin Developers

If you're forking this plugin:

1. Update the plugin name in `.claude-plugin/plugin.json`
2. Modify commands and skills as needed
3. Push to your own GitHub repository
4. Share your GitHub username/repo with users for installation

## Validation

Validate your plugin before publishing:

```bash
cd my-dummy-plugin
claude plugin validate .
```

## License

MIT License - Feel free to modify and distribute
