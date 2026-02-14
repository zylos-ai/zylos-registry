<p align="center">
  <img src="./assets/logo.png" alt="Zylos" height="120">
</p>

<h1 align="center">zylos-registry</h1>

<p align="center">
  Component registry for the <a href="https://github.com/zylos-ai/zylos-core">Zylos</a> ecosystem.
</p>

<p align="center">
  <a href="./LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License"></a>
  <a href="https://discord.gg/GS2J39EGff"><img src="https://img.shields.io/badge/Discord-join-5865F2?logo=discord&logoColor=white" alt="Discord"></a>
  <a href="https://x.com/ZylosAI"><img src="https://img.shields.io/badge/X-follow-000000?logo=x&logoColor=white" alt="X"></a>
  <a href="https://zylos.ai"><img src="https://img.shields.io/badge/website-zylos.ai-blue" alt="Website"></a>
  <a href="https://coco.xyz"><img src="https://img.shields.io/badge/Built%20by-Coco-orange" alt="Built by Coco"></a>
</p>

<p align="center">
  <a href="./README.zh-CN.md">中文</a>
</p>

---

- **One command to install** — discover and install any component with `zylos add`
- **Community-driven** — submit your own component via pull request
- **Always current** — the Zylos CLI reads the registry automatically, no manual config

## Official Components

| Component | Type | Description |
|-----------|------|-------------|
| [telegram](https://github.com/zylos-ai/zylos-telegram) | communication | Telegram messaging |
| [lark](https://github.com/zylos-ai/zylos-lark) | communication | Lark/Feishu messaging |
| [feishu](https://github.com/zylos-ai/zylos-feishu) | communication | Feishu messaging (飞书, WebSocket + Webhook) |
| [browser](https://github.com/zylos-ai/zylos-browser) | capability | Browser automation |

## Usage

The registry is used automatically by the Zylos CLI:

```bash
zylos add telegram
zylos add lark
zylos add feishu
zylos add browser
```

## Submit Your Component

Want to add your component to the registry?

1. Build your component using [zylos-component-template](https://github.com/zylos-ai/zylos-component-template)
2. Ensure it follows the [contributing guidelines](./CONTRIBUTING.md)
3. Open a pull request adding your component to `registry.json`

### Requirements

- Public GitHub repository
- Valid `package.json` (official components use `zylos-` prefix)
- Working `SKILL.md` for agent integration
- MIT license (recommended)

## Registry Format

`registry.json` contains a map of component entries:

```json
{
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

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `repo` | string | Yes | GitHub repository in `owner/repo` format |
| `description` | string | Yes | Short description of the component |
| `type` | string | Yes | `communication` or `capability` |
| `official` | boolean | No | `true` for Zylos team components |

## Contributing

See [Contributing Guide](./CONTRIBUTING.md).

## Built by Coco

Zylos is the open-source core of [Coco](https://coco.xyz/) — the AI employee platform.

We built Zylos because we needed it ourselves: reliable infrastructure to keep AI agents running 24/7 on real work. Every component is battle-tested in production at Coco, serving teams that depend on their AI employees every day.

Want a managed experience? [Coco](https://coco.xyz/) gives you a ready-to-work AI employee — persistent memory, multi-channel communication, and skill packages — deployed in 5 minutes.

## License

[MIT](./LICENSE)
