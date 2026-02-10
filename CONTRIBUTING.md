# Contributing to Zylos Registry

Thank you for your interest in contributing a component to the Zylos ecosystem!

## Adding a Component

### Prerequisites

Your component must:

1. **Be a public GitHub repository** with a working installation
2. **Follow the component structure** — use [zylos-component-template](https://github.com/zylos-ai/zylos-component-template) as a starting point
3. **Include a `SKILL.md`** that defines how agents interact with the component
4. **Include a `README.md`** with installation and usage instructions
5. **Use ESM** (ES Modules) — no CommonJS

### Submission Process

1. Fork this repository
2. Add your component entry to `registry.json`:

```json
{
  "your-component": {
    "repo": "your-org/zylos-your-component",
    "description": "Brief description of what it does",
    "type": "communication or capability"
  }
}
```

3. Open a pull request with:
   - Component name and description
   - Link to the repository
   - Brief explanation of what it does and why it's useful

### Review Criteria

We review submissions for:

- **Functionality** — Does it work as described?
- **Quality** — Code follows ESM standards, proper error handling
- **Security** — No obvious vulnerabilities, safe credential handling
- **Documentation** — Clear README and SKILL.md

### Component Types

- **communication** — Messaging channels (Telegram, Lark, Discord, etc.)
- **capability** — Agent abilities (browser automation, file processing, etc.)

## Questions?

Open an [issue](https://github.com/zylos-ai/zylos-registry/issues) if you have questions about submitting a component.
