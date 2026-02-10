<p align="center">
  <img src="./assets/logo.png" alt="Zylos" height="120">
</p>

<h1 align="center">zylos-registry</h1>

<p align="center">
  <a href="https://github.com/zylos-ai/zylos-core">Zylos</a> 生态的组件注册表。
</p>

<p align="center">
  <a href="./LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License"></a>
  <a href="https://discord.gg/vbcR7MWe"><img src="https://img.shields.io/badge/Discord-join-5865F2?logo=discord&logoColor=white" alt="Discord"></a>
  <a href="https://x.com/ZylosAI"><img src="https://img.shields.io/badge/X-follow-000000?logo=x&logoColor=white" alt="X"></a>
  <a href="https://zylos.ai"><img src="https://img.shields.io/badge/website-zylos.ai-blue" alt="Website"></a>
  <a href="https://coco.xyz"><img src="https://img.shields.io/badge/Built%20by-Coco-orange" alt="Built by Coco"></a>
</p>

<p align="center">
  <a href="./README.md">English</a>
</p>

---

- **一条命令安装** — 通过 `zylos add` 发现并安装任意组件
- **社区驱动** — 通过 Pull Request 提交你自己的组件
- **始终最新** — Zylos CLI 自动读取注册表，无需手动配置

## 官方组件

| 组件 | 类型 | 说明 |
|------|------|------|
| [telegram](https://github.com/zylos-ai/zylos-telegram) | 通讯 | Telegram 消息 |
| [lark](https://github.com/zylos-ai/zylos-lark) | 通讯 | 飞书/Lark 消息 |
| [browser](https://github.com/zylos-ai/zylos-browser) | 能力 | 浏览器自动化 |

## 使用方式

Zylos CLI 会自动使用注册表：

```bash
zylos add telegram
zylos add lark
zylos add browser
```

## 提交你的组件

想把你的组件加入注册表？

1. 使用 [zylos-component-template](https://github.com/zylos-ai/zylos-component-template) 构建组件
2. 确保遵循[贡献指南](./CONTRIBUTING.md)
3. 提交 Pull Request，将你的组件添加到 `registry.json`

### 要求

- 公开的 GitHub 仓库
- 有效的 `package.json`（官方组件使用 `zylos-` 前缀）
- 可用的 `SKILL.md` 用于智能体集成
- MIT 许可证（推荐）

## 注册表格式

`registry.json` 包含组件条目映射：

```json
{
  "version": "2.0.0",
  "components": {
    "component-name": {
      "repo": "owner/repo",
      "description": "简短描述",
      "type": "communication | capability",
      "official": true
    }
  }
}
```

| 字段 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `repo` | string | 是 | GitHub 仓库，格式为 `owner/repo` |
| `description` | string | 是 | 组件简短描述 |
| `type` | string | 是 | `communication` 或 `capability` |
| `official` | boolean | 否 | Zylos 团队维护的组件为 `true` |

## 参与贡献

请查看[贡献指南](./CONTRIBUTING.md)。

## 由 Coco 构建

Zylos 是 [Coco](https://coco.xyz/)（AI 员工平台）的开源核心基础设施。

我们构建 Zylos 是因为我们自己需要它：可靠的基础设施，让 AI 智能体 24/7 稳定运行。每个组件都在 Coco 生产环境中经过实战检验，服务于每天依赖 AI 员工的团队。

想要开箱即用？[Coco](https://coco.xyz/) 提供即开即用的 AI 员工——持久记忆、多渠道沟通、技能包——5 分钟完成部署。

## 许可证

[MIT](./LICENSE)
