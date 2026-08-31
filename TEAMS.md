# Using @Cursor in Microsoft Teams

Mention **@Cursor** in a Teams chat or channel to start a Cloud Agent against this workspace (`dannywong999/Teams`, branch `Architelier`) unless you name another repository.

The agent does not run inside Teams. It works in a Cursor VM, then posts a card with the result and any pull request.

## Commands

| You type | What happens |
| --- | --- |
| `@Cursor [task]` | Starts an agent. In an existing agent thread, this is a follow-up. |
| `@Cursor help` | Live command list from Cursor. |
| `@Cursor unlink` or `@Cursor disconnect` | Disconnects *your* Cursor account from Teams. |
| `@Cursor repo=dannywong999/Teams branch=Architelier [task]` | Pins repo and base branch. |

Natural language also works: `@Cursor with opus, draft a city memo for PromoChrom`.

## Outstanding tasks (Grok Bot)

`@Cursor` shares `tasks/outstanding.md` with a Cursor **Grok Bot** named `Outstanding`. That Bot is the standing tracker; Teams `@Cursor` is the mention that updates it from a channel.

| You type | What happens |
| --- | --- |
| `@Cursor list outstanding` | Reads the board and replies on the card |
| `@Cursor add outstanding: [one line]` | Adds a row and opens a PR |
| `@Cursor done T-007` | Marks that ID done |

Create the Bot once: sign into Grok Bot as `dwong@architelier.com` (Pro+ includes it) and follow [bots/outstanding.md](bots/outstanding.md). Weekday 08:00 America/Vancouver routine refreshes the same file.

## What to ask

Good:

- `@Cursor draft a reply to Ehsan about the hair salon unit suffix — don’t send it`
- `@Cursor find the latest accessibility memo for 11351 Commerce Parkway in Drive`
- `@Cursor what is on the calendar tomorrow morning`
- `@Cursor add a letter template for occupancy letters`
- `@Cursor list outstanding`

A ping with no task (`@Cursor` alone) confirms the bot is connected and lists **open** outstanding items.

## Follow-ups

In a **team channel thread**, reply with another `@Cursor …` to steer the same agent.

In a **personal or group chat**, use **Open in Web** or **Open in Desktop** on the card for follow-ups.

## Accounts

Link Cursor to the **Architelier work** Microsoft account (`dwong@architelier.com`), not a personal Microsoft / Teams Free identity. Work and personal accounts stay separate; switch accounts from the Teams profile menu if the Cursor app was installed while signed into the wrong one.

Install and connect from [Cursor integrations](https://cursor.com/dashboard/integrations) → Microsoft Teams, with GitHub already connected.

## Privacy

Agent summaries on a Teams card can include file names and short excerpts. Do not @Cursor with material you would not put in a shared channel. Do not ask the agent to commit client drawings or financial files to GitHub.
