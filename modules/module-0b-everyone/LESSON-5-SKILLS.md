# Lesson 5: Skills — Reusable Slash Commands

**Time:** 20 minutes | **Type:** Hands-on | **You'll build:** 3 working slash commands

---

## What You'll Learn

- What Skills are and how they work
- How to create a SKILL.md file
- How to pass arguments to skills (e.g., `/research productivity habits`)

---

## Concept (3 min read)

### The Problem

You type the same prompts every day:
- "Brainstorm 10 ideas for [topic]"
- "Create an outline for [piece of writing]"
- "Summarize this text in 3 bullet points"
- "Research [topic] and give me the key facts"

Every time, you re-type the instructions, the format, the rules. It's tedious and inconsistent — different wording every time means different quality every time.

### The Solution: Skills

Skills are saved prompts that become slash commands. Create a file, and you can type `/brainstorm` instead of writing a 10-line prompt every morning.

**How Skills work:**
1. Create a folder: `.claude/skills/[skill-name]/`
2. Inside, create `SKILL.md` with your prompt
3. Type `/skill-name` in Claude Code — it runs the prompt

**Skills can take arguments:** `/research productivity habits` passes "productivity habits" to the skill as `$ARGUMENTS`.

> **Included files:** The complete SKILL.md files for this lesson are in this module's `skills/` folder. You can copy them directly to your workspace, or type them out for practice.

---

## Exercise 1: Build Your /brainstorm Skill (7 min)

### Step 1: Create the skills folder

```bash
mkdir -p .claude/skills/brainstorm
```

### Step 2: Create the SKILL.md file

Create `.claude/skills/brainstorm/SKILL.md` with the content below, or copy it from this module's `skills/brainstorm/SKILL.md`.

```markdown
---
name: brainstorm
description: Generate creative ideas on any topic
argument-hint: topic (e.g., "newsletter content ideas")
---

Generate 10 creative ideas for: $ARGUMENTS

Rules:
- Make each idea distinct — no two ideas should feel similar
- Be specific, not generic. "Write about morning routines" is better than "Write about productivity"
- For each idea, add a 1-sentence description of what makes it interesting or useful
- Number them 1-10
- Don't filter yourself — include wild or unexpected ideas alongside practical ones

Format:
1. [Idea title] — [1-sentence description]
2. [Idea title] — [1-sentence description]
...
```

> **Source file:** [`skills/brainstorm/SKILL.md`](./skills/brainstorm/SKILL.md)

### Step 3: Test it

In Claude Code, type:

```
/brainstorm newsletter content ideas for a freelance designer
```

Claude should generate 10 distinct, numbered ideas with descriptions.

---

## Exercise 2: Build /outline with Arguments (7 min)

### Step 1: Create the skill folder

```bash
mkdir -p .claude/skills/outline
```

### Step 2: Create the SKILL.md with arguments

Create `.claude/skills/outline/SKILL.md` with the content below, or copy it from this module's `skills/outline/SKILL.md`.

```markdown
---
name: outline
description: Create a structured outline for any piece of writing
argument-hint: topic or title (e.g., "blog post about remote work")
---

Create a detailed outline for: $ARGUMENTS

Before writing the outline, ask me:
1. Who is the audience? (who will read this)
2. What's the goal? (inform, persuade, entertain, sell?)
3. How long should the final piece be? (rough word count or "short/medium/long")

After I answer, create an outline with:
- A clear title
- 4-6 main sections (with headers)
- 2-3 bullet points under each section showing what to cover
- A suggested intro hook and closing call-to-action

Format as markdown.
```

> **Source file:** [`skills/outline/SKILL.md`](./skills/outline/SKILL.md)

### Step 3: Test it with a real topic

```
/outline blog post about how I started freelancing
```

Claude should ask you the 3 questions, then generate a structured outline.

---

## Exercise 3: Build a Custom Skill (3 min)

### Step 1: Think of something YOU do every day

What prompt do you type repeatedly? Some ideas:
- `/summarize` — Summarize long text into bullet points
- `/email-reply` — Draft a reply to an email
- `/research` — Research a topic and give key facts
- `/daily-plan` — Plan my day from a list of tasks
- `/feedback` — Give constructive feedback on a piece of writing

### Step 2: Create it

```bash
mkdir -p .claude/skills/[your-skill-name]
```

Write the SKILL.md following the same pattern:
- YAML frontmatter with name, description, and optional argument-hint
- Clear instructions for what Claude should do
- The format you want the output in

### Step 3: Test it

Type `/[your-skill-name]` and verify it works.

---

## Quick Reference

```
Skill location:    .claude/skills/[name]/SKILL.md
Activate:          /[name] in Claude Code
Arguments:         Use $ARGUMENTS in the skill body
                   User types: /brainstorm newsletter ideas
                   $ARGUMENTS becomes: newsletter ideas
Frontmatter:       name, description, argument-hint (all optional but recommended)
Personal skills:   ~/.claude/skills/ (available in all projects)
Project skills:    .claude/skills/ (only in this project)
Module skills:     All skills from this lesson are in skills/ in this module folder
```

---

## Checkpoint

- [ ] `/brainstorm` skill created and tested
- [ ] `/outline` skill created with argument support and tested
- [ ] One custom skill created for YOUR workflow
- [ ] All 3 skills live in `.claude/skills/`

**Next:** Lesson 6 — Hooks (Automate the Boring Stuff)
