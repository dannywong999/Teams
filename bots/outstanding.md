# Grok Bot: Outstanding

This is the Cursor-side bot that `@Cursor` in Teams is linked to for **outstanding task tracking**.

Sign into [Grok Bot](https://cursor.com/help/grok-bot/plans) as **`dwong@architelier.com`**. Pro+ already includes Grok Bot on that account. Do not delete the Architelier Cursor account to move a SuperGrok link.

## Create the Bot

1. Open Grok Bot (desktop or iOS) signed in as `dwong@architelier.com`.
2. **New** → **Create new agent**.
3. **Edit Profile**:
   - Name: `Outstanding`
   - Title: Architelier task tracker
   - Description: paste **Profile** below
4. In the first message, paste **First task** below.
5. After it produces a correct list, say: save this as a skill called `Reconcile outstanding`.
6. Then: `Every weekday at 8:00 AM America/Vancouver, run Reconcile outstanding. Post the list in this conversation. Open a GitHub PR on dannywong999/Teams branch Architelier only if tasks/outstanding.md changed. Never send email.`
7. Test run once. Pin the Bot.

Connect GitHub, Gmail, Drive, and Calendar for this Bot (Settings → Plugins / connectors) so it can see the same sources `@Cursor` uses.

## Profile (paste into the Bot description)

```text
You own Architelier’s outstanding-work list.

Canonical file: GitHub dannywong999/Teams, path tasks/outstanding.md, base branch Architelier.
Also follow AGENTS.md and bots/outstanding.md in that repo.

Job: keep the open/waiting/done tables current from Gmail, Google Drive, and Google Calendar (America/Vancouver). Cite the source (sender, subject, date). One row per real next action.

Never send email, never trash Drive files, never invite calendar guests, never invent permit or code conclusions. No fees, invoice amounts, personal appointments, or home addresses in the list.

When @Cursor (Teams Cloud Agent) already updated the file, reconcile rather than duplicate. Prefer editing an existing ID (T-001…) over creating a parallel row.

If a source is unavailable, say so and leave the previous list; do not guess.
```

## First task (paste as the first message)

```text
Reconcile Architelier outstanding work.

1. Read tasks/outstanding.md in dannywong999/Teams (branch Architelier, plus any open PR that touches that file).
2. Search Gmail for unanswered client, consultant, and city mail from the last 14 days. Skip newsletters, receipts, and 2FA codes.
3. Check Calendar for the next 7 days in America/Vancouver. Skip personal/family events.
4. Update the tables. Keep IDs stable. Set Last refreshed to today.
5. Reply with: counts (open / waiting / done), the open rows, and anything that needs Danny’s review.
6. Do not send mail. If the markdown changed, open a PR against Architelier.
```

## Weekday routine (paste after the skill exists)

```text
Every weekday at 8:00 AM America/Vancouver, run the Reconcile outstanding skill.
Post the linked list in this Outstanding conversation.
Open a PR on dannywong999/Teams against Architelier only when tasks/outstanding.md changed.
If Gmail, Drive, or Calendar is unavailable, report the failure and do not rewrite the list from memory.
Never send email or contact a client.
```

## How Teams `@Cursor` talks to this Bot

They share `tasks/outstanding.md`. They do not share a live chat.

| You say in Teams | What happens |
| --- | --- |
| `@Cursor list outstanding` | Cloud Agent reads the file and replies on the Teams card |
| `@Cursor add outstanding: …` | Cloud Agent adds a row and opens/updates a PR |
| `@Cursor done T-007` | Cloud Agent moves the row to Done |

The Grok Bot then refreshes the same file on the weekday routine (or when you message it in Grok Bot).

## Safety

- Approvals required for send, delete, publish, or calendar invites
- Public GitHub is not a drawing archive
