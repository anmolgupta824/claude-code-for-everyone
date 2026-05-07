# Lesson 5: Deploy

**Time:** 15 minutes | **You'll do:** Push your site live to Vercel and get a real URL

---

## What Happens in This Lesson

You'll deploy your website to Vercel — a free hosting platform used by millions of developers. By the end of this lesson, your site will be live at a URL like `yourname.vercel.app` that anyone in the world can visit.

> **What is "deploying"?** It means putting your files on a server so anyone can access them through a URL. Right now your site only exists on your computer. After this lesson, it exists on the internet.

---

## Step 1: Create a Free Vercel Account

If you don't have one already:

1. Go to [vercel.com](https://vercel.com)
2. Sign up with GitHub, Google, or email (any works)
3. You don't need to set up a project in the dashboard — we'll do it from the terminal

---

## Step 2: Install the Vercel CLI

The Vercel CLI is a tool that lets you deploy from the terminal with one command.

Check if Node.js is installed first:

```bash
node --version
```

If you see a version number (like `v18.0.0`), you're good. If not, tell Claude and it will guide you through installing Node.js first.

Install the Vercel CLI:

```bash
npm install -g vercel
```

> **What is npm?** It's a package manager — a tool that installs other tools. It comes with Node.js.

---

## Step 3: Log In to Vercel

```bash
vercel login
```

This will ask you to confirm your email. Check your inbox for a Vercel email, click the button, and come back to the terminal.

---

## Step 4: Deploy Your Site

Make sure you're in your website folder:

```bash
cd ~/my-website
```

Then deploy:

```bash
vercel
```

Vercel will ask you a few questions:

- **Set up and deploy?** → Yes
- **Which scope?** → Your personal account
- **Link to existing project?** → No
- **What's your project's name?** → Type your name or a project name (all lowercase, hyphens OK: `jane-doe` or `my-portfolio`)
- **In which directory is your code located?** → `./` (just press Enter)
- **Want to override the settings?** → No

Vercel will build and deploy. In about 30 seconds, you'll see:

```
Production: https://your-project-name.vercel.app [2s]
```

**That's your URL. Your site is live.**

---

## Step 5: Open It

Click the URL in your terminal, or copy-paste it into your browser.

You're looking at YOUR website, live on the internet, accessible to anyone in the world.

---

## Step 6: Test It

- Open it on your phone (share the URL with yourself via text or email)
- Ask a friend to open it
- Check that everything looks the same as your local version

If anything looks different or broken, tell Claude — it will fix the issue and you'll re-deploy with the same `vercel` command.

---

## Bonus: Connect a Custom Domain (Optional)

If you own a domain (like `yourname.com`), you can connect it to Vercel for free:

1. In the Vercel dashboard, open your project
2. Go to Settings → Domains
3. Add your domain and follow the DNS instructions from your domain registrar

This is optional — your `.vercel.app` URL works perfectly as your permanent address.

---

## Quick Reference

```
Install CLI:       npm install -g vercel
Login:             vercel login
Deploy:            vercel (from your project folder)
Re-deploy:         vercel (run again after any changes)
Custom domain:     Vercel dashboard → Settings → Domains
Your URL format:   https://[project-name].vercel.app
```

---

## Checkpoint

- [ ] Vercel account created
- [ ] Vercel CLI installed (`npm install -g vercel`)
- [ ] Logged in to Vercel
- [ ] Site deployed — you have a live URL
- [ ] Tested on phone — looks good
- [ ] URL saved somewhere (you'll want to share this)

**Next:** Lesson 6 — Celebrate (you shipped, now share it)
