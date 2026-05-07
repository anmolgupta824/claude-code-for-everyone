# Lesson 7: Advanced Prompting Patterns

**Time:** 20 minutes | **Type:** Hands-on | **You'll learn:** 8 patterns that unlock a different level of output

---

## What You'll Learn

- 8 proven prompting patterns and when to use each
- How to apply them to your actual work
- How to combine patterns for complex tasks

---

## Concept (2 min read)

You already know CRAFT (Lesson 2). That's Pattern 1. But there are 7 more patterns that unlock very specific behaviors in Claude.

Each pattern is a different way to shape how Claude thinks and responds. Once you know them, you'll reach for the right one instinctively — like a chef who grabs the right knife without thinking.

---

## The 8 Patterns

---

### Pattern 1: CRAFT (Review)

**When to use:** Any time you want high-quality, well-structured output on the first try.

**Format:**
```
Context: [situation]
Role: [who Claude should be]
Action: [what to do]
Format: [how to structure output]
Tone: [voice/style]
```

**Example:**
```
Context: I'm writing a newsletter for indie hackers. This week's topic is building an audience before launching.
Role: You're a growth writer who's built audiences from scratch.
Action: Write a 500-word newsletter intro that hooks readers in the first sentence.
Format: Short paragraphs, no headers, conversational flow.
Tone: Direct, practical, no fluff.
```

---

### Pattern 2: Socratic Method

**When to use:** You're not sure what you want yet. Use Claude to help you figure it out.

**Format:** "Ask me questions about [topic] to help me clarify [goal]. Ask them one at a time."

**Example:**
```
I want to start a side project but I'm not sure what to build. Ask me questions one at a time to help me narrow it down. Don't suggest ideas — just ask questions.
```

Claude asks, you answer, your thinking gets clearer. Use this before any big decision.

---

### Pattern 3: Role Stacking

**When to use:** You need multiple perspectives on the same output (writing, decision, plan).

**Format:** "Review this as [Role 1], then as [Role 2], then as [Role 3]."

**Example:**
```
Review my website copy as:
1. A first-time visitor who knows nothing about me
2. A skeptical buyer who needs to be convinced
3. A copywriter looking for weak spots

For each role, give 2-3 specific observations.
```

---

### Pattern 4: The 3-Draft Method

**When to use:** Creative work where you're not sure what direction is best.

**Format:** "Write 3 versions of [thing]. Make each one clearly different from the others: [Version A], [Version B], [Version C]."

**Example:**
```
Write 3 versions of my Twitter bio:
Version A: Professional and credibility-focused
Version B: Casual and personality-forward
Version C: Outcome-focused (what I help people do)

Keep each under 160 characters.
```

You'll probably end up mixing elements from all three. That's the point.

---

### Pattern 5: Devil's Advocate

**When to use:** Before you commit to a decision or plan. Force Claude to challenge you.

**Format:** "Here's my plan: [plan]. Play devil's advocate. What are the strongest arguments against this? What am I missing?"

**Example:**
```
I'm planning to quit my job in 3 months to freelance full-time. I have 2 clients lined up and 4 months of savings.

Play devil's advocate. What are the strongest arguments against doing this? What scenarios am I not thinking about? Be brutally honest.
```

This is one of the highest-value uses of Claude. It finds your blind spots.

---

### Pattern 6: Constraints-First

**When to use:** When you're tempted to write a very open-ended prompt. Constraints produce better output.

**Format:** "Write [thing]. Constraints: [list]. Non-negotiable: [hard rules]."

**Example:**
```
Write a cold email to a potential client.

Constraints:
- Under 100 words
- No buzzwords ("synergy", "leverage", "reach out")
- One clear ask in the last sentence
- Don't mention my company name until sentence 2

Non-negotiable: No exclamation points. Ever.
```

---

### Pattern 7: Teach It Back

**When to use:** After Claude explains something complex. Verify you actually understood it.

**Format:** "I'm going to explain [concept] back to you. Tell me where I'm wrong or what I'm missing."

**Example:**
```
I'm going to explain how hooks work in Claude Code:

"Hooks are rules I set in settings.json that run shell commands when Claude does things like write files or finish responding. I can use them to block Claude from touching certain files by making the command exit with code 2."

Where am I wrong? What did I miss?
```

This is how you actually learn something, not just think you learned it.

---

### Pattern 8: The Reverse Brief

**When to use:** When you want to test if your instructions are clear enough.

**Format:** "Before doing the task, summarize what you think I'm asking for. What are the key constraints? What would success look like?"

**Example:**
```
Before doing anything, summarize what you think I'm asking for: write a landing page for a productivity app targeting remote workers. What are the key constraints? What does success look like for this page?
```

If Claude's summary doesn't match what you wanted — fix the prompt before it does the work.

---

## Exercise: Apply 3 Patterns to Your Work (10 min)

Pick 3 patterns from the list above. Apply each one to something from YOUR project (from your CLAUDE.md).

For each:
1. Write the prompt using the pattern
2. Run it
3. Note: what was different about the output vs. your normal prompts?

---

## Quick Reference

```
CRAFT:             Structure any prompt for quality output
Socratic:          Ask questions to clarify your own thinking
Role Stacking:     Get multiple expert perspectives at once
3-Draft Method:    Generate options, then choose or blend
Devil's Advocate:  Challenge your plans and decisions
Constraints-First: Better output through explicit limits
Teach It Back:     Verify you actually understood something
Reverse Brief:     Test if your instructions are clear
```

---

## Checkpoint

- [ ] Read all 8 patterns
- [ ] Applied 3 patterns to your actual project
- [ ] Noticed the difference in output quality vs. basic prompts
- [ ] Can describe when to use each pattern

**Next:** Lesson 8 — Build Your Mini Automation (Capstone)
