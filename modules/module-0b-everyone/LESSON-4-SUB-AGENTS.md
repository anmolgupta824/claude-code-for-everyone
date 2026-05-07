# Lesson 4: Sub-agents — Do 5 Things at Once

**Time:** 15 minutes | **Type:** Hands-on | **You'll build:** Parallel research and multi-task execution

---

## What You'll Learn

- What sub-agents are and how they work
- When to use parallel tasks vs. sequential work
- How to run a real multi-task research job in this session

---

## Concept (3 min read)

### The Problem

You want to research 4 different things before making a decision. Or you have 3 independent tasks that all need to get done. Claude does them one at a time. Task 1, wait. Task 2, wait. Task 3, wait.

If each task takes 30 seconds, you're waiting 90 seconds total. But more importantly — Claude's context fills up as it chains tasks. Later tasks get worse because earlier tasks are clogging the window.

### The Solution: Sub-agents

Sub-agents let Claude run multiple tasks IN PARALLEL. Claude spins up separate "agents" — each one handles one task independently, without affecting the others. They run simultaneously and report back.

**The result:**
- Faster (parallel, not sequential)
- Better quality (each agent has a clean, focused context)
- More thorough (more ground covered in less time)

### When to Use Sub-agents

Good use cases:
- Research multiple options at the same time (compare 3 tools, read 4 articles, investigate 5 questions)
- Do independent tasks that don't depend on each other
- Generate multiple drafts in parallel and pick the best one

Not worth it when:
- Tasks depend on each other (Task B needs results from Task A)
- You only have 1-2 tasks (overhead isn't worth it)
- You need one coherent output (use regular chat instead)

---

## Exercise 1: Watch Sub-agents in Action (5 min)

### Step 1: Give Claude a parallel research task

Try this prompt (or adapt it to your project):

```
I need to research [3 things relevant to your project]. Run these as parallel sub-agents and report back what you find:

1. [Research question 1]
2. [Research question 2]
3. [Research question 3]

For each one, give me: a 3-sentence summary and 2-3 key takeaways.
```

**Example for a freelancer:**
```
I'm deciding what tools to use for my freelance writing business. Run these as parallel sub-agents:

1. Compare Notion vs. Obsidian for writing and project management
2. What are the best invoicing tools for freelancers under $20/month?
3. What are the most effective ways to get freelance writing clients in 2025?

For each: 3-sentence summary + 2-3 key takeaways.
```

### Step 2: Watch the output

Notice:
- Claude runs all 3 tasks simultaneously
- Each report is clean and focused (no cross-contamination)
- You get comprehensive research in one shot

---

## Exercise 2: Apply Sub-agents to YOUR Project (5 min)

Think about your CLAUDE.md project. What are 3 independent questions you could research right now?

Write your own parallel research prompt and run it.

**Prompts to adapt:**
- "Compare these 3 approaches to [problem]: ..."
- "Research these 3 topics for my project: ..."
- "Generate 3 independent drafts of [thing], each with a different angle: ..."

---

## Quick Reference

```
When to use sub-agents:
  - Research multiple options simultaneously
  - Independent tasks (don't depend on each other)
  - Generate multiple drafts in parallel

How to trigger:
  - "Run these as parallel sub-agents: ..."
  - "Do these tasks simultaneously: ..."
  - Claude will spin up separate agents automatically

Format tip:
  Ask each agent to return a consistent format
  (e.g., "3-sentence summary + 2-3 key takeaways")
  Makes it easy to compare results
```

---

## Checkpoint

- [ ] Understood what sub-agents are and when to use them
- [ ] Ran a parallel research task and got simultaneous results
- [ ] Applied sub-agents to your own project
- [ ] Can see the speed and quality difference vs. sequential tasks

**Next:** Lesson 5 — Skills (Reusable Slash Commands)
