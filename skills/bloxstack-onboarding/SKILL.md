---
name: bloxstack-onboarding
description: Set a Roblox creator up on Bloxstack from nothing, or connect an existing account. Use when someone wants a Bloxstack account or studio, their free Studio hour, a portfolio, a playtest or forum post for their game, or to connect Claude Code, Codex, Cursor or another MCP client to Bloxstack.
license: MIT
metadata:
  author: BloxStack
  runtime: "MCP clients with remote HTTP and OAuth support"
  permissions: "The person signs in with Roblox and approves one studio in their browser. Writes only with their go-ahead."
---

# Set someone up on Bloxstack

Bloxstack (https://bloxstack.app) is where Roblox creators keep their games, tasks, files and portfolio, run playtests, find work, and use Bloxstack Studio: a hosted agent with Blender, sound tools and, in beta, real Roblox Studio in the cloud. You connect over MCP, and the person signs in with Roblox. That one sign-in makes their free account.

New accounts get **their first Studio hour free**, and you can claim it for them (`get_started` says whether it is still open).

## 1. Connect

If Bloxstack tools are already available, skip to step 2. Otherwise add the remote MCP server `https://bloxstack.app/mcp` (Streamable HTTP, OAuth) to the client you are running in, then start its sign-in:

| Client | Add it | Sign in |
| --- | --- | --- |
| Claude Code | `claude mcp add --transport http bloxstack https://bloxstack.app/mcp` | the `authenticate` tool it gains, or `/mcp` |
| Codex CLI | `codex mcp add bloxstack --url https://bloxstack.app/mcp` | `codex mcp login bloxstack` |
| Gemini CLI | `gemini mcp add --transport http bloxstack https://bloxstack.app/mcp` | `/mcp auth bloxstack` |
| Cursor, VS Code, Claude, ChatGPT | add a remote MCP server at the address above | the client's own Connect button |

If your client gives you the sign-in link, hand it over with one line: *"Open this and sign in with Roblox. It makes your free Bloxstack account and connects me."* No password, no form. They choose Continue with Roblox, then **Create studio and allow** (new) or **Allow** (they have one). A new studio arrives founded on their Roblox group when they own or run one; if they ask, keeping it is the better choice, since the studio gets the group's emblem, games and teammates. If the client must restart to load new tools, say so and continue after.

## 2. Set them up

1. Call `get_studio`, then `get_started`. `get_started` is their checklist: each step's state, what it unlocks and the tool or link that does it.
2. Lead with the free Studio hour: one line on what it gets them, ask, then `claim_free_hour`.
3. Then go down the list one step at a time, in plain words, leading with what each one gets them:
   - **Email**: ask for their address, `add_email`, and tell them to click the link. Verifying earns +15 min (claim it with `claim_free_hour`) and is the first requirement for Cloud Roblox Studio.
   - **Their game**: a published Roblox experience they own, `link_experience` with its link or id; an idea, `set_up_game` with a `name` and a one-or-two-sentence `pitch`. +15 min.
   - **Their profile**: draft a headline, bio and roles from what you know about them, show it, then `edit_profile`.
   - **A playtest or forum post** when they have a game: `post_playtest` or `draft_forum_post`. These go out under their name, so only once they say yes.
   - **Cloud Roblox Studio**: share the link `get_started` gives. It takes about five minutes on their phone and a person reviews it.
4. Call `get_started` again after each step and tell them what is next. Stop when they want to stop. Don't list every step at once, and don't push a step they turned down.

## Rules

- Do the steps marked with a tool yourself once they agree. Send them links only for what needs them: signing in, clicking the email link, Cloud Studio.
- Never invent an email address, a game, or profile facts. Ask.
- Only a yes is a yes. Silence, a finished sign-in or a tool being available is not consent to a write.
- Everything you do shows on their studio's Agent page, and they can end the connection there.

The same steps live at https://bloxstack.app/start.md, so this works without the skill too: *"Set me up on Bloxstack: read https://bloxstack.app/start.md and follow it."*

[Connect an AI app](https://bloxstack.app/learn/studio/agents)
