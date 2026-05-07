# Lesson 1: CLAUDE.md — Your Project Brain

**Time:** 15 minutes | **Type:** Hands-on | **You'll build:** Your personal CLAUDE.md file

---

## What You'll Learn

- What CLAUDE.md is and why every session should start with one
- How to write a CLAUDE.md that makes Claude feel like a collaborator who already knows your project
- How to test that it actually works

---

## Concept (3 min read)

### The Problem

Every time you start a new Claude Code session, Claude has amnesia. It doesn't know what you're working on, what your goals are, how you like things formatted, or what you want it to avoid. So you waste the first 5 minutes of every session re-explaining everything. And if you forget something, Claude makes assumptions that lead to bad output.

### The Solution: CLAUDE.md

Create a file called `CLAUDE.md` in your project folder. Claude Code reads it automatically at the start of every session. Think of it as a briefing doc for a new collaborator — except this collaborator reads it in 2 seconds and never forgets.

It works for any kind of project:
- A side project you're building
- A writing project (blog, book, newsletter)
- A freelance client you're doing work for
- Your job (writing, research, marketing, design)
- A hobby (music, travel planning, learning something new)

### The 5 Sections

Every good CLAUDE.md has:

1. **Who I Am** — Your role, context, what you do
2. **My Project** — What you're working on, who it's for, what success looks like
3. **My Tools** — Apps and tools you use (Notion, Figma, GitHub, Google Docs, etc.)
4. **My Preferences** — How you like outputs formatted, tone, length, terminology
5. **Rules** — What Claude should NEVER do (this is the most important section)

That's it. Let's build yours.

---

## Exercise 1: Build Your CLAUDE.md (7 min)

### Step 1: Create your workspace folder

This folder is where you'll build everything throughout this course:

```bash
mkdir -p ~/my-workspace
```

### Step 2: Answer these questions about YOUR actual project

Think about something you're currently working on — a project, job, hobby, or goal.

**Who I Am:**
- What do you do? (your job, role, or what you spend most time on)
- What's your experience level with AI tools?
- How do you prefer Claude to communicate with you? (casual/formal, short/detailed)

**My Project:**
- What are you working on right now?
- Who is it for? (yourself, a client, an audience, a team?)
- What does success look like?
- What stage is it at? (just starting / in progress / near the end)

**My Tools:**
- Where do you write or take notes? (Notion, Google Docs, Obsidian, plain text?)
- Where do you manage tasks? (Todoist, Notion, sticky notes, spreadsheet?)
- How do you communicate? (email, Slack, iMessage?)

**My Preferences:**
- Bullet points or paragraphs?
- Short and punchy or detailed and thorough?
- Any words or phrases you hate (or love)?

**Rules — What should Claude NEVER do?**
Examples:
- Never write in a formal tone (I hate corporate speak)
- Always ask questions before starting a long document
- Never make up facts or statistics
- Never suggest tools I haven't mentioned

### Step 3: Create the file

Create `CLAUDE.md` in your workspace using this template — fill in YOUR answers:

```markdown
# CLAUDE.md

## Who I Am
- [What you do / your role]
- [Your experience level with AI tools]
- [How you like Claude to communicate: casual/formal, brief/detailed]

## My Project
- **Project:** [What you're working on]
- **For:** [Who it's for]
- **Goal:** [What success looks like]
- **Status:** [Where you are now]

## My Tools
- **Writing/notes:** [Notion/Google Docs/Obsidian/etc.]
- **Tasks:** [How you track work]
- **Communication:** [Email/Slack/etc.]

## My Preferences
- [How you want outputs formatted]
- [Tone preference]
- [Length preference]
- [Any terminology or style notes]

## Rules
- NEVER [thing 1]
- ALWAYS [thing 2]
- NEVER make up facts, data, or quotes
- [Add your own rules]
```

Save this as `CLAUDE.md` in your workspace directory (the folder you just created).

---

## Exercise 2: Test It (5 min)

### Step 1: Ask Claude about your project

Try these prompts:

1. "What am I working on?"
2. "Write a 2-sentence description of my project"
3. "What tools do I use?"

**What to look for:** Claude should answer using details from your CLAUDE.md without you explaining anything.

### Step 2: Test the Rules

Try to make Claude break a rule:

- If your rule says "never be formal," ask "write a professional memo about my project"
- If your rule says "always ask questions first," ask "write a full plan for my project right now"

Claude should follow your rules. If it doesn't, make your Rules section more specific and direct.

---

## Quick Reference

```
File location:     Project root (CLAUDE.md in your working directory)
When it's read:    Automatically at session start
Sections:          Who I Am, My Project, My Tools, My Preferences, Rules
Most important:    Rules — prevents Claude from doing things you'll undo
Pro tip:           Keep it under 100 lines. Be specific, not verbose.
```

---

## Checkpoint

- [ ] Workspace folder created (`~/my-workspace`)
- [ ] `CLAUDE.md` with all 5 sections filled with YOUR real info
- [ ] Tested — Claude knows your context from CLAUDE.md
- [ ] Tested Rules — Claude follows your boundaries

**Next:** Lesson 2 — Context Management
