<div align="center">
  <img src="https://raw.githubusercontent.com/Prompd/.github/main/assets/logo.png" alt="Prompd" width="120">
  <h1>Prompd</h1>
  <p><strong>From prompt to production</strong></p>
  <p>
    <a href="https://www.prompdhub.ai">Website</a>
    &nbsp;&middot;&nbsp;
    <a href="https://github.com/Prompd/prompd-docs">Docs</a>
    &nbsp;&middot;&nbsp;
    <a href="https://github.com/Prompd/prompd-app/releases">Download</a>
    &nbsp;&middot;&nbsp;
    <a href="https://www.prompdhub.ai/registry">Registry</a>
  </p>
</div>

---

Prompd is an open-source ecosystem for building, composing, and deploying AI workflows. Everything runs on your machine — your API keys stay local and your workflows stay yours.

- **Structured prompt format** — YAML frontmatter + Markdown with typed parameters and context references
- **Package-based inheritance** — inherit, extend, and compose prompts like code
- **Multi-provider compilation** — compile once, target any AI provider
- **Visual workflow canvas** — chain prompts, add logic, connect tools

## The Prompd Format

Prompd introduces `.prmd` — a structured prompt format that turns prompts into versionable, composable, and shareable artifacts.

```yaml
---
name: code-reviewer
version: 1.0.0
inherits: "@prompd/base-agent@^1.0.0"
model: claude-sonnet-4-20250514
parameters:
  - name: language
    type: string
    default: typescript
context:
  - ./standards/style-guide.md
---

Review the following {{language}} code for correctness, performance, and adherence to our style guide.
```

Prompts can inherit from packages, include context files, define typed parameters, and compile to any provider's format.

## How It Works

**Write** structured prompts in `.prmd` with inheritance, parameters, and context references.

**Compose** workflows visually on the canvas or in `.pdflow` files — chain prompts, add logic, connect tools.

**Deploy** workflows as background services with cron triggers, webhooks, or manual execution.

**Share** prompts as packages on the [PrompdHub](https://www.prompdhub.ai/registry) — version, publish, and reuse across projects.

## Get Started

1. [Download the desktop app](https://github.com/Prompd/prompd-app/releases)
2. [Read the docs](https://github.com/Prompd/prompd-docs)
3. [Install the CLI](https://github.com/Prompd/prompd-cli)
4. [Browse community prompts](https://github.com/Prompd/prompds)

## Repositories

| Repo | Description |
|------|-------------|
| [prompd-app](https://github.com/Prompd/prompd-app) | Desktop IDE — Electron + React + Monaco editor + visual workflow canvas |
| [prompd-cli](https://github.com/Prompd/prompd-cli) | CLI toolchain — compile, validate, package, and publish prompts |
| [prompd-api](https://github.com/Prompd/prompd-api) | API integration — turn `.prmd` files into REST, GraphQL, gRPC, and WebSocket endpoints |
| [prompd-vscode](https://github.com/Prompd/prompd-vscode) | VS Code extension — syntax highlighting and IntelliSense for `.prmd` files |
| [prompd-docs](https://github.com/Prompd/prompd-docs) | Documentation — format spec, guides, and examples |
| [prompds](https://github.com/Prompd/prompds) | Community prompts — open-source prompt packages and templates |

## Community

Follow along and get involved:

- [X (Twitter)](https://x.com/prompdhub)
- [Instagram](https://instagram.com/prompdhub)
- [GitHub Discussions](https://github.com/orgs/Prompd/discussions)

## License

Prompd is source-available under the [Elastic License 2.0 (ELv2)](https://github.com/Prompd/prompd-app/blob/main/LICENSE). Free to use, modify, and self-host. The only restriction: you can't offer it as a competing hosted service.
