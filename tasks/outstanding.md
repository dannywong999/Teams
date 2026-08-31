# Task board

Canonical ledger for **all** Architelier work items — open, waiting, and done.

`@Cursor` (Teams) **instructs**. Grok Bot **Outstanding** **tracks**. They share this file.

- Time zone: `America/Vancouver`
- Next ID: `T-010`
- Last refreshed: 2026-08-31
- Never log fees, invoice amounts, personal appointments, or home addresses
- Never delete a task; move it to Done with a closed date

## Instruct (`@Cursor` → Outstanding)

Treat the Teams (or chat) message as an assignment to the bot. Match an **existing** task when the ID, project, address, or next action is the same. Otherwise create a **new** `T-xxx`.

| Instruction | Effect |
| --- | --- |
| Track / assign `[work]` | Create or update; propose priority if none given |
| Update `T-xxx`: `[text]` | Change description and/or next action |
| Priority `T-xxx` P1–P4 | Set priority (or propose if they said “urgent” / “later”) |
| Waiting `T-xxx` on `[who]` | Status → waiting |
| Done `T-xxx` | Status → done; keep the record |
| List / list outstanding | Open + waiting, P1 first |
| List done / list all | Done history, or the full ledger |

Natural language is enough: *“@Cursor track Vulcan Way code analysis as P1”*, *“@Cursor update T-005: city access is CF-2026-002887”*, *“@Cursor the invoice to accounting is done”*.

## Priority (bot proposes if unset)

| Pri | Use when |
| --- | --- |
| **P1** | Deadline inside 48 hours, or unread city/permit mail that blocks a meeting or filing |
| **P2** | Client, consultant, or city is waiting on us this week |
| **P3** | Real work, no hard date this week |
| **P4** | Setup, housekeeping, or parked until someone else moves |

If the user states a priority, use it. If they say “urgent” / “today” / “before the meeting” → P1. If they say “when you can” / “later” → P3 or P4. Otherwise apply the table and say why in **Last instruction**.

## Index (P1 first)

| ID | Pri | Status | Project | Next action |
| --- | --- | --- | --- | --- |
| T-005 | P1 | open | The Key | Site visit Tue 1 Sep 11:00; read CF-2026-002887 |
| T-003 | P1 | open | 750 Pacific | Review unread DP-2026-00681 city update |
| T-004 | P1 | open | Vulcan Way | Update 3.2.2.76 analysis; send to Avan |
| T-007 | P2 | open | Medcorp | Resend invoice 22280 to accounting@ |
| T-006 | P2 | open | Farm market | Package list for Dave (promised this weekend) |
| T-002 | P2 | open | Teams | Link Cursor to work Teams account |
| T-001 | P2 | open | Grok Bot | Create Bot Outstanding and weekday routine |
| T-008 | P3 | waiting | Hair salon | City / consultant on unit A + Avenue spelling |
| T-009 | P3 | waiting | ATR Expansion | Client follow-up on existing paint booth |

## Records

### T-001 — Create Grok Bot Outstanding
- **Status:** open
- **Priority:** P2
- **Project:** Grok Bot
- **Description:** Standing tracker in Cursor. Sign in as dwong@architelier.com (Pro+ includes Grok Bot). Create Bot `Outstanding` from `bots/outstanding.md`. Weekday 08:00 America/Vancouver routine reconciles this file.
- **Next:** Create the Bot, paste profile, save skill, enable routine, test once
- **Source:** this workspace
- **Last instruction:** @Cursor 2026-08-31: link Teams @Cursor to this Bot for assigned-task tracking
- **Updated:** 2026-08-31

### T-002 — Link Cursor to work Teams
- **Status:** open
- **Priority:** P2
- **Project:** Teams
- **Description:** @Cursor must run under the Architelier work Microsoft account, not a personal Teams identity. Work and personal accounts stay separate.
- **Next:** Sign into Teams as dwong@architelier.com and finish Cursor linking
- **Source:** Microsoft support case opened 31 Aug
- **Last instruction:** @Cursor 2026-08-31: track as setup, P2
- **Updated:** 2026-08-31

### T-003 — DP-2026-00681 750 Pacific Boulevard
- **Status:** open
- **Priority:** P1
- **Project:** 750 Pacific
- **Description:** Unread City of Vancouver development-permit application update. Review before acting; do not invent permit conclusions.
- **Next:** Open the 28 Aug mail from permits@vancouver.ca and decide the next filing or reply
- **Source:** permits@vancouver.ca, 28 Aug, unread
- **Last instruction:** @Cursor 2026-08-31: new task, P1 (unread city mail)
- **Updated:** 2026-08-31

### T-004 — 13631 Vulcan Way Unit 125 code analysis
- **Status:** open
- **Priority:** P1
- **Project:** Vulcan Way
- **Description:** Avan asked to update BCBC 3.2.2.76 and send the code analysis. Building Permit 26-019802. Draft for Danny’s review; do not send unless asked.
- **Next:** Draft the 3.2.2.76 update and hold for send to Avan
- **Source:** Avan Chen, 28 Aug, unread
- **Last instruction:** @Cursor 2026-08-31: new task, P1 (client waiting on code analysis)
- **Updated:** 2026-08-31

### T-005 — The Key site visit
- **Status:** open
- **Priority:** P1
- **Project:** The Key
- **Description:** Site visit with the City Tuesday 1 Sep 2026, 11:00–12:00 Pacific. Unread forward CF-2026-002887 (access) from Troy at Mercury Contracting.
- **Next:** Read CF-2026-002887; attend / prep for 1 Sep 11:00
- **Source:** Troy Felix / Mercury Contracting, 28 Aug
- **Last instruction:** @Cursor 2026-08-31: new task, P1 (deadline inside 48 hours)
- **Updated:** 2026-08-31

### T-006 — Farm market list package
- **Status:** open
- **Priority:** P2
- **Project:** Farm market
- **Description:** Danny told Dave (WHG Design) he would package the farm-market list this weekend.
- **Next:** Assemble the package and send (or draft) to Dave
- **Source:** Dave Wong, 27–28 Aug
- **Last instruction:** @Cursor 2026-08-31: new task, P2 (promised this weekend)
- **Updated:** 2026-08-31

### T-007 — Resend Medcorp invoice 22280
- **Status:** open
- **Priority:** P2
- **Project:** Medcorp
- **Description:** Gary asked that invoice 22280 be resent to accounting@medcorp.ca. Do not record amounts on this board. Draft or send only if Danny says send.
- **Next:** Resend (or draft) invoice 22280 to accounting@medcorp.ca
- **Source:** Gary, 28 Aug
- **Last instruction:** @Cursor 2026-08-31: new task, P2 (accounting waiting)
- **Updated:** 2026-08-31

### T-008 — Hair salon address suffix
- **Status:** waiting
- **Priority:** P3
- **Project:** Hair salon
- **Description:** City requires unit suffix A and “Avenue” (not Ave). Revised schedules/docs sent to Ehsan 31 Aug.
- **Next:** Wait for city / consultant confirmation
- **Source:** Ehsan, 31 Aug
- **Last instruction:** @Cursor 2026-08-31: existing work, status waiting
- **Updated:** 2026-08-31

### T-009 — ATR existing paint booth
- **Status:** waiting
- **Priority:** P3
- **Project:** ATR Expansion
- **Description:** Existing painting room (Engraving Room, Unit 12) is not to current code. Danny advised using the new paint booth. Tracy asked why it is no longer to code.
- **Next:** Wait on client; no further mail unless they ask again
- **Source:** Tracy / Aerojet, 28 Aug
- **Last instruction:** @Cursor 2026-08-31: existing work, status waiting
- **Updated:** 2026-08-31

## Done

_No closed items yet. When a task is done, move its full record here and add **Closed:** YYYY-MM-DD. Keep IDs forever._
