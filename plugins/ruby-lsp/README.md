# ruby-lsp

Claude Code plugin that integrates [ruby-lsp](https://github.com/Shopify/ruby-lsp) as an LSP server, giving Claude live Ruby code intelligence.

## Features

- **Diagnostics** — Real-time syntax errors and warnings after every edit
- **Hover info** — Type signatures and documentation on hover
- **Go-to-definition** — Navigate to method/class/constant definitions
- **Find references** — Locate all usages of a symbol
- **Code navigation** — Outline symbols in a file

## Requirements

- Ruby >= 3.0
- `ruby-lsp` gem installed

## Installation

### 1. Install the ruby-lsp gem

```bash
gem install ruby-lsp
```

Or add to your `Gemfile`:

```ruby
gem "ruby-lsp", group: :development
```

### 2. Install this plugin

```bash
/plugin install ruby-lsp@ruby-lsp-cc
```

## Supported File Types

| Extension | Language |
|-----------|----------|
| `.rb` | Ruby |
| `.rake` | Ruby |
| `.gemspec` | Ruby |
| `.ru` | Ruby (Rack) |
| `Gemfile` | Ruby |
| `Rakefile` | Ruby |

## Troubleshooting

If you see `Executable not found in $PATH`, ensure `ruby-lsp` is installed and available:

```bash
which ruby-lsp
ruby-lsp --version
```

## Scope

This is a **pure LSP integration** plugin — it registers ruby-lsp as a language server only. It does not add slash commands, agents, or hooks. Ruby diagnostics and navigation features come entirely from the ruby-lsp gem.

## License

MIT
