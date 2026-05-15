---
name: ai-folder-setup
description: Scaffolds a .ai/ folder for a new project by walking the user through a short onboarding questionnaire, then writing agents.md, todo.md, and session-opener.md tailored to their answers.
---

# .ai Folder Setup Skill

When this skill is invoked, guide the user through creating a `.ai/` folder for their project. This folder gives AI coding assistants full context at the start of every session so the user never has to re-explain their project from scratch.

## How to run this skill

Work through the steps below in order. Do not skip steps or ask all questions at once — the flow should feel like a focused onboarding conversation, not a form dump.

---

## Step 1 — Introduce what you're doing

Tell the user in 2–3 sentences what the `.ai/` folder is and what you're about to create:
- `agents.md` — describes the project to the AI (stack, conventions, guardrails)
- `todo.md` — their running task list
- `session-opener.md` — a ready-to-paste prompt for starting every AI session

---

## Step 2 — Ask about the project

Ask these questions. You can group them into one message but keep it readable:

1. **Project name** — What's this project called?
2. **What it does** — One or two sentences: what does it do, and who is it for?
3. **Frontend** — What are you using for the UI? (e.g. React, Next.js, plain HTML, none)
4. **Backend** — Any server-side code? (e.g. Node.js, Python, Cloudflare Workers, none)
5. **Database** — Are you storing data? What with? (e.g. Postgres, Supabase, SQLite, none)
6. **Hosting** — Where does it live or where will it be deployed? (e.g. Vercel, Cloudflare Pages, not sure yet)

---

## Step 3 — Ask about conventions and guardrails

Ask these in a second message:

7. **Conventions** — Do you have any rules the AI should follow? (e.g. "keep components small", "use plain CSS not Tailwind", "always ask before adding a new package") — it's fine if they don't have any yet, suggest a sensible default
8. **Never do** — Is there anything the AI should never do without asking first? (e.g. "don't rewrite files I haven't mentioned", "don't change the database schema", "don't install new tools") — suggest "don't rewrite files I haven't asked you to touch" as a default if they're unsure

---

## Step 4 — Ask about current work

Ask in a third message:

9. **First task** — What's the first thing you want to build or fix? This becomes the first item in `todo.md` and the `Current focus` in `agents.md`.

---

## Step 5 — Confirm before writing

Summarize what you're about to create:
- List the three files and their key contents
- Ask: "Ready to create these files?"

Wait for confirmation before proceeding.

---

## Step 6 — Create the files

Create the following files in the current working directory:

### `.ai/agents.md`

```markdown
# Project: {project_name}

## What it does
{one_two_sentence_description}

## Stack
- Frontend: {frontend}
- Backend: {backend}
- Database: {database}
- Hosting: {hosting}

## Conventions
{bullet list of conventions — one per line}

## Never
{bullet list of guardrails — one per line}

## Current focus
{first_task}
```

### `.ai/todo.md`

```markdown
# Todo

## In progress
- [ ] {first_task}

## Up next
- [ ] (add your next priority here)

## Done
(nothing yet)
```

### `.ai/session-opener.md`

```markdown
# Session Opener

Paste this at the start of every AI coding session:

---

Take a look at the agents.md file and any other markdown files inside the .ai folder.
Once you've reviewed everything, let me know which tasks we have next, prioritized.
Also, let me know what the last change in the git repo was so I can jog my own memory
of where we left off. Then we'll discuss and get started.
```

---

## Step 7 — Finish with a clear summary

After writing the files, tell the user:

1. What was created (list the three file paths)
2. What to do next:
   - Open `.ai/agents.md` and fill in anything that was left as a placeholder
   - Update `.ai/todo.md` as they complete tasks and add new ones
   - Copy the prompt from `.ai/session-opener.md` at the start of every AI session
3. Remind them that the template repo at https://github.com/schutzsmith/ai-folder-template has more examples and context if they want to see how others have filled these out
