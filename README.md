# .github-private

This is the DynamoDS organization repository for [Copilot custom agents](https://docs.github.com/en/copilot/concepts/agents/cloud-agent/about-custom-agents). It stores agent profiles and supporting skills that extend GitHub Copilot's cloud agent for all members of the organization.

## Repository structure

```txt
.github-private/
├── agents/                                  # Released agents — available to all org members
│   ├── <agent-name>.agent.md                # Agent profile (full prompt inlined)
│   └── <agent-name>/
│       └── assets/                          # Reference files loaded on demand by the agent
└── .github/
    └── agents/                              # Test agents — only accessible within this repo
        └── <agent-name>.agent.md
```

## Available agents

| Agent | Description |
|-------|-------------|
| [Dynamo Content Designer](agents/dynamo-content-designer.agent.md) | Technical writing specialist for Dynamo product documentation, blog posts, tutorials, release notes, and educational content. |

## Adding or updating an agent

1. **Read the docs.** Familiarize yourself with the agent profile syntax and available fields: [Creating custom agents](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/create-custom-agents).
2. **Test first.** Create your agent profile in `.github/agents/` using the naming convention `<agent-name>.agent.md`. Agents there are only visible to members with access to this repository, making it safe to iterate. See [Testing custom agents](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/test-custom-agents).
3. **Release.** Move the profile to `agents/` and merge to the default branch. The agent becomes available to all organization members.
4. **Assets.** If your agent references supporting content (style guides, templates, examples), place them under `agents/<agent-name>/assets/`. The agent will read them on demand using its file-reading tools. Do not use relative paths like `./assets/` — use full repo-relative paths like `agents/<agent-name>/assets/<file>.md` so they resolve correctly at runtime.
