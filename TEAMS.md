# Using @Cursor in Microsoft Teams

Mention **@Cursor** in a Teams chat or channel to start a Cloud Agent against this workspace (`dannywong999/Teams`, branch `Architelier`) unless you name another repository.

The agent does not run inside Teams. It **instructs** the Cursor Grok Bot named **Outstanding**, which **tracks** every assigned task (new or existing): description, priority, open/waiting/done.

## Assign work to the bot

Say what to track. Outstanding matches an existing `T-xxx` or creates a new one, proposes P1–P4 if you omit priority, and keeps done items forever.

| You type | What the bot does |
| --- | --- |
| `@Cursor track: [work]` | New task, or update if it already exists |
| `@Cursor update T-004: [new description]` | Change description / next action |
| `@Cursor priority T-004 P1` | Set priority (`P1` urgent … `P4` parked) |
| `@Cursor waiting T-008 on the city` | Status → waiting |
| `@Cursor done T-007` | Status → done (record kept) |
| `@Cursor list outstanding` | Open + waiting, P1 first |
| `@Cursor list done` | Closed history |
| `@Cursor list all` | Full ledger |

Natural language is enough:

- `@Cursor track the Vulcan Way 3.2.2.76 update as P1 — don’t send it`
- `@Cursor update T-005: access letter is CF-2026-002887`
- `@Cursor the Medcorp invoice to accounting is done`

Create the Bot once: Grok Bot as `dwong@architelier.com` (Pro+ includes it) → [bots/outstanding.md](bots/outstanding.md). Weekday 08:00 America/Vancouver refreshes the same file (`@Cursor` covers that run until Outstanding exists).

## Other commands

| You type | What happens |
| --- | --- |
| `@Cursor [task]` | Starts an agent. In an existing agent thread, adds a follow-up. |
| `@Cursor help` | Live command list from Cursor. |
| `@Cursor unlink` or `@Cursor disconnect` | Disconnects *your* Cursor account from Teams. |
| `@Cursor repo=dannywong999/Teams branch=Architelier [task]` | Pins repo and base branch. |

## What to ask besides tracking

- `@Cursor draft a reply to Ehsan about the hair salon unit suffix — don’t send it`
- `@Cursor find the latest accessibility memo for 11351 Commerce Parkway in Drive`
- `@Cursor what is on the calendar tomorrow morning`

A ping with no task (`@Cursor` alone) confirms the link and lists **open + waiting**, P1 first.

## Follow-ups

In a **team channel thread**, reply with another `@Cursor …` to steer the same agent.

In a **personal or group chat**, use **Open in Web** or **Open in Desktop** on the card for follow-ups.

## Accounts

Link Cursor to the **Architelier work** Microsoft account (`dwong@architelier.com`), not a personal Microsoft / Teams Free identity.

Install from [Cursor integrations](https://cursor.com/dashboard/integrations) → Microsoft Teams, with GitHub already connected.

## Privacy

Agent summaries on a Teams card can include file names and short excerpts. Do not @Cursor with material you would not put in a shared channel. Do not ask the agent to commit client drawings or financial files to GitHub.
