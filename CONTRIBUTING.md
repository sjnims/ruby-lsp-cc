# Contributing

Contributions are welcome! This marketplace currently contains a single plugin (`ruby-lsp`), but PRs improving it are appreciated.

## What to Contribute

- Bug fixes in `plugin.json` configuration
- Improved LSP server settings or extension mappings
- Documentation improvements
- Additional Ruby-related plugins (open an issue first)

## Process

1. Fork the repository
2. Create a branch (`git checkout -b fix/your-fix`)
3. Make your changes
4. Validate with `jq . .claude-plugin/marketplace.json`
5. Open a pull request

## Adding a New Plugin

Open an issue describing the plugin before implementing. New plugins should:

- Focus on Ruby / Rails development tooling
- Have a clear, single purpose
- Include a `plugin.json` and `README.md`
- Be validated before submitting
