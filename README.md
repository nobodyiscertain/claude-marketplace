# Claude Marketplace

A collection of custom plugins for Claude Code, providing additional commands, agents, hooks, and MCP server integrations.

## Installation

Install plugins from this marketplace using:

```bash
# Interactive installation
/plugin install

# Direct installation
/plugin install <plugin-name>@nobodyiscertain/claude-marketplace
```

## Available Plugins

### example-plugin
An example plugin demonstrating all plugin components including commands, agents, hooks, and MCP servers.

**Install:** `/plugin install example-plugin@nobodyiscertain/claude-marketplace`

## Creating Your Own Plugin

Use the `example-plugin` as a template. Each plugin should have:

```
plugins/your-plugin-name/
├── .claude-plugin/
│   └── plugin.json          # Required: Plugin metadata
├── commands/                # Optional: Custom slash commands
├── agents/                  # Optional: Specialized subagents
├── hooks/
│   └── hooks.json          # Optional: Event handlers
├── .mcp.json               # Optional: MCP server config
└── README.md               # Recommended: Plugin documentation
```

### Plugin Manifest (plugin.json)

```json
{
  "name": "your-plugin-name",
  "version": "1.0.0",
  "description": "What your plugin does",
  "author": "Your Name",
  "homepage": "https://github.com/nobodyiscertain/claude-marketplace",
  "repository": "https://github.com/nobodyiscertain/claude-marketplace",
  "license": "MIT",
  "keywords": ["relevant", "keywords"]
}
```

### Guidelines

- Use **kebab-case** for plugin names
- Follow **semantic versioning** (MAJOR.MINOR.PATCH)
- All custom paths must be **relative** and start with `./`
- Use `${CLAUDE_PLUGIN_ROOT}` for path references in hooks and MCP configs
- Test with `claude --debug` to see plugin loading details

## Contributing

Contributions are welcome! To add a new plugin:

1. Fork this repository
2. Create your plugin in the `plugins/` directory
3. Follow the structure shown in `example-plugin`
4. Test locally with `claude --debug`
5. Submit a pull request

## License

MIT
