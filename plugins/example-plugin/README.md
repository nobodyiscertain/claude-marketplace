# Example Plugin

An example plugin demonstrating all the components of a Claude Code plugin.

## Features

### Commands
- `/hello` - Greets the user with the current date and time

### Agents
- `code-reviewer` - Reviews code for best practices and potential issues

### Hooks
- Pre/Post tool use logging for debugging

### MCP Servers
- `example-server` - Demonstrates external tool integration

## Installation

```bash
/plugin install example-plugin@nobodyiscertain/claude-marketplace
```

## Usage

After installation, try:
- `/hello` to test the command
- Ask Claude to review your code (the agent will be automatically available)

## Development

This plugin serves as a template. Copy this structure to create your own plugins.
