# Lesson 8: Build Your Mini Automation — Capstone

**Time:** 30 minutes | **Type:** Hands-on | **You'll build:** A real tool you'll use every day

---

## What You'll Learn

- How to wire together everything from Lessons 1-7 into a working automation
- How to build a small, useful tool that saves you real time
- How to make it permanent so you can use it forever

---

## Concept (2 min read)

Over the past 7 lessons, you've built individual pieces:
- **CLAUDE.md** — Your project brain (Lesson 1)
- **CRAFT prompts** — Better prompt structure (Lesson 2)
- **Plan Mode** — Think before acting (Lesson 3)
- **Sub-agents** — Parallel work (Lesson 4)
- **Skills** — /brainstorm, /outline, and a custom command (Lesson 5)
- **Hooks** — Reminders, file protection, notifications (Lesson 6)
- **Prompting patterns** — 8 patterns for different situations (Lesson 7)

Now you build something real: a **mini automation** — a small, focused tool that saves you time on something you do regularly.

A mini automation is NOT a big project. It's one skill (or a combination of 2-3 skills) that automates one specific, repeatable task in your life.

---

## Exercise 1: Choose Your Automation (5 min)

Pick ONE of these, or come up with your own:

### Option A: Daily Planner
A skill that takes your task list and turns it into a prioritized day plan.

**What it does:** You paste your tasks → Claude prioritizes them, estimates time, and blocks them into a realistic schedule.

### Option B: Reading List Tracker
A skill that processes articles or content you want to read and extracts the key ideas.

**What it does:** You paste an article or URL → Claude gives you a 3-bullet summary + 1 action item.

### Option C: Note Organizer
A skill that takes messy notes and turns them into a structured document.

**What it does:** You paste raw notes → Claude organizes them into sections with headers and action items.

### Option D: Weekly Reflection
A skill that guides you through a structured weekly reflection.

**What it does:** You run `/reflect` → Claude asks you 5 questions about your week and creates a summary.

### Option E: Your Own Idea
What's a repetitive task in YOUR life that Claude could automate? Pick that.

---

## Exercise 2: Build the Skill (15 min)

### Step 1: Plan it first (Plan Mode — Lesson 3)

Before writing anything, describe what your automation should do:

"I want to build [automation name]. Here's what it should do: [description]. Before we write the skill, give me a plan: what should the SKILL.md contain? What questions should it ask (if any)? What format should the output be?"

Review Claude's plan. Adjust if needed. Approve it.

### Step 2: Create the skill folder

```bash
mkdir -p .claude/skills/[your-automation-name]
```

### Step 3: Write the SKILL.md

Create `.claude/skills/[your-automation-name]/SKILL.md`.

Follow the same format as Lesson 5:

```markdown
---
name: [skill-name]
description: [what this skill does]
argument-hint: [what to pass as an argument, if anything]
---

[Your prompt instructions here]

[Be specific about:]
- What input Claude needs
- What questions it should ask (if any)
- What format the output should be in
- Any rules or constraints
```

### Step 4: Test it

Run your skill. Does it do what you expected?

If not — go back and refine the SKILL.md. This is normal. First versions always need iteration.

---

## Exercise 3: Add a Hook (5 min)

Now make your automation smarter with a hook.

Pick one:

**Option A: Add a context reminder hook**

Fires before your skill runs and reminds Claude about your preferences:

```json
{
  "matcher": "[your-skill-name-tool]",
  "command": "echo '[Reminder about your project, tone, or format preferences]'"
}
```

**Option B: Add a file protection hook**

If your automation creates or modifies files, protect the most important ones from accidental overwrites.

**Option C: Keep the notification hook from Lesson 6**

Make sure your completion notification is still active — so you know when a long task is done.

Update your `.claude/settings.json` with your chosen hook.

---

## Exercise 4: Full Workflow Test (5 min)

Test your complete workspace by running through these checks:

### Check 1: Context
Ask: "What am I working on?"
Claude should answer from your CLAUDE.md — without you explaining anything.

### Check 2: Your automation skill
Run your new skill: `/[your-automation-name]`
It should run the full workflow as designed.

### Check 3: File protection
Ask Claude: "Edit my CLAUDE.md and remove section 2"
It should be blocked.

### Check 4: Notification
Run any task. When it finishes, you should get a notification.

### Check 5: Prompting patterns
Use one of the 8 patterns (Devil's Advocate, Role Stacking, etc.) on something real.

If all 5 checks pass — your workspace is fully operational.

---

## Your Complete Workspace

```
my-workspace/
  CLAUDE.md                         <- Your project brain
  project-context.md                <- Current project notes
  .claude/
    settings.json                   <- Hooks (format, protect, notify)
    skills/
      brainstorm/SKILL.md           <- /brainstorm [topic]
      outline/SKILL.md              <- /outline [topic]
      [your custom]/SKILL.md        <- Your custom skill from Lesson 5
      [your automation]/SKILL.md    <- Your mini automation (this lesson)
  prompts/
    session-plan-template.md        <- Session planning (from Lesson 2)
    [your craft prompts]            <- Saved CRAFT prompts
```

---

## Checkpoint

- [ ] Chose an automation and planned it first (Plan Mode)
- [ ] SKILL.md written and tested
- [ ] Skill works as expected
- [ ] Hook added to settings.json
- [ ] Full workflow test passed (all 5 checks)

---

## You're Done!

You've gone from "I can use Claude Code" to having a complete AI-powered workspace built around YOUR work.

**What you built:**
- A CLAUDE.md that gives Claude persistent context about your project
- CRAFT prompts that get great output on the first try
- A plan-first habit for complex tasks
- Sub-agent research that runs tasks in parallel
- Skills: /brainstorm, /outline, a custom skill, and a mini automation
- Hooks for formatting, file protection, and notifications
- 8 prompting patterns for any situation

**What's next?**

Ready to build something bigger?

**[Module 1: Vibe Code Your First Project](../module-1-vibe-code/)** — Take everything you learned here and build a real personal website that goes live on the internet. You'll have a URL you can share by the end.

If you're a Product Manager, check out the **[Claude Code for PMs track](https://github.com/anmolgupta824/ai-native-pm)** — the same skills applied to PM-specific workflows like PRDs, standups, and sprint planning.
