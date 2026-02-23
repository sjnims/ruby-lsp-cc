# ruby-lsp-cc

A Claude Code marketplace providing [ruby-lsp](https://github.com/Shopify/ruby-lsp) integration for Ruby development.

## Installation

Add this marketplace to Claude Code:

```bash
/plugin marketplace add sjnims/ruby-lsp-cc
```

## Available Plugins

| Plugin | Description | Version |
|--------|-------------|---------|
| [ruby-lsp](./plugins/ruby-lsp) | LSP server integration providing Ruby diagnostics, hover info, and go-to-definition | 0.1.0 |

## Installing a Plugin

After adding the marketplace:

```bash
/plugin install ruby-lsp@ruby-lsp-cc
```

## Requirements

- [ruby-lsp](https://github.com/Shopify/ruby-lsp) gem installed (`gem install ruby-lsp`)
- Ruby >= 3.0

## License

MIT
