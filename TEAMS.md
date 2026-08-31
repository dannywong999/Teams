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

## What to ask

Good:

- `@Cursor draft a reply to Ehsan about the hair salon unit suffix — don’t send it`
- `@Cursor find the latest accessibility memo for 11351 Commerce Parkway in Drive`
- `@Cursor what is on the calendar tomorrow morning`
- `@Cursor add a letter template for occupancy letters`

Less good: a ping with no task (`@Cursor` alone). That only confirms the bot is connected.

## Follow-ups

In a **team channel thread**, reply with another `@Cursor …` to steer the same agent.

In a **personal or group chat**, use **Open in Web** or **Open in Desktop** on the card for follow-ups.

## Accounts

Link Cursor to the **Architelier work** Microsoft account (`dwong@architelier.com`), not a personal Microsoft / Teams Free identity. Work and personal accounts stay separate; switch accounts from the Teams profile menu if the Cursor app was installed while signed into the wrong one.

Install and connect from [Cursor integrations](https://cursor.com/dashboard/integrations) → Microsoft Teams, with GitHub already connected.

## Privacy

Agent summaries on a Teams card can include file names and short excerpts. Do not @Cursor with material you would not put in a shared channel. Do not ask the agent to commit client drawings or financial files to GitHub.
