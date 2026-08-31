# Cloud Agent extras (Teams)

This file is read by Cloud / background agents in addition to `AGENTS.md`.

## Teams is the front door

Most runs start because someone mentioned `@Cursor` in Microsoft Teams. The agent executes in a Cursor VM against GitHub, not inside Teams. The Teams card is the status UI; this repo (or another named repo) is the workbench.

Use thread context. If the channel already named the project, address, consultant, or desired change, do not make Danny restate it.

## Empty or ping-only mentions

Treat `@Cursor`, `@cursor`, and “are you there” as a health check:

- Shared ledger: `tasks/outstanding.md`. `@Cursor` **instructs** and may write that file; Grok Bot **Outstanding** **tracks** the same file
- Until T-001 is done, this Cloud Agent is the live writer (including weekday 08:00 America/Vancouver refresh)
- If the default Architelier branch is behind an open PR that edits the ledger, list/update on that PR branch
- Reply with **open + waiting** from `tasks/outstanding.md`, P1 first (ID, pri, next action)
- Mention that new/existing assignments, description edits, and priority changes go on the same board

Do not start a feature build from a ping.

## Write for a Teams card

Keep the final answer short enough to read on a phone:

1. Outcome in the first sentence
2. Links (PR, Drive, Gmail draft, calendar event, Grok Bot Outstanding)
3. Task ID, priority, and status for anything you created or updated; what Danny must still review
4. One suggested follow-up mention if useful

Put long drafts behind a link or in a collapsible section, not as the entire card body.

## Follow-ups

In a **channel thread**, another `@Cursor` reply is a follow-up on the same run. In personal or group chats, tell the user to continue in Cursor (Open in Web / Desktop) if follow-up from Teams is not available.

## Routing

- Default repo: `dannywong999/Teams`
- Default base branch: `Architelier`
- Honor explicit `repo=`, `branch=`, `env=`, `model=`
- If the user names a different repository and this environment cannot access it, say so and stop; do not dump the work into this repo as a substitute

## Safety on a live mailbox

Gmail, Drive, and Calendar are the real office. Destructive or outward-facing actions need an explicit instruction in the prompt or thread (send, delete, trash, invite guests, change sharing). Default to drafts, search, and proposed times.
