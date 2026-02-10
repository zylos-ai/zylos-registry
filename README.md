# Zylos Component Registry

The official component registry for the [Zylos](https://github.com/zylos-ai/zylos-core) ecosystem.

## Overview

This registry is consumed by the `zylos` CLI to discover and install components. It contains metadata for all official and community-contributed components.

## Registry Format

`registry.json` contains a map of component entries:

```json
{
  "version": "2.0.0",
  "components": {
    "component-name": {
      "repo": "owner/repo",
      "description": "Short description",
      "type": "communication | capability",
      "official": true
    }
  }
}
```

### Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `repo` | string | Yes | GitHub repository in `owner/repo` format |
| `description` | string | Yes | Short description of the component |
| `type` | string | Yes | `communication` (messaging channels) or `capability` (agent abilities) |
| `official` | boolean | No | `true` for components maintained by the Zylos team |

## Official Components

| Component | Type | Description |
|-----------|------|-------------|
| [telegram](https://github.com/zylos-ai/zylos-telegram) | communication | Telegram messaging |
| [lark](https://github.com/zylos-ai/zylos-lark) | communication | Lark/Feishu messaging |
| [browser](https://github.com/zylos-ai/zylos-browser) | capability | Browser automation |

## Submitting a Component

Want to add your component to the registry?

1. Build your component using [zylos-component-template](https://github.com/zylos-ai/zylos-component-template)
2. Ensure it follows the [contributing guidelines](https://github.com/zylos-ai/.github/blob/main/CONTRIBUTING.md)
3. Open a pull request adding your component to `registry.json`

### Requirements

- Public GitHub repository
- Valid `package.json` with `zylos-` prefix in name
- Working `SKILL.md` for agent integration
- MIT license (recommended)

## Usage

The registry is used automatically by the Zylos CLI:

```bash
# List available components
zylos component list

# Install a component
zylos component install telegram
```

## License

[MIT](LICENSE)
