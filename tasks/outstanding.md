# Task board

Canonical ledger for **all** Architelier work items — open, waiting, and done.

`@Cursor` (Teams) **instructs**. Grok Bot **Outstanding** **tracks**. They share this file.

- Time zone: `America/Vancouver`
- Next ID: `T-016`
- Last refreshed: 2026-08-31 (Cloud Agent reconcile: Gmail + Drive + Calendar)
- Weekday 08:00 America/Vancouver refresh: this Cloud Agent runs it until T-001 closes (Grok Bot Outstanding then owns the routine). Re-subscribe the timer before it expires (currently 2026-09-07).
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
| T-005 | P1 | open | The Key | Site visit Tue 1 Sep 11:00; read unread CF-2026-002887 |
| T-003 | P1 | open | 750 Pacific | Review unread DP-2026-00681 city update; draft only |
| T-004 | P1 | open | Vulcan Way | Draft 3.2.2.76 update for Avan; do not send |
| T-006 | P1 | open | Farm market | Weekend package promise (28 Aug) has passed; still unsent |
| T-010 | P2 | open | Oak Station Dental | Read unread Gary 28 Aug follow-up; draft reply |
| T-012 | P2 | open | Capital Direct | Unread code/CAD mail; answer shower accessibility |
| T-014 | P2 | open | 501 Nelson | Draft reply to Coquitlam additional-unit mail; do not send |
| T-013 | P2 | open | 5514 Smith Ave | Read unread 28 Aug Helen forward on height / excavation |
| T-015 | P2 | open | Dr. Au Hastings | City notes 26 Aug; schedules/drawings still unrevised |
| T-002 | P2 | open | Teams | Reply to Microsoft case 2608310010000403 |
| T-001 | P2 | open | Grok Bot | Create Bot Outstanding and weekday routine |
| T-011 | P3 | waiting | CU Vision | Danny replied 30 Aug; wait on contractor / SE |
| T-008 | P3 | waiting | Hair salon | Revised IFP sent 31 Aug; wait on city occupancy |
| T-009 | P3 | waiting | ATR Expansion | Wait on client; no new mail this refresh |

## Records

### T-001 — Create Grok Bot Outstanding
- **Status:** open
- **Priority:** P2
- **Project:** Grok Bot
- **Description:** Standing tracker in Cursor. Sign in as dwong@architelier.com (Pro+ includes Grok Bot). Create Bot `Outstanding` from `bots/outstanding.md`. Weekday 08:00 America/Vancouver routine reconciles this file. Until that Bot exists, this Cloud Agent runs the same weekday refresh (Gmail + Drive + Calendar → this file). No mail is sent.
- **Next:** Create the Bot, paste profile, save skill, enable the weekday routine, test once. Then this Cloud Agent stops covering the 08:00 run.
- **Source:** this workspace; Cursor support (ticket T-F24808) confirmed Grok account link is permanent — do not delete dwong@architelier.com to move SuperGrok
- **Last instruction:** @Cursor 2026-08-31: still no Bot; Cloud Agent weekday timer covers the refresh until T-001 is done (timer expires 2026-09-07; renew if still open)
- **Updated:** 2026-08-31

### T-002 — Link Cursor to work Teams
- **Status:** open
- **Priority:** P2
- **Project:** Teams
- **Description:** @Cursor must run under the Architelier work Microsoft account (`dwong@architelier.com`), not a personal Teams identity. Work and personal accounts stay separate. Microsoft cannot fully consolidate them.
- **Next:** Reply to unread Microsoft case **2608310010000403** (31 Aug 06:58): Cursor should link to the **work** Teams account; include the exact linking error if any. Do not switch @Cursor to a personal Microsoft account.
- **Source:** help@mail.support.microsoft.com, unread 31 Aug; Teams Essentials welcome 31 Aug
- **Last instruction:** @Cursor 2026-08-31 reconcile: Microsoft asked two facts (work vs personal; error text)
- **Updated:** 2026-08-31

### T-003 — DP-2026-00681 750 Pacific Boulevard
- **Status:** open
- **Priority:** P1
- **Project:** 750 Pacific
- **Description:** Unread City of Vancouver development-permit application update. Review before acting; do not invent permit conclusions.
- **Next:** Open the 28 Aug mail from permits@vancouver.ca and draft any reply for Danny. Do not send.
- **Source:** permits@vancouver.ca, 28 Aug 16:01 Pacific, still UNREAD
- **Last instruction:** @Cursor 2026-08-31 reconcile: still unread city mail → keep P1
- **Updated:** 2026-08-31

### T-004 — 13631 Vulcan Way Unit 125 code analysis
- **Status:** open
- **Priority:** P1
- **Project:** Vulcan Way
- **Description:** Avan asked to update BCBC 3.2.2.76 and send the code analysis. Building Permit 26-019802. Draft for Danny’s review; do not send unless asked. Do not invent code conclusions.
- **Next:** Draft the 3.2.2.76 update and hold for Danny
- **Source:** Avan Chen, 28 Aug 21:27 Pacific, still UNREAD
- **Last instruction:** @Cursor 2026-08-31 reconcile: Avan still unread → keep P1
- **Updated:** 2026-08-31

### T-005 — The Key site visit
- **Status:** open
- **Priority:** P1
- **Project:** The Key
- **Description:** Site visit with the City Tuesday 1 Sep 2026, 11:00–12:00 Pacific (Troy Felix / Mercury Contracting invite in Gmail). Unread forward CF-2026-002887 (access) from Troy. Invite is **not** on the Google Calendar this run saw (only a personal appointment was listed — do not put personal events on this board).
- **Next:** Read unread CF-2026-002887; prep / attend 1 Sep 11:00. Draft a city reply only if needed; do not send.
- **Source:** troy@mercurycontracting.com, 28 Aug, UNREAD city forward + Gmail invite
- **Last instruction:** @Cursor 2026-08-31 reconcile: visit is tomorrow; city mail still unread → keep P1
- **Updated:** 2026-08-31

### T-006 — Farm market list package
- **Status:** open
- **Priority:** P1
- **Project:** Farm market
- **Description:** Danny told Dave (WHG Design) on 28 Aug he would package the farm-market list **this weekend** (29–30 Aug). That window has passed. Thread still unread. This is the Dave / WHG list package, not a separate Kerr Street filing.
- **Next:** Assemble the package and draft (or send only if Danny says send) to Dave
- **Source:** dave@whgdesign.ca, 27–28 Aug, UNREAD
- **Last instruction:** @Cursor 2026-08-31 reconcile: promised weekend passed with no sent package → raise P2 to P1
- **Updated:** 2026-08-31

### T-008 — Hair salon address suffix
- **Status:** waiting
- **Priority:** P3
- **Project:** Hair salon
- **Description:** City requires unit suffix A and “Avenue” (not Ave). Danny sent revised IFP / schedules to Ehsan 31 Aug. Drive: `2613 - Booked - IFP - 26.08.30.pdf`.
- **Next:** Wait for city / consultant confirmation. No chase unless Danny asks.
- **Source:** ehsan@validesign.ca, 31 Aug; Danny reply 31 Aug 22:10 Pacific
- **Last instruction:** @Cursor 2026-08-31 reconcile: IFP sent; keep waiting
- **Updated:** 2026-08-31

### T-009 — ATR existing paint booth
- **Status:** waiting
- **Priority:** P3
- **Project:** ATR Expansion
- **Description:** Existing painting room (Engraving Room, Unit 12) is not to current code. Danny advised using the new paint booth. Tracy asked why it is no longer to code and said they are researching.
- **Next:** Wait on client; no further mail unless they ask again
- **Source:** Tracy / Aerojet, 27–28 Aug; no new ATR occupancy mail this refresh
- **Last instruction:** @Cursor 2026-08-31 reconcile: no change
- **Updated:** 2026-08-31

### T-010 — Oak Station Dental / Dr. Chris Low
- **Status:** open
- **Priority:** P2
- **Project:** Oak Station Dental
- **Description:** Courtney (Opal) sent permit bases 14 Aug for 1055 West Broadway Unit 201. Gary followed up 28 Aug; that mail is still unread. Drive folder `2602 - 1055 West Broadway, Unit 201 (Chris)` opened 30 Aug. Job #2602.
- **Next:** Read Gary’s 28 Aug follow-up. Draft a reply for Danny. Do not send unless Danny says send.
- **Source:** courtney@opaldesignstudio.ca / gary@medcorp.ca; unread 28 Aug 04:37 Pacific
- **Last instruction:** @Cursor 2026-08-31 reconcile: new from unread client follow-up, P2 (waiting on us this week)
- **Updated:** 2026-08-31

### T-011 — CU Vision 6388 No. 3 Rd SE sign-off
- **Status:** waiting
- **Priority:** P3
- **Project:** CU Vision
- **Description:** Sara (Medico) asked 28 Aug whether the building inspector’s request for structural-engineer sign-off on architectural drawings is typical. Danny replied 30 Aug: get SE sign-off on **steel stud and ceiling** for seismic.
- **Next:** Wait on contractor / SE. No chase unless Danny asks.
- **Source:** sara@medicoconstruction.com, 28 Aug; Danny sent 30 Aug 08:00 Pacific
- **Last instruction:** @Cursor 2026-08-31 reconcile: new, status waiting (ball is elsewhere)
- **Updated:** 2026-08-31

### T-012 — Capital Direct 3rd floor expansion code review
- **Status:** open
- **Priority:** P2
- **Project:** Capital Direct
- **Description:** Patricia (SSDG) sent code items 27 Aug, including whether the new shower room must be accessible. Danny asked for CAD 28 Aug; CAD came back the same day (unread). Ellen followed up 28 Aug: accessibility answer is needed for corridor widths (unread).
- **Next:** Read the unread CAD / follow-up. Draft accessibility and corridor answers for Danny. Mark as draft for professional review. Do not send.
- **Source:** pcho@ssdg.com / epeterson@ssdg.com, 27–28 Aug, UNREAD
- **Last instruction:** @Cursor 2026-08-31 reconcile: new from unread consultant mail, P2
- **Updated:** 2026-08-31

### T-013 — 5514 Smith Ave height / excavation
- **Status:** open
- **Priority:** P2
- **Project:** 5514 Smith Ave
- **Description:** Unread 28 Aug forward from Helen: please check an excavation scheme (one-foot down; keep front level, drop rear) against the zoning 9.5 m height limit, aiming for 8'-6" ceilings on second and top floors. Danny is architect of record on the coordination thread with Canadian Blueprint / Rion / Voltas. Do not invent zoning conclusions.
- **Next:** Read the unread forward. Draft a height/excavation response for Danny. Do not send.
- **Source:** helen_maison@vip.163.com, 28 Aug 13:40 Pacific, UNREAD
- **Last instruction:** @Cursor 2026-08-31 reconcile: new from unread design-team mail, P2
- **Updated:** 2026-08-31

### T-014 — 501 Nelson St additional unit
- **Status:** open
- **Priority:** P2
- **Project:** 501 Nelson
- **Description:** Coquitlam (hyeo) followed up 27 Aug on the additional-unit discussion. Ruth asked Danny to answer the city because the mail was addressed to him. Carlo said Danny’s reply would carry more weight, or Carlo can send if Danny prefers. No Architelier reply in the thread after 27 Aug.
- **Next:** Draft a reply for Danny (or a note telling Carlo to send). Do not send unless Danny says send. Do not invent occupancy/unit conclusions.
- **Source:** hyeo@coquitlam.ca / ruth@janksdesigngroup.com / carlo@milancpm.com, 27 Aug
- **Last instruction:** @Cursor 2026-08-31 reconcile: new from city + team waiting on Danny, P2
- **Updated:** 2026-08-31

### T-015 — Dr. Au 2122 East Hastings city notes
- **Status:** open
- **Priority:** P2
- **Project:** Dr. Au Hastings
- **Description:** Ameer (Seasons) sent city notes 26 Aug and asked Danny to change schedules and drawings (including an existing pre-renovation drawing). Address confirmed in-thread as 2122 East Hastings. No Architelier reply in the thread.
- **Next:** Review city notes and draft schedule/drawing revisions for Danny. Do not send. Do not invent permit conclusions.
- **Source:** ameer@seasonscontractingltd.com, 26 Aug
- **Last instruction:** @Cursor 2026-08-31 reconcile: new from city notes waiting on us, P2
- **Updated:** 2026-08-31

## Done

### T-007 — Resend Medcorp invoice 22280
- **Status:** done
- **Priority:** P2
- **Project:** Medcorp
- **Description:** Gary asked that invoice 22280 be resent to accounting@medcorp.ca. Do not record amounts on this board.
- **Next:** none
- **Source:** Gary 28 Aug 12:04 Pacific; Danny sent 22280 (and 22281) to Accounting@medcorp.ca 28 Aug 12:55 Pacific. No bounce found.
- **Last instruction:** @Cursor 2026-08-31 reconcile: resend evidenced in Sent; close
- **Updated:** 2026-08-31
- **Closed:** 2026-08-31
