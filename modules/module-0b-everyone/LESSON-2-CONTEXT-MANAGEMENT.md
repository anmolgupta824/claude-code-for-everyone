# Lesson 2: Context Management

**Time:** 15 minutes | **Type:** Hands-on | **You'll build:** CRAFT framework + session planning system

---

## What You'll Learn

- Why Claude gets worse the longer you chat (and how to fix it)
- The CRAFT framework for writing prompts that get great results every time
- How to plan a session so Claude always knows what you're trying to accomplish

---

## Concept (3 min read)

### The Problem: Context Decay

Here's something that surprises most people: Claude doesn't get better the longer you chat. It gets worse.

Why? Because every session has a context window — a limit to how much it can "remember" at once. As your conversation gets longer, earlier context gets pushed out. Claude starts forgetting what you told it at the beginning, making connections less accurately, producing lower-quality output.

### Two Solutions

**Solution 1: Better prompts (CRAFT framework)**

Most people write vague prompts like "write a blog post about productivity." Claude has to guess at everything — your audience, tone, length, format. Better prompts give Claude everything it needs upfront.

**Solution 2: Session planning**

Before a long session, write a quick plan: what you want to accomplish, what context Claude needs, what output you want. Save it as a file. Reference it at the start of every session.

### The CRAFT Framework

CRAFT stands for:

- **C — Context:** What's the situation? What does Claude need to know?
- **R — Role:** What role should Claude play? (editor, researcher, devil's advocate, expert in X)
- **A — Action:** What exactly do you want Claude to DO?
- **F — Format:** How should the output be structured? (bullets, paragraphs, table, numbered list)
- **T — Tone:** What's the voice? (casual, professional, punchy, detailed)

You don't always need all 5 — but the more you include, the better the output.

---

## Exercise 1: Write a CRAFT Prompt (5 min)

### Step 1: Think of something you need Claude to help with today

It could be:
- Writing a social media post
- Researching a topic
- Planning a project
- Drafting an email
- Brainstorming ideas

### Step 2: Write it WITHOUT CRAFT first

Type your normal prompt. See what you get.

### Step 3: Rewrite it WITH CRAFT

Now rewrite the same prompt using all 5 CRAFT elements:

**Example — Without CRAFT:**
```
Write a tweet about my new side project
```

**Example — With CRAFT:**
```
Context: I'm launching a side project — a Chrome extension that blocks social media during focus time. It's called FocusLock. My audience is knowledge workers and students.
Role: You're a Twitter copywriter who writes punchy, relatable tech content.
Action: Write 3 tweet options for a "just launched" announcement.
Format: Each tweet should be under 280 characters. Number them 1, 2, 3.
Tone: Casual, a little funny, self-aware. Not corporate.
```

**Try it yourself.** Write a CRAFT prompt for your task and paste it.

### Step 4: Compare the outputs

Look at what changed. Usually: more specific, more useful, less editing needed.

---

## Exercise 2: Build Your Session Planning Template (7 min)

### Step 1: Create a prompts folder

```bash
mkdir -p prompts
```

### Step 2: Create a session plan template

Create `prompts/session-plan-template.md`:

```markdown
# Session Plan

**Date:** [Today's date]
**Goal:** [What I want to accomplish in this session]

## Context for Claude
[2-3 sentences about where the project is right now]

## Tasks
1. [First task]
2. [Second task]
3. [Third task]

## Output Format
[How do I want the results? Bullet points? A document? A list?]

## Constraints
- [Time limit, length limit, anything to avoid]
```

### Step 3: Fill in one real session plan

Fill out this template for what you're actually trying to do today (or a project you're working on right now).

### Step 4: Start a session using it

At the start of any Claude session, paste your session plan and say: "Here's my plan for today. Let's start with Task 1."

Watch how much better the output is compared to just diving in.

---

## Exercise 3: Save a CRAFT Prompt (3 min)

Pick your best CRAFT prompt from Exercise 1. Save it as a reusable file.

Create `prompts/[name-of-task].md` — for example:
- `prompts/tweet-announcement.md`
- `prompts/blog-post-outline.md`
- `prompts/research-brief.md`

Next time you need that output, just open the file and paste the prompt. No re-writing.

---

## Quick Reference

```
CRAFT:
  C — Context: What Claude needs to know
  R — Role: Who Claude should be
  A — Action: What to do
  F — Format: How to structure output
  T — Tone: What voice to use

Session planning:
  1. Write a session plan before starting
  2. Paste it at the beginning of your session
  3. Claude knows exactly what you want

Saved prompts:
  prompts/ folder — store your best CRAFT prompts
  Reuse them instead of rewriting every time
```

---

## Checkpoint

- [ ] Wrote one prompt WITHOUT CRAFT — compared to WITH CRAFT
- [ ] Session plan template created in `prompts/`
- [ ] At least one CRAFT prompt saved in `prompts/`
- [ ] You can feel the quality difference

**Next:** Lesson 3 — Plan Mode (Think Before You Act)
