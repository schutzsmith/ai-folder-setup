# ai-folder-setup

A Claude Code skill that scaffolds a `.ai/` folder for any new project — the single biggest workflow upgrade most non-developers haven't made yet.

## What is the `.ai/` folder?

When you build with AI coding tools, every conversation starts from zero. The AI has no memory of your project, your decisions, or what you built last session. The `.ai/` folder fixes that.

Drop it at the root of your project and fill it in once. At the start of every session, ask your AI to read it before doing anything else. From that point on, you stop re-explaining your project from scratch — the AI starts with full context every time.

## What gets created

Running `/ai-folder-setup` walks you through a short set of questions and generates three files tailored to your project:

| File | Purpose |
|------|---------|
| `.ai/agents.md` | Describes your project to the AI — stack, conventions, and things it should never do |
| `.ai/todo.md` | Your running task list — what's done, what's next, what you're working on now |
| `.ai/session-opener.md` | A ready-to-paste prompt for starting every AI session with full context |

## Examples

See how the `.ai/` folder looks across different project types:

| Example | Stack | Description |
|---------|-------|-------------|
| [`examples/mobile-app`](examples/mobile-app/.ai/) | React Native + Expo + Supabase | Personal expense tracking app |
| [`examples/web-app`](examples/web-app/.ai/) | Next.js 15 + Supabase + Vercel | Freelance proposal generator |
| [`examples/ecommerce`](examples/ecommerce/.ai/) | Shopify + Dawn theme | Handmade textile goods store |
| [`examples/marketing-website`](examples/marketing-website/.ai/) | Astro + Netlify | HR consulting firm site |

## How to install the skill

1. Create the folder `~/.claude/skills/ai-folder-setup/`
2. Copy `SKILL.md` into it
3. In any project, run `/ai-folder-setup` to start the setup flow

## How to use without the skill

If you just want the templates without the skill, copy the `.ai/` folder from any example above into your project root and fill in the blanks.

Then paste this at the start of every AI session:

```
Take a look at the agents.md file and any other markdown files inside the .ai folder.
Once you've reviewed everything, let me know which tasks we have next, prioritized.
Also, let me know what the last change in the git repo was so I can jog my own memory
of where we left off. Then we'll discuss and get started.
```

## Learn more

This skill was built as part of [Good Code](https://goodcode.danielhayessmith.com) — a practical field guide for founders, PMs, and operators who are building with AI tools. It covers the principles, workflows, and pitfalls that matter most when you're not a developer by training.

## Questions or want help building with AI?

I'm [Daniel Hayes Smith](https://danielhayessmith.com), an AI consultant who helps teams and founders build better with AI tools. If you have questions about this template, want to talk through your project setup, or are interested in working together — reach out:

- **Website:** [danielhayessmith.com](https://danielhayessmith.com)
- **X:** [@danielhayesmith](https://x.com/danielhayesmith)
- **LinkedIn:** [danielhayessmith](https://linkedin.com/in/danielhayessmith)
