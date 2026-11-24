# BloxStack agent skills

Connect your AI assistant to the [BloxStack workspace for Roblox teams](https://bloxstack.app/studio). Ask about the games your team is building, the tasks on its board, or what to pick up first.

## Install the onboarding skill

```sh
npx skills add BloxStack/skills --skill bloxstack-onboarding
```

Then ask your assistant, **“Connect me to BloxStack and show me what my Roblox team is working on.”** It guides you through sign-in, checks the studio you selected, and answers from your workspace. You can choose read-only access.

## Install in Claude Code with the MCP connection included

```sh
claude plugin install bloxstack-onboarding --marketplace BloxStack/skills
```

Open Claude Code and complete the BloxStack browser sign-in when prompted. Pick your studio and choose read-only access for the first briefing.

[Read the skill](skills/bloxstack-onboarding/SKILL.md) · [Studio setup](https://bloxstack.app/learn/studio) · [MCP connection guide](https://bloxstack.app/learn/studio/agents)

**Remote MCP endpoint** `https://bloxstack.app/mcp`
