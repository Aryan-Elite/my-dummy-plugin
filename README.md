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
- **Usage:** `/hello [name]`
- **Purpose:** Greets the user with a motivational quote

## Plugin Structure

```
my-dummy-plugin/
├── .claude-plugin/
│   ├── plugin.json          # Plugin metadata
│   └── marketplace.json     # Marketplace configuration
├── commands/
│   └── hello.md            # Slash command
├── skills/
│   └── task-helper/
│       └── SKILL.md        # Skill definition
└── README.md               # This file
```

## Testing Locally

Test this plugin before publishing:

```bash
# From the parent directory
claude --plugin-dir ./my-dummy-plugin

# Or add as a marketplace
claude plugin marketplace add ./my-dummy-plugin

# Then install
claude plugin install my-dummy-plugin@my-dummy-marketplace
```

## Publishing to Marketplace

### Option 1: GitHub (Recommended)

1. Create a new GitHub repository
2. Push this plugin to the repository:
   ```bash
   cd my-dummy-plugin
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/yourusername/my-dummy-plugin.git
   git push -u origin main
   ```

3. Update `marketplace.json` source to point to your GitHub repo:
   ```json
   "source": "https://github.com/yourusername/my-dummy-plugin"
   ```

4. Users can then add your marketplace:
   ```bash
   claude plugin marketplace add https://github.com/yourusername/my-dummy-plugin
   ```

### Option 2: Local Distribution

1. Share the plugin directory with users
2. Users install with:
   ```bash
   claude plugin marketplace add /path/to/my-dummy-plugin
   claude plugin install my-dummy-plugin@my-dummy-marketplace
   ```

## Validation

Validate your plugin before publishing:

```bash
cd my-dummy-plugin
claude plugin validate .
```

## License

MIT License - Feel free to modify and distribute
