<div align="center">
  <img src="https://raw.githubusercontent.com/Prompd/.github/main/assets/prompd-icon.png" alt="Prompd" width="120">
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

Prompd is an open-source desktop application for building, composing, and deploying AI workflows. It gives you a local-first prompt IDE with a visual workflow canvas, structured prompt format, package-based inheritance, and a CLI that compiles prompts into provider-ready output.

Everything runs on your machine. Your API keys stay local. Your workflows stay yours.

## Repositories

| Repo | Description |
|------|-------------|
| [prompd-app](https://github.com/Prompd/prompd-app) | Desktop IDE — Electron + React + Monaco editor + visual workflow canvas |
| [prompd-cli](https://github.com/Prompd/prompd-cli) | CLI toolchain — compile, validate, package, and publish prompts |
| [prompd-vscode](https://github.com/Prompd/prompd-vscode) | VS Code extension — syntax highlighting and IntelliSense for `.prmd` files |
| [prompd-docs](https://github.com/Prompd/prompd-docs) | Documentation — format spec, guides, and examples |
| [prompds](https://github.com/Prompd/prompds) | Community prompts — open-source prompt packages and templates |

## The Prompd Format

Prompd introduces `.prmd` — a structured prompt format with YAML frontmatter and Markdown content. Prompts become versionable, composable, and shareable artifacts instead of disposable text.

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

**Share** prompts as packages on the [Prompd Registry](https://www.prompdhub.ai/registry) — version, publish, and reuse across projects.

## Get Started

1. [Download the desktop app](https://github.com/Prompd/prompd-app/releases)
2. [Read the docs](https://github.com/Prompd/prompd-docs)
3. [Install the CLI](https://github.com/Prompd/prompd-cli)
4. [Browse community prompts](https://github.com/Prompd/prompds)

## Community

Follow along and get involved:

- [X (Twitter)](https://x.com/prompdhub)
- [Instagram](https://instagram.com/prompdhub)
- [GitHub Discussions](https://github.com/orgs/Prompd/discussions)

## License

Prompd is open source under the [MIT License](https://github.com/Prompd/prompd-app/blob/main/LICENSE).
