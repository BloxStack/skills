# BloxStack agent skills

[Bloxstack](https://bloxstack.app) is where Roblox creators keep their games, tasks, files and portfolio, run playtests and find work. This skill lets your assistant set you up there: you sign in with Roblox once, and it does the rest, starting with your free Studio hour.

## Install the onboarding skill

```sh
npx skills add BloxStack/skills --skill bloxstack-onboarding
```

Then ask **“Set me up on Bloxstack.”**

## Install in Claude Code with the MCP connection included

```sh
claude plugin install bloxstack-onboarding --marketplace BloxStack/skills
```

## No skill? Paste this

```text
Set me up on Bloxstack: read https://bloxstack.app/start.md and follow it.
```

Works in any assistant that can open a web page and add an MCP server.

[Read the skill](skills/bloxstack-onboarding/SKILL.md) · [Connect an AI app](https://bloxstack.app/learn/studio/agents)

**Remote MCP endpoint** `https://bloxstack.app/mcp`
