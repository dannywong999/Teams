# Task board

Canonical ledger for **all** Architelier work items — open, waiting, and done.

`@Cursor` (Teams) **instructs**. Grok Bot **Outstanding** **tracks**. They share this file.

- Time zone: `America/Vancouver`
- Next ID: `T-026`
- Last refreshed: 2026-09-01 (weekday 08:00 America/Vancouver Cloud Agent reconcile: Gmail + Drive + Calendar)
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
| T-005 | P1 | open | The Key | Site visit **today** 1 Sep 11:00; read unread CF-2026-002887 |
| T-017 | P1 | open | 4488 Main | Unread VCH sink-label ask + unread CoV completeness; draft only |
| T-003 | P1 | open | 750 Pacific | Review unread DP-2026-00681 city update; draft only |
| T-004 | P1 | open | Vulcan Way | Draft 3.2.2.76 update for Avan; do not send |
| T-006 | P1 | open | Farm market | Weekend package promise (28 Aug) has passed; still unsent |
| T-016 | P2 | open | Medora Seymour | Unread Hark firestop submittal 1 Sep; review; do not invent |
| T-018 | P2 | open | Kamloops office | Unread MAK new-project mail; draft only |
| T-019 | P2 | open | May Nails Lounge | CoV comments need Danny’s seal; draft; do not send |
| T-014 | P2 | open | 501 Nelson | Draft reply to Coquitlam additional-unit mail; do not send |
| T-013 | P2 | open | 5514 Smith Ave | Draft height/excavation response for Danny; do not send |
| T-015 | P2 | open | Dr. Au Hastings | City notes 26 Aug; schedules/drawings still unrevised |
| T-002 | P2 | open | Teams | Reply to Microsoft case 2608310010000403 |
| T-001 | P2 | open | Grok Bot | Create Bot Outstanding and weekday routine |
| T-012 | P3 | waiting | Capital Direct | Comments sent 1 Sep; wait on SSDG |
| T-011 | P3 | waiting | CU Vision | Danny replied 30 Aug; wait on contractor / SE |
| T-008 | P3 | waiting | Hair salon | Revised IFP sent 31 Aug; wait on city occupancy |
| T-010 | P3 | waiting | Oak Station Dental | Danny replied 31 Aug; wait on designer / client |
| T-009 | P3 | waiting | ATR Expansion | Danny 1 Sep: use prior spreadsheet; wait on Tracy |
| T-020 | P3 | waiting | Dr Sharma | Washroom dimension sent 1 Sep; wait on Medcorp |
| T-021 | P3 | waiting | Symmetry Lighting | Closeout list sent 1 Sep; wait on contractor |
| T-022 | P3 | waiting | 22339 48 Ave | Code comments sent 1 Sep; wait on Canadian Blueprint |
| T-023 | P3 | waiting | Evolution New West | PID/legal reply sent 1 Sep; wait on Fusion |
| T-024 | P3 | waiting | Scupper | Drawing-change note sent 1 Sep; wait on SBA |
| T-025 | P3 | waiting | Vancity Chinatown | Danny replied 1 Sep on coordination meeting |

## Records

### T-001 — Create Grok Bot Outstanding
- **Status:** open
- **Priority:** P2
- **Project:** Grok Bot
- **Description:** Standing tracker in Cursor. Sign in as dwong@architelier.com (Pro+ includes Grok Bot). Create Bot `Outstanding` from `bots/outstanding.md`. Weekday 08:00 America/Vancouver routine reconciles this file. Until that Bot exists, this Cloud Agent runs the same weekday refresh (Gmail + Drive + Calendar → this file). No mail is sent.
- **Next:** Create the Bot, paste profile, save skill, enable the weekday routine, test once. Then this Cloud Agent stops covering the 08:00 run.
- **Source:** this workspace; Cursor support (ticket T-F24808) confirmed Grok account link is permanent — do not delete dwong@architelier.com to move SuperGrok
- **Last instruction:** @Cursor 2026-09-01 weekday 08:00: still no Bot (zero sand agents); Cloud Agent weekday timer covers the refresh until T-001 is done (timer expires 2026-09-07; renew-weekday-outstanding-timer already set)
- **Updated:** 2026-09-01

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
- **Last instruction:** @Cursor 2026-09-01 weekday 08:00: still unread city mail → keep P1
- **Updated:** 2026-09-01

### T-004 — 13631 Vulcan Way Unit 125 code analysis
- **Status:** open
- **Priority:** P1
- **Project:** Vulcan Way
- **Description:** Avan asked to update BCBC 3.2.2.76 and send the code analysis. Building Permit 26-019802. Draft for Danny’s review; do not send unless asked. Do not invent code conclusions.
- **Next:** Draft the 3.2.2.76 update and hold for Danny
- **Source:** Avan Chen, 28 Aug 21:27 Pacific, still UNREAD
- **Last instruction:** @Cursor 2026-09-01 weekday 08:00: Avan still unread → keep P1
- **Updated:** 2026-09-01

### T-005 — The Key site visit
- **Status:** open
- **Priority:** P1
- **Project:** The Key
- **Description:** Site visit with the City **today** Tuesday 1 Sep 2026, 11:00–12:00 Pacific (Troy Felix / Mercury Contracting invite in Gmail). Unread forward CF-2026-002887 (access) from Troy. Invite is **not** on the Google Calendar this run (calendar empty for the next 7 days — do not put personal events on this board).
- **Next:** Read unread CF-2026-002887; prep / attend 1 Sep 11:00. Draft a city reply only if needed; do not send.
- **Source:** troy@mercurycontracting.com, 28 Aug, UNREAD city forward + Gmail invite
- **Last instruction:** @Cursor 2026-09-01 weekday 08:00: visit is **today** 11:00; CF letter still unread; still not on Google Calendar → keep P1
- **Updated:** 2026-09-01

### T-006 — Farm market list package
- **Status:** open
- **Priority:** P1
- **Project:** Farm market
- **Description:** Danny told Dave (WHG Design) on 28 Aug he would package the farm-market list **this weekend** (29–30 Aug). That window has passed. Thread still unread. This is the Dave / WHG list package, not a separate Kerr Street filing.
- **Next:** Assemble the package and draft (or send only if Danny says send) to Dave
- **Source:** dave@whgdesign.ca, 27–28 Aug, UNREAD
- **Last instruction:** @Cursor 2026-09-01 weekday 08:00: still no sent package → keep P1
- **Updated:** 2026-09-01

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
- **Description:** Existing painting room (Engraving Room, Unit 12) is not to current code. Danny advised using the new paint booth. Tracy sent an equipment-list spreadsheet 31 Aug. Danny replied 1 Sep 05:52 Pacific: update the previous spreadsheet instead of separate tabs.
- **Next:** Wait on Tracy / client. No chase unless Danny asks.
- **Source:** Tracy / Aerojet, 31 Aug–1 Sep; Danny sent 1 Sep 05:52 Pacific
- **Last instruction:** @Cursor 2026-09-01 weekday 08:00: equipment-list reply sent; keep waiting
- **Updated:** 2026-09-01

### T-010 — Oak Station Dental / Dr. Chris Low
- **Status:** waiting
- **Priority:** P3
- **Project:** Oak Station Dental
- **Description:** Courtney (Opal) sent permit bases 14 Aug for 1055 West Broadway Unit 201. Gary followed up 28 Aug. Danny replied 31 Aug 05:30 Pacific: submit with the attached drawing; M&E not required for dental-office acceptance; application documents still needed. Drive folder `2602 - 1055 West Broadway, Unit 201 (Chris)`. Job #2602.
- **Next:** Wait on designer / client. No chase unless Danny asks.
- **Source:** courtney@opaldesignstudio.ca / gary@medcorp.ca; Danny sent 31 Aug 05:30 Pacific
- **Last instruction:** @Cursor 2026-08-31 weekday 08:00: Danny replied; ball elsewhere → waiting P3
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
- **Status:** waiting
- **Priority:** P3
- **Project:** Capital Direct
- **Description:** Patricia (SSDG) sent code items 27 Aug, including whether the new shower room must be accessible. Danny asked for CAD 28 Aug. Ellen followed up on corridor widths. Danny replied 1 Sep 07:53 Pacific: minor comments attached; turning radius looks fine. Drive folder `2604 - 555 West 8th Avenue, Unit 305 (Capital)` opened 1 Sep.
- **Next:** Wait on SSDG. No chase unless Danny asks.
- **Source:** pcho@ssdg.com / epeterson@ssdg.com; Danny sent 1 Sep 07:53 Pacific
- **Last instruction:** @Cursor 2026-09-01 weekday 08:00: comments sent; ball elsewhere → waiting P3
- **Updated:** 2026-09-01

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

### T-016 — Medora Medical Clinic 1065 Seymour field reviews
- **Status:** open
- **Priority:** P2
- **Project:** Medora Seymour
- **Description:** Aman (Aquavolt) sent rough-in field review reports 28 Aug for Medora Medical Clinic/Pharmacy at 1065 Seymour St (job 25163). Danny replied 31 Aug 08:00 Pacific “As attached.” Hark forwarded an unread 1 Sep firestop submittal and letter. Drive folder `2509 - 1065 Seymour Street (Medora)`. Do not invent permit conclusions.
- **Next:** Read the unread Hark firestop forward. Draft any architect reply for Danny. Do not send.
- **Source:** aman@aquavolt.ca 28 Aug; Hark 1 Sep 03:08 UTC, UNREAD
- **Last instruction:** @Cursor 2026-09-01 weekday 08:00: unread firestop → open P2
- **Updated:** 2026-09-01

### T-017 — 4488 Main St DB-2026-02496 / VCH
- **Status:** open
- **Priority:** P1
- **Project:** 4488 Main
- **Description:** Unread City of Vancouver completeness follow-up from Joy Chen 31 Aug (contractor Richmond business license still needed) and unread DB-2026-02496 application update the same evening. VCH (Jennifer Kassimatis) asked 31 Aug–1 Sep about equipment and owners; Danny replied twice; latest VCH mail is **unread**: label sinks (handwashing / food prep / mop). Do not invent health or permit conclusions.
- **Next:** Read the unread VCH and CoV mail. Draft sink labels and any completeness reply for Danny. Do not send.
- **Source:** Jennifer.Kassimatis@vch.ca UNREAD 31 Aug 17:47 Pacific; Joy.Chen@vancouver.ca UNREAD 31 Aug 15:18 Pacific; permits@vancouver.ca UNREAD 31 Aug 15:22 Pacific
- **Last instruction:** @Cursor 2026-09-01 weekday 08:00: new from unread city + VCH → P1
- **Updated:** 2026-09-01

### T-018 — Kamloops office reno (MAK)
- **Status:** open
- **Priority:** P2
- **Project:** Kamloops office
- **Description:** Unread 1 Sep mail from Colin (MAK Interiors): small office reno in Kamloops — new office and a second washroom; plan attached; mechanical mentioned. No Architelier reply.
- **Next:** Read the unread mail and attached plan. Draft a reply for Danny. Do not send. Do not invent code conclusions.
- **Source:** colin@makinteriors.ca, 1 Sep 04:19 UTC, UNREAD
- **Last instruction:** @Cursor 2026-09-01 weekday 08:00: new from unread client mail, P2
- **Updated:** 2026-09-01

### T-019 — May Nails Lounge CoV comments
- **Status:** open
- **Priority:** P2
- **Project:** May Nails Lounge
- **Description:** James (jamesyeerid.com) sent 31 Aug CoV additional comments from Brandon. Both items require Danny’s seal. Energy Statement placed on the cover sheet. No Architelier reply in-thread.
- **Next:** Review the CoV comments and draft sealed responses for Danny. Do not send. Do not invent permit conclusions.
- **Source:** james@jamesyeerid.com, 31 Aug 11:32 Pacific
- **Last instruction:** @Cursor 2026-09-01 weekday 08:00: new from CoV seal request, P2
- **Updated:** 2026-09-01

### T-020 — Dr. V. Sharma washroom dimensions
- **Status:** waiting
- **Priority:** P3
- **Project:** Dr Sharma
- **Description:** Gurv (Medcorp) sent finished wall-to-wall measurements for the universal washroom 31 Aug. Danny replied 1 Sep 07:24 Pacific: need 5'-0" from the edge of the counter to the opposite wall with the door.
- **Next:** Wait on Medcorp / designer. No chase unless Danny asks.
- **Source:** gurv@medcorp.ca 31 Aug; Danny sent 1 Sep 07:24 Pacific
- **Last instruction:** @Cursor 2026-09-01 weekday 08:00: new, status waiting
- **Updated:** 2026-09-01

### T-021 — Symmetry Lighting 1991 Franklin closeout
- **Status:** waiting
- **Priority:** P3
- **Project:** Symmetry Lighting
- **Description:** Susmitha (Merola) asked 31 Aug for closeout documents. Danny replied 1 Sep 07:16 Pacific: obtain Schedule CB from mech and structural; seismic sign-off; FA and sprinkler verification; emergency light testing; current photos.
- **Next:** Wait on contractor. No chase unless Danny asks.
- **Source:** Susmitha@merolacon.com 31 Aug; Danny sent 1 Sep 07:16 Pacific
- **Last instruction:** @Cursor 2026-09-01 weekday 08:00: new, status waiting
- **Updated:** 2026-09-01

### T-022 — 22339 48 Ave contract drawings
- **Status:** waiting
- **Priority:** P3
- **Project:** 22339 48 Ave
- **Description:** Canadian Blueprint sent a nearly complete set 31 Aug (Team Cannabis). Danny replied 1 Sep 06:58 Pacific with drawing comments (classification, universal washroom, accessible counter, area, storage door). Do not invent code conclusions beyond what Danny already sent.
- **Next:** Wait on Canadian Blueprint. No chase unless Danny asks.
- **Source:** design@canadianblueprint.ca 31 Aug; Danny sent 1 Sep 06:58 Pacific
- **Last instruction:** @Cursor 2026-09-01 weekday 08:00: new, status waiting
- **Updated:** 2026-09-01

### T-023 — Evolution Canada 11 Eighth St BP015516
- **Status:** waiting
- **Priority:** P3
- **Project:** Evolution New West
- **Description:** Fusion (Tushar / Sandra) forwarded City of New Westminster PID / legal-description questions 31 Aug for Units 1102 & 1200. Danny replied 1 Sep 06:04 Pacific: ask the city to check again; documents have been signed repeatedly.
- **Next:** Wait on Fusion / city. No chase unless Danny asks.
- **Source:** tbarot@fusion-projects.com / schapman@fusion-projects.com 31 Aug; Danny sent 1 Sep 06:04 Pacific
- **Last instruction:** @Cursor 2026-09-01 weekday 08:00: new, status waiting
- **Updated:** 2026-09-01

### T-024 — Scupper drawing change (SBA)
- **Status:** waiting
- **Priority:** P3
- **Project:** Scupper
- **Description:** Danny sent 1 Sep 07:14 Pacific to Gurmukh (SBA): look at the attached and alter drawings to suit; talk first about how they plan to change.
- **Next:** Wait on SBA. No chase unless Danny asks.
- **Source:** Danny sent 1 Sep 07:14 Pacific to gurmukh.singh@sba-dnc.com
- **Last instruction:** @Cursor 2026-09-01 weekday 08:00: new, status waiting
- **Updated:** 2026-09-01

### T-025 — Vancity Chinatown consultant coordination
- **Status:** waiting
- **Priority:** P3
- **Project:** Vancity Chinatown
- **Description:** SSDG (Lindsay Reid) sent a consultant coordination meeting invite 31 Aug (Danny on cc). Danny replied 1 Sep 07:01 Pacific that he may not stay for the full meeting.
- **Next:** Wait on the coordination meeting / SSDG. No chase unless Danny asks.
- **Source:** lreid@ssdg.com 31 Aug; Danny sent 1 Sep 07:01 Pacific
- **Last instruction:** @Cursor 2026-09-01 weekday 08:00: new, status waiting
- **Updated:** 2026-09-01

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
