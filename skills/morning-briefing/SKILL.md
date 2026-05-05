---
name: morning-briefing
description: Get a full morning briefing — trending AI news, your calendar, emails that need replies, and social media stats. All before you open your laptop.
---

Give me my morning briefing. Sub-command: $ARGUMENTS

## PURPOSE

Start every day with a complete briefing delivered in under 2 minutes. This skill pulls together everything you need to know before your day starts — no more checking 5 different apps.

---

## WORKFLOW

### STEP 1: TRENDING AI NEWS

Search for the top 3-5 AI stories from the last 24 hours:
- Major company announcements (Google, OpenAI, Anthropic, Meta, Microsoft)
- New tool launches or major updates
- Viral AI posts or demos

Use WebSearch to find breaking news. Format as quick bullet points with one-line summaries.

### STEP 2: CALENDAR CHECK

Check today's calendar using the Google Calendar connector:
- List all events for today with times
- Flag any conflicts or back-to-back meetings
- Highlight the most important meeting of the day

### STEP 3: EMAIL TRIAGE

Check Gmail for emails that need attention:
- Unread emails from the last 12 hours
- Flag anything urgent or time-sensitive
- Draft one-line suggested replies for the top 3 priority emails

### STEP 4: SOCIAL MEDIA STATS

Pull quick stats from Instagram:
- Follower count (current)
- How the last post is performing (likes, comments, saves)
- Any DMs or comments that need a response

### STEP 5: DELIVER THE BRIEFING

Format everything as a clean, scannable briefing:

```
## ☀️ Morning Briefing — [DATE]

### 📰 AI News
- [Story 1]: [one-line summary]
- [Story 2]: [one-line summary]
- [Story 3]: [one-line summary]

### 📅 Today's Calendar
- [Time] — [Event]
- [Time] — [Event]
⚠️ [Any conflicts or notes]

### 📧 Emails That Need You
1. [Sender] — [Subject] → Suggested reply: "[one-liner]"
2. [Sender] — [Subject] → Suggested reply: "[one-liner]"
3. [Sender] — [Subject] → Suggested reply: "[one-liner]"

### 📊 Social Stats
- Followers: [count]
- Last post: [likes] likes, [comments] comments, [saves] saves
- [Any DMs or comments flagged]

### 🎯 Top Priority Today
[One sentence on what matters most today]
```

Keep it short. Keep it scannable. The whole briefing should take under 60 seconds to read.
