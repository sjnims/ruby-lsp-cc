# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Claude Code plugin marketplace (`ruby-lsp-cc`) containing a single plugin that integrates [ruby-lsp](https://github.com/Shopify/ruby-lsp) as an LSP server. This is a pure LSP integration — no commands, agents, skills, or hooks.

## Architecture

This is a Claude Code **marketplace** (not just a plugin). Two manifest files drive everything:

- `.claude-plugin/marketplace.json` — marketplace manifest; `pluginRoot: ./plugins` sets the base path for local plugin sources
- `plugins/ruby-lsp/.claude-plugin/plugin.json` — plugin manifest; defines `lspServers.ruby` configuration

The `lspServers` config maps file extensions (`.rb`, `.rake`, `.gemspec`, `.ru`) to the `ruby-lsp` command, which must be in the user's PATH.

## Validation

```bash
jq . .claude-plugin/marketplace.json
jq . plugins/ruby-lsp/.claude-plugin/plugin.json
```

## Key Constraints

- All JSON files must be valid — no trailing commas, no comments
- Names must be kebab-case
- Versions must be semver
- `extensionToLanguage` keys must start with `.` (no bareword filenames like `Gemfile`)
- Plugin and marketplace versions should stay in sync
- New plugins go under `plugins/<name>/.claude-plugin/plugin.json` and need a `README.md`
