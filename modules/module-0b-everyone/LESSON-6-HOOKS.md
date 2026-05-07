# Lesson 6: Hooks — Automate the Boring Stuff

**Time:** 20 minutes | **Type:** Hands-on | **You'll build:** Auto-format, file protection, and desktop notifications

---

## What You'll Learn

- What Hooks are and when they fire
- How to create a `settings.json` file with hooks
- 3 hooks you'll use every day: format reminder, file protection, completion notification

---

## Concept (3 min read)

### What Are Hooks?

Hooks are shell commands that run automatically when Claude Code does certain things. You configure them in a `.claude/settings.json` file.

Think of hooks as your silent assistant:
- **Before Claude writes a file** → remind it about your formatting preferences
- **Before Claude edits an important file** → block it from touching files you want to protect
- **When Claude finishes a task** → send you a desktop notification

You write the rule once. It runs automatically, every time, forever.

### The Three Hook Types

| Hook | When It Fires | Good For |
|------|--------------|----------|
| `PreToolUse` | Before Claude uses a tool | Reminders, validation, file protection |
| `PostToolUse` | After Claude uses a tool | Logging, cleanup |
| `Stop` | When Claude finishes responding | Notifications, cleanup |

### How Hooks Work

Each hook has:
- `matcher` — what tool to watch for (e.g., "Write", "Edit", "Task")
- `command` — what shell command to run
- Exit code matters: exit 0 = allow, exit 2 = block

---

## Exercise 1: Create Your settings.json (5 min)

### Step 1: Create the .claude folder if needed

```bash
mkdir -p .claude
```

### Step 2: Create settings.json

Create `.claude/settings.json` with your first hook — a format reminder:

```json
{
  "hooks": {
    "PreToolUse": [
      {
        "matcher": "Write",
        "command": "echo 'FORMAT REMINDER: Use bullet points. Keep sections short. Match the tone from CLAUDE.md.'"
      }
    ]
  }
}
```

This fires every time Claude is about to write a file, reminding it of your formatting preferences. Customize the message to match YOUR preferences from CLAUDE.md.

---

## Exercise 2: Add File Protection (7 min)

Some files you never want Claude to accidentally overwrite. Your `CLAUDE.md` is the most important one — if Claude rewrites it, you lose your context.

### Step 1: Add a protection hook

Update your `settings.json`:

```json
{
  "hooks": {
    "PreToolUse": [
      {
        "matcher": "Write",
        "command": "echo 'FORMAT REMINDER: Use bullet points. Keep sections short. Match the tone from CLAUDE.md.'"
      },
      {
        "matcher": "Edit|Write",
        "command": "bash -c 'if echo \"$CLAUDE_TOOL_INPUT\" | grep -q \"CLAUDE.md\"; then echo \"BLOCKED: Cannot edit CLAUDE.md\" && exit 2; fi'"
      }
    ]
  }
}
```

### Step 2: Test it

Ask Claude: "Add a new section to my CLAUDE.md"

Claude should be blocked by the hook. The protection is working.

**Customize:** Want to protect other files? Add them to the grep pattern:
```bash
grep -q "CLAUDE.md\|important-notes.md\|config.json"
```

---

## Exercise 3: Add a Completion Notification (5 min)

When Claude finishes a long task, it's easy to miss. A desktop notification brings you back.

### Step 1: Add a Stop hook

Add a `Stop` section to your `settings.json`:

```json
{
  "hooks": {
    "PreToolUse": [
      {
        "matcher": "Write",
        "command": "echo 'FORMAT REMINDER: Use bullet points. Keep sections short. Match the tone from CLAUDE.md.'"
      },
      {
        "matcher": "Edit|Write",
        "command": "bash -c 'if echo \"$CLAUDE_TOOL_INPUT\" | grep -q \"CLAUDE.md\"; then echo \"BLOCKED: Cannot edit CLAUDE.md\" && exit 2; fi'"
      }
    ],
    "Stop": [
      {
        "command": "osascript -e 'display notification \"Claude finished\" with title \"Claude Code\"' 2>/dev/null; echo done"
      }
    ]
  }
}
```

### Step 2: Test it

Ask Claude to do any task. When it finishes, you should get a macOS desktop notification saying "Claude finished."

> **Note:** The `2>/dev/null` means if `osascript` isn't available (non-Mac), it silently fails and still prints "done". On Windows or Linux, you can replace this with a different notification command.

---

## Your Complete settings.json

Here's the full file with all 3 hooks:

```json
{
  "hooks": {
    "PreToolUse": [
      {
        "matcher": "Write",
        "command": "echo 'FORMAT REMINDER: Use bullet points. Keep sections short. Match the tone from CLAUDE.md.'"
      },
      {
        "matcher": "Edit|Write",
        "command": "bash -c 'if echo \"$CLAUDE_TOOL_INPUT\" | grep -q \"CLAUDE.md\"; then echo \"BLOCKED: Cannot edit CLAUDE.md\" && exit 2; fi'"
      }
    ],
    "Stop": [
      {
        "command": "osascript -e 'display notification \"Claude finished\" with title \"Claude Code\"' 2>/dev/null; echo done"
      }
    ]
  }
}
```

---

## Quick Reference

```
File location:     .claude/settings.json
Hook types:        PreToolUse, PostToolUse, Stop
Exit codes:        0 = allow, 2 = block
Matcher:           Tool name regex (Write, Edit, Task, Bash, etc.)
                   Use | for multiple: "Edit|Write"

Common hooks:
  Format reminder  → PreToolUse on Write
  File protection  → PreToolUse on Edit|Write, exit 2 to block
  Notification     → Stop hook with osascript (mac) or notify-send (linux)
```

---

## Checkpoint

- [ ] `.claude/settings.json` created
- [ ] Format reminder hook added and working
- [ ] File protection hook added — CLAUDE.md is protected
- [ ] Completion notification working
- [ ] You understand what each hook does and when it fires

**Next:** Lesson 7 — Advanced Prompting Patterns
