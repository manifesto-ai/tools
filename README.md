# @manifesto-ai/tools

[![CI](https://github.com/manifesto-ai/tools/actions/workflows/ci.yml/badge.svg)](https://github.com/manifesto-ai/tools/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> Developer tools for the Manifesto AI ecosystem

## Overview

This monorepo contains **developer tools** for working with the [Manifesto AI](https://github.com/manifesto-ai) ecosystem. These tools help with migration, code generation, and development workflows.

## Packages

| Package | Description | npm |
|---------|-------------|-----|
| [`@manifesto-ai/react-migrate`](./packages/react-migrate) | Agent-powered React to Manifesto migration tool | [![npm](https://img.shields.io/npm/v/@manifesto-ai/react-migrate)](https://www.npmjs.com/package/@manifesto-ai/react-migrate) |

## react-migrate

An AI-powered CLI tool that helps migrate existing React applications to use Manifesto AI's domain-driven architecture.

### Features

- AST-based React component analysis using SWC
- Multi-provider LLM support (OpenAI, Anthropic, Ollama)
- Interactive CLI with progress tracking
- Incremental migration with state persistence
- Automatic domain model generation

### Quick Start

```bash
# Install globally
npm install -g @manifesto-ai/react-migrate

# Or use with npx
npx @manifesto-ai/react-migrate

# Run in your React project
cd your-react-app
react-migrate
```

### Usage

```bash
# Interactive mode
react-migrate

# Analyze specific files
react-migrate analyze src/components/**/*.tsx

# Generate domain models
react-migrate generate --output src/domains
```

## Development

### Prerequisites

- Node.js >= 22
- pnpm >= 9

### Setup

```bash
# Clone the repository
git clone https://github.com/manifesto-ai/tools.git
cd tools

# Install dependencies
pnpm install

# Build all packages
pnpm build

# Run tests
pnpm test

# Type check
pnpm typecheck
```

### Project Structure

```
tools/
├── packages/
│   └── react-migrate/    # Migration CLI tool
├── .github/workflows/    # CI/CD
├── package.json          # Root workspace config
├── pnpm-workspace.yaml
└── turbo.json            # Build orchestration
```

## Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Related Projects

- [@manifesto-ai/core](https://github.com/manifesto-ai/core) - Core domain modeling and runtime
- [@manifesto-ai/bridge](https://github.com/manifesto-ai/bridge) - Framework bindings
- [@manifesto-ai/projection](https://github.com/manifesto-ai/projection) - Read-only projections

## License

MIT © [Manifesto AI](https://github.com/manifesto-ai)
