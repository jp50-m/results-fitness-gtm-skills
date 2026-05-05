---
name: calendar-control
description: Map your week against priorities, build a daily game plan, protect deep-work blocks, and review what slipped. Use when the user says "plan my week," "what should I do today," "review my calendar," "build my game plan," "protect my time," or shares a list of meetings/tasks. Works with Google Calendar (via MCP) or pasted schedule.
---

# Calendar Control

Your AI scheduler. Builds the day around what matters, not what's loudest.

## When to use this skill

Trigger when the user asks for help planning their week or day, reviewing what they got done, protecting their time, or making sense of a packed calendar. Works with Google Calendar MCP or any pasted schedule.

## What to ask the user (first time only)

Save these as memory:

1. **Top 3 priorities for this quarter** (not this week — the bigger picture)
2. **When is your peak focus time?** (e.g., "8-11am" — defended for deep work)
3. **What does "deep work" look like for you?** (writing, building, strategic thinking — be specific)
4. **Hard NO meeting times?** (e.g., "no meetings before 10am or after 5pm")
5. **Default meeting length?** (15, 30, 45, 60 min)
6. **Energy reset rituals?** (e.g., "30 min walk after lunch," "no back-to-back calls")

## Workflow — Weekly Plan

When the user asks "plan my week" or similar:

1. **Pull the week.** Get all calendar events Mon-Fri (or Sun-Sat depending on user). If no calendar access, ask them to paste.

2. **Map every event against the saved Top 3 priorities.** Tag each one:
   - 🟢 **Aligned** — moves a Top 3 priority forward
   - 🟡 **Maintenance** — necessary but not strategic (admin, ops, recurring)
   - 🔴 **Misaligned** — doesn't serve any priority; candidate for decline/delegate/move

3. **Identify open deep-work blocks** during the user's saved peak hours. Protect them by suggesting calendar holds.

4. **Output a weekly plan** in this format:

```
WEEK OF [date]

🎯 YOUR TOP 3 THIS QUARTER
  1. [priority]
  2. [priority]
  3. [priority]

📅 WEEK MAPPED
  Mon: 4 events (2 🟢 aligned, 1 🟡, 1 🔴)
  Tue: 3 events (3 🟢)
  Wed: 6 events (1 🟢, 3 🟡, 2 🔴)  ⚠️ overcrowded
  Thu: 2 events (2 🟢)
  Fri: 5 events (1 🟢, 4 🟡)

🔴 RECONSIDER THESE
  - Wed 11am — [meeting] — doesn't serve any priority. Decline or move?
  - Wed 3pm — [meeting] — could be an email. Suggest async?

🛡️ DEEP-WORK BLOCKS TO PROTECT
  Mon 8-11am — work on [Priority 1]
  Tue 8-11am — work on [Priority 2]
  Thu 8-11am — work on [Priority 1]
  → Block these now? (yes/no)

⚖️ BALANCE
  Strategic (🟢): 8 events — 35%
  Admin (🟡):    8 events — 35%
  Misaligned (🔴): 4 events — 30%  ⚠️ above 20% threshold
```

## Workflow — Daily Game Plan

When the user asks "what should I do today" or it's morning:

1. **Pull today's events.**
2. **Build a tight game plan** in this format:

```
TODAY — [day, date]

🌅 BEFORE THE LAPTOP OPENS
  - [biggest priority task, 1 line]

🕐 SCHEDULE
  8:00–11:00 — DEEP WORK: [topic]
  11:00–11:30 — [meeting] — prep: [1 line]
  ...

⚠️ WATCH OUT
  - 2pm meeting will likely run over. Build in 15 min buffer after.
  - You have 4 calls back-to-back from 1-4pm. No reset time.

🎯 WIN CONDITION
  If you only do ONE thing today, do this: [the thing]
```

## Workflow — Evening Review

When the user says "what slipped" or "end of day":

1. Compare today's plan vs. what actually happened (if calendar shows reschedules/no-shows).
2. Output a 3-line review:
   - What got done (wins)
   - What slipped (and why, if known)
   - What to carry to tomorrow

## Rules

- Never suggest blocking time the user has marked as a hard NO.
- Always defend the saved peak focus hours first. Build the rest of the day around them.
- If the calendar shows >40% misaligned meetings, flag it as a structural problem — not just a weekly tweak.
- Never tell the user what their priorities should be. Surface the misalignment; let them decide.

## What "moving the needle" looks like

After two weeks: user wakes up knowing exactly what to do first, has 6+ hours of protected deep-work time per week, and stops ending the week wondering where the time went.
