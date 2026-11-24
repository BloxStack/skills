# BloxStack agent skills

[BloxStack Studio](https://bloxstack.app/studio) gives Roblox teams tools to organize their games, plan tasks, and share files. Your team adds its own work. This skill connects your assistant to the studio you choose through MCP.

## Install the onboarding skill

```sh
npx skills add BloxStack/skills --skill bloxstack-onboarding
```

Ask **“Connect me to my BloxStack studio.”** Sign in, choose a studio, and approve read-only access to get started.

- **Starting fresh?** Tell the assistant what your team is building. It can help you draft your first task in chat. You decide what to add to the workspace.
- **Already using Studio?** Ask a question about work your team has added, such as “Which tasks are still open?” The assistant checks your board before answering.

## Install in Claude Code with the MCP connection included

```sh
claude plugin install bloxstack-onboarding --marketplace BloxStack/skills
```

Open Claude Code and complete the BloxStack browser sign-in when prompted. Pick your studio and choose read-only access to get started.

[Read the skill](skills/bloxstack-onboarding/SKILL.md) · [Studio setup](https://bloxstack.app/learn/studio) · [MCP connection guide](https://bloxstack.app/learn/studio/agents)

**Remote MCP endpoint** `https://bloxstack.app/mcp`
