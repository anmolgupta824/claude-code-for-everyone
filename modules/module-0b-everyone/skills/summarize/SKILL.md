---
name: summarize
description: Summarize any text into clear, actionable bullet points
---

Summarize the following text (or the most recent content in our conversation):

$ARGUMENTS

Give me:

**In One Sentence**
The single most important takeaway. Start with the conclusion, not the setup.

**Key Points** (3-5 bullets)
The most important ideas. Each bullet should be a complete, specific thought — not a vague summary.

**Action Items** (if applicable)
Any decisions, tasks, or next steps suggested by this content.

Rules:
- Cut anything that's just padding, filler, or repetition
- Use plain language — avoid jargon unless it's essential
- If no text is provided in $ARGUMENTS, summarize the last document or content discussed in this session
