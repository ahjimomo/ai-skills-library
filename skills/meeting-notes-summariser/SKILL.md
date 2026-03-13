---
name: meeting-notes-summariser
description: Turn raw meeting notes or transcripts into a clean summary with clearly labelled action items, decisions, and owners.
category: Synthesis & Insights
type: Reusable Instruction
---

# Meeting Notes Summariser
Turn raw meeting notes or transcripts into a clean, structured summary — with action items, decisions, and owners clearly separated.

## When to Activate
Activate this skill when the user:
- Shares meeting notes, bullet points, or a transcript and asks for a summary
- Uses phrases like "summarise my meeting", "write up my notes", "extract action items", or "what did we decide"
- Pastes a block of unstructured text that appears to be from a meeting or discussion
- Asks for a follow-up email or recap based on meeting content

Do not activate for general summarisation tasks unrelated to meetings or discussions.

## When to Use It
- You have just finished a meeting and need to send a summary to attendees
- You have a transcript or rough notes and want to extract what actually matters
- You want to make sure nothing fell through the cracks — decisions, actions, and owners all accounted for
- You need a record of what was discussed that is easy to reference later
- You are summarising on behalf of someone who could not attend

## What It Does
Takes raw meeting notes, bullet points, or a full transcript and structures it into four clear sections: a short summary of what was discussed, decisions made organised by topic, a table of action items with owners and deadlines, and a proposed agenda for the next meeting. Nothing is invented — if something was not in the notes, it will not appear in the output.

## How to Use It

**Option A — For Claude users (via Skills)**
1. Open the skill file on GitHub ↗ and download `SKILL.md`
2. Place the file in your Claude skills folder — `~/.claude/skills/meeting-notes-summariser/SKILL.md` for personal use, or `.claude/skills/meeting-notes-summariser/SKILL.md` inside your project directory for project use
3. The skill will be available automatically in your next Claude conversation

*Note: This applies to personal and project use. Enterprise and plugin setups have separate configuration — check with your administrator.*

**Option B — Copy and paste the instruction**
1. Copy the full instruction from the section below
2. Open a new conversation in your preferred AI tool and paste it in
3. Paste your meeting notes or transcript directly into the chat
4. If you want the summary in a specific format (e.g. email-ready, bullet points only), say so at the start

## The Instruction
Copy the full text below and paste it into a new conversation.

```
You are a professional meeting facilitator and note-taker.

When I give you meeting notes, bullet points, or a transcript, first extract the following meeting details if available:

**Meeting Details**
- Subject / Title:
- Date:
- Time:
- Attendees:

If any of these details are not mentioned in the notes, write "Not mentioned" in the relevant field.

Then structure the rest of the output into four sections:

**Section 1 — Meeting Summary**
Write a short paragraph (3–5 sentences) summarising what was discussed. Cover the main topics and the overall outcome of the meeting. Do not include action items or decisions here — those go in their own sections.

**Section 2 — Decisions Made**
Organise decisions by topic. For each topic, use a subtitle and list the decisions made under it as bullet points. If decisions span only one topic, a single subtitle is fine. If no decisions were made, write "No decisions recorded."

Format:
### [Topic Name]
- Decision one
- Decision two

**Section 3 — Action Items**
List every action item in a table with four columns: Action, Owner, Deadline, and Status. Set all Status values to "Open" by default.

| Action | Owner | Deadline | Status |
|--------|-------|----------|--------|
| Description of action | Name or team | Date or timeframe | Open |

If the owner or deadline was not mentioned, write "Not assigned" or "No deadline set" in the relevant field.

**Section 4 — Next Meeting**
If a next meeting was discussed, include:
- Date and time (if mentioned)
- Proposed agenda items as a bullet list

If no next meeting was discussed, write "Not discussed."

**Important rules:**
- Only include information that appears in the notes provided. Do not infer, assume, or add context that was not stated.
- If something is ambiguous — for example, it is unclear who owns an action — flag it using "Flagged for review:" so the user can clarify.
- If the notes are incomplete or difficult to parse, note this at the top of your response and do your best with what is available.
- If I ask for a specific output format at the start (e.g. email-ready, Notion-ready), apply that format while keeping the four-section structure.
```

## Guardrails & Accuracy Checks

**Built into this skill**
- Claude will only summarise what is in the notes — nothing is inferred or added
- Ambiguous ownership or missing deadlines are flagged explicitly rather than guessed
- Incomplete or unclear notes are flagged at the top of the response
- Missing meeting details are marked as "Not mentioned" rather than left blank or guessed

**Before you act on the output, check**
- [ ] Are the meeting details (date, time, attendees) correct?
- [ ] Does the summary accurately reflect what was discussed, or has anything been missed or misrepresented?
- [ ] Are all decisions listed ones that were actually agreed upon — not just discussed?
- [ ] Do all action items have a real owner, or have any been left as "Not assigned" that should have one?
- [ ] Is the next meeting date and agenda correct?
- [ ] Did Claude flag anything for review? If yes, resolve those before sending the summary
- [ ] If you are sending this to others, has a meeting participant reviewed it for accuracy before it goes out?

## Example Output

**Meeting Details**
- Subject / Title: Q2 Roadmap Review
- Date: 12 March 2026
- Time: 10:00 AM SGT
- Attendees: Sarah (Product), James (Engineering), Priya (Data), Marcus (Design)

---

**Meeting Summary**

The team met to review progress on the Q2 product roadmap and discuss priorities for the next sprint. Key topics included the delay to the mobile feature release, resourcing for the data migration project, and the upcoming client demo on 20 March. The team agreed to deprioritise two roadmap items to free up capacity, and demo preparation was assigned to the product team.

---

**Decisions Made**

### Mobile Feature Release
- The mobile feature release will be pushed to the end of Q2
- Two lower-priority roadmap items will be deprioritised to free up engineering capacity

### Data Migration
- Resourcing for the data migration project will be reviewed at next week's leadership meeting

### Client Demo
- The client demo on 20 March will be led by the product team

---

**Action Items**

| Action | Owner | Deadline | Status |
|--------|-------|----------|--------|
| Update roadmap to reflect revised mobile release date | Sarah | End of week | Open |
| Prepare demo script and slide deck | Product team | 17 March 2026 | Open |
| Send resourcing proposal to leadership | Flagged for review: owner not confirmed | No deadline set | Open |

---

**Next Meeting**
- Date and time: 19 March 2026, 10:00 AM SGT
- Proposed agenda:
  - Leadership resourcing decision update
  - Demo rehearsal sign-off
  - Sprint planning for Q2 remainder
