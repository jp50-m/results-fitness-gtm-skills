---
name: inbox-command
description: Triage your email inbox and draft replies in your voice. Use when the user says "check my inbox," "what's in my email," "draft a reply to," "triage my emails," or pastes email content asking for help responding. Handles Gmail (via MCP) or pasted email text.
---

# Inbox Command

Your AI inbox manager. Scans, sorts, and drafts — so you only touch the messages that need YOU.

## When to use this skill

Trigger this skill when the user asks for help with email — checking inbox, drafting replies, deciding who to respond to, or sorting through what's new. Works whether they have Gmail MCP connected or just paste email text into the chat.

## What to ask the user (first time only)

Before running the first triage, ask these one-time questions and save the answers as memory:

1. **What does YES sound like for you?** (auto-reply with calendar link, custom warm yes, etc.)
2. **What does PASS sound like?** (polite decline template, ghost, redirect to team, etc.)
3. **Who always gets a reply, no matter what?** (key clients, family, named contacts)
4. **Your tone in 3 words?** (e.g., "warm, direct, no fluff")
5. **Sign-off?** (e.g., "— Edwina" or "Talk soon, E")

Save these to memory so future inbox runs use the same voice automatically.

## Workflow

When triggered:

1. **Pull or receive emails.** If Gmail MCP is connected, fetch unread from the last 24 hrs. Otherwise ask the user to paste the threads.

2. **Sort each email into one of four buckets:**
   - 🔴 **Needs YOU** — paying client, time-sensitive, requires your judgment
   - 🟡 **Draft & Send** — clear yes/no/info request, can be handled with a templated reply
   - 🟢 **Auto-archive** — newsletters, promos, no action needed
   - ⚫ **Spam/delete** — obvious junk

3. **For every "Needs YOU" or "Draft & Send" email, write a draft reply** in the user's saved voice. Keep replies under 6 sentences unless the email demands more.

4. **Output a single triage report** in this format:

```
INBOX TRIAGE — [date, time]

🔴 NEEDS YOU (3)
  1. [Sender] — [subject] — [why it needs you, one line]
     DRAFT: [reply text]
  2. ...

🟡 DRAFT & SEND (5)
  1. [Sender] — [subject]
     DRAFT: [reply text — short]
  2. ...

🟢 AUTO-ARCHIVE (12)
  - List of senders/subjects, one per line

⚫ SPAM (4)
  - List, one per line

Total processed: 24 emails. Time saved: ~45 min.
```

5. **Ask the user**: "Want me to send the 🟡 drafts as-is, or review them with you first?"

## Rules

- Never send an email without explicit user approval ("yes, send all 🟡" or "send #2 and #4").
- Never invent facts (meeting times, prices, commitments) — if information is missing, mark the draft `[NEEDS INPUT: ...]` and ask the user.
- Always match the user's saved tone. If no tone is saved, ask before drafting.
- For sensitive emails (legal, finance, conflict, family), default to 🔴 Needs YOU even if the request seems simple.

## What "moving the needle" looks like

A user spending 90 min/day on email should be down to 15 min/day after one week of consistent use. They only touch the 🔴 pile.
