# Zen Code — AI Coding Agent for Your Terminal

An open-source AI coding agent that lives in your terminal. Powered by the Zen Coder model family from [Zen LM](https://zenlm.org).

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Node.js Version](https://img.shields.io/badge/node-%3E%3D20.0.0-brightgreen.svg)](https://nodejs.org/)

## Why Zen Code?

- **Codebase understanding**: Ask questions about large, unfamiliar repos
- **Multi-file edits**: Refactor across files with a single prompt
- **Test execution**: Run tests and iterate on failures automatically
- **Git integration**: Commit, diff, and review changes in-flow
- **MCP tools**: 260+ tools via Model Context Protocol
- **Intelligent routing**: Automatically selects from Zen Coder 4B–480B based on task complexity

## Installation

```bash
npm install -g @zen/code
```

Or with Homebrew:

```bash
brew install zen-code
```

## Quick Start

```bash
# Launch interactive session
zen-code

# Run a single task (headless)
zen-code "add tests for the auth module"

# Reference specific files
zen-code "refactor @src/api/handler.ts to use async/await"
```

## Usage

### Interactive mode

```bash
cd your-project/
zen-code
```

Type prompts directly. Use `@filename` to reference files in context.

### Headless mode (scripts, CI)

```bash
zen-code -p "fix the failing tests in src/"
```

### IDE integration

Zen Code integrates with VS Code, Zed, and JetBrains IDEs. See [zenlm.org](https://zenlm.org) for setup guides.

## Configuration

Create `~/.zen/settings.json`:

```json
{
  "modelProviders": {
    "openai": [
      {
        "id": "zenlm/zen-coder",
        "name": "Zen Coder",
        "baseUrl": "http://localhost:8000/v1",
        "envKey": "ZEN_API_KEY"
      }
    ]
  },
  "model": {
    "name": "zenlm/zen-coder"
  }
}
```

## Models

Zen Code uses the Zen Coder family with intelligent routing:

| Model | Parameters | Context | Best For |
|-------|-----------|---------|----------|
| Zen Coder 4B | 4B | 32K | Fast edits, edge deployment |
| Zen Coder Flash | 31B MoE | 131K | Balanced performance |
| Zen Coder 480B | 480B MoE | 128K | Complex refactors, frontier tasks |

Deploy with vLLM:

```bash
vllm serve zenlm/zen-coder --port 8000
```

## Session Commands

- `/help` — list commands
- `/clear` — clear conversation history
- `/compress` — compress history to save tokens
- `/stats` — show session info
- `/exit` — quit

## Links

- **Website**: https://zenlm.org
- **Models**: https://huggingface.co/zenlm
- **GitHub**: https://github.com/zenlm
- **Hanzo MCP**: https://github.com/hanzoai/mcp

## License

Apache 2.0

---

**Zen AI**: Clarity Through Intelligence
