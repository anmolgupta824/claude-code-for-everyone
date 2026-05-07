# Lesson 1: Setup

**Time:** 10 minutes | **You'll do:** Create your project folder and initialize it with Claude Code

---

## What Happens in This Lesson

You'll create a clean folder for your website project. That's it. Simple start, real foundation.

---

## Step 1: Create Your Project Folder

In this Claude Code session, run:

```bash
mkdir -p ~/my-website
cd ~/my-website
```

This creates a folder called `my-website` in your home directory and moves into it.

> **What is a folder?** It's just a place to keep all your website files together — like a folder on your desktop, but in the terminal.

---

## Step 2: Create a CLAUDE.md for Your Website

This file tells Claude what your website project is about — so it remembers your context across every session.

Create `CLAUDE.md` with this template:

```markdown
# CLAUDE.md — My Website Project

## Project
Building a personal website to go live at a Vercel URL.

## Me
- Name: [Your name]
- What I do: [Your job, role, or passion in 1-2 sentences]
- The vibe I want: [e.g., "minimal and professional" / "bold and creative" / "warm and personal"]

## My Website Goals
- [Who is this website for? Who will visit it?]
- [What do I want visitors to do or feel?]

## Sections I want (I'll decide in Lesson 2, but rough ideas):
- [e.g., About, Work, Projects, Contact, Blog]

## My Preferences
- Colors I like: [any colors, vibes, or reference sites]
- Fonts: [modern/classic/minimal/bold — or specific font names]
- Style: [clean/playful/dark/light]

## Rules
- NEVER make up information about me — ask if you're unsure
- Keep the code simple — no complex frameworks, just HTML/CSS/JS
- Always explain what you changed in plain language
```

Fill in what you know. Leave blanks for things you'll decide in Lesson 2.

Save this as `CLAUDE.md` in your `~/my-website` folder.

---

## Step 3: Verify the Setup

Check that everything is in place:

- You're inside the `~/my-website` folder
- `CLAUDE.md` exists with your info filled in (at least partially)

Ask Claude: "What's my website project about?"

Claude should answer using your CLAUDE.md — without you explaining anything.

---

## Checkpoint

- [ ] `~/my-website` folder created
- [ ] `CLAUDE.md` created with your info
- [ ] Claude can read your context from CLAUDE.md

**Next:** Lesson 2 — Design Brief (Tell Claude exactly what you want)
