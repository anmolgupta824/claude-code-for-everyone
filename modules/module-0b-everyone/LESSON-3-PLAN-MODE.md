# Lesson 3: Plan Mode — Think Before You Act

**Time:** 15 minutes | **Type:** Hands-on | **You'll build:** A plan-first workflow for complex tasks

---

## What You'll Learn

- Why jumping straight to output is a mistake for complex tasks
- How Plan Mode works and when to use it
- How to build a plan-first habit that saves you hours of revision

---

## Concept (3 min read)

### The Problem

You ask Claude to do something complex: "Plan my move to a new city" or "Help me outline a course I want to create" or "Figure out the best way to set up my freelance business."

Claude dives right in and produces... something. It's technically an answer, but it's full of assumptions. It guessed at what you meant. It prioritized things you don't care about. It missed things that matter to you.

Now you have to tear it apart and redirect. Half your session is wasted.

### The Solution: Plan First

Instead of asking Claude to DO the thing, first ask Claude to PLAN the thing. Review the plan. Fix it. Approve it. THEN execute.

This is exactly what `/plan` does in Claude Code — it locks Claude into planning mode before acting. But you can simulate this workflow for any task, even outside of Claude Code.

### When to Use Plan Mode

Use Plan Mode when:
- The task has multiple steps or decisions to make
- Getting it wrong means a lot of rework
- You're not sure what you want yet (planning helps you figure it out)
- The output needs to match your specific situation closely

Don't use Plan Mode when:
- The task is simple and quick
- You'd rather iterate on a rough output than review a plan

---

## Exercise 1: The Plan-First Workflow (7 min)

### Step 1: Pick a complex task

Pick something from this list (or use your own project):
- Plan a 3-month learning goal (new skill, subject, or project)
- Outline a piece of writing (blog post, essay, presentation)
- Plan a side project from idea to launch
- Organize a big life decision (move, career change, big purchase)

### Step 2: Ask for a plan FIRST

Instead of: "Help me plan my move to Austin"

Type: "I want to plan a move to Austin in 3 months. Before we start, give me a high-level plan outline — the main areas to think about and decisions I'll need to make. Don't start on any of them yet. Just the plan."

### Step 3: Review and revise the plan

Look at Claude's plan. Ask yourself:
- Is anything missing?
- Is anything prioritized wrong?
- Are there sections I don't need?

Tell Claude what to change: "Remove section 3, it's not relevant. Add something about finding a neighborhood. Move housing to the top."

### Step 4: Approve and execute

Once the plan looks right, say: "The plan looks good. Let's start with [section 1]."

Now Claude executes one section at a time, with your actual priorities, not its guesses.

---

## Exercise 2: Practice on YOUR Project (5 min)

Take something from your CLAUDE.md — your actual project.

Run the plan-first workflow on a real task:

1. Ask for a plan outline
2. Review and revise it
3. Pick one section to execute

**Notice:** The output from an approved plan is almost always better than the output from a cold prompt. You spend less time editing.

---

## Quick Reference

```
Plan Mode workflow:
  1. Ask for a plan outline first
  2. Review — remove, add, reorder
  3. Approve the plan
  4. Execute one section at a time

When to use:
  - Complex, multi-step tasks
  - High-stakes outputs (important emails, big documents)
  - When you're not sure what you want

Claude Code shortcut:
  Type /plan before any task — Claude plans before acting
```

---

## Note on /plan in Claude Code

In Claude Code, you can type `/plan` before any task to automatically trigger plan mode. Claude will outline what it's going to do and wait for your approval before starting.

This is especially useful for tasks that involve writing files, making changes, or doing research — anything where you want to review the approach before Claude commits to it.

---

## Checkpoint

- [ ] Understood the plan-first workflow
- [ ] Practiced plan-first on a complex task (got a plan, revised it, approved it, executed)
- [ ] Applied it to your actual project
- [ ] Can feel the difference vs. diving straight to output

**Next:** Lesson 4 — Sub-agents (Do 5 Things at Once)
