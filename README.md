# Career Agent

A single-file system for using AI to maintain an honest LinkedIn presence and generate job application materials — without inflating your resume.

## The problem this solves

AI can help you write a version of yourself that sounds coherent before it is actually true.

The fluency is the danger. A coding agent will polish your language until a reasonable inference sounds like a direct credential, and a stretch sounds like a fact. You may not notice until you're in an interview trying to defend something you wrote but didn't quite do.

This system adds friction on purpose. It makes you write your own story first, trace every claim to that story, and verify before you submit.

## How to use it

You don't need to know how to code. You need [Claude Code](https://docs.anthropic.com/en/docs/claude-code) and a folder.

1. Clone or download this repository
2. Open the folder in Claude Code
3. Tell Claude you want to get started — it will walk you through writing `my-story.md`
4. Once your story exists, ask Claude to help with LinkedIn or a specific application

That's it. Claude reads `CLAUDE.md` automatically and follows the protocol.

## What this does

**LinkedIn mode** — helps you draft and maintain:
- Headline and about section
- Post drafts, grounded in real experience
- A content pipeline organized around your actual expertise

**Applications mode** — helps you build, for each job:
- An honest fit assessment (including gaps)
- A claims register that traces every resume bullet to your story
- Resume and cover letter generated only from verified claims
- A pre-submission checklist that asks the hard questions

## What this does not do

- Generate claims you haven't earned
- Recycle language from old applications
- Paper over gaps
- Skip the evidence check

## Files

```
career-agent/
├── CLAUDE.md        ← the agent's instructions (read this to understand the system)
├── README.md        ← this file
└── my-story.md      ← you write this; it becomes the source of everything else
```

Claude will create additional files and directories as you work.

## Credit

This system was built by Eric Allatta, a mid-career educator and data worker, after a close encounter with his own inflated resume. The `CLAUDE.md` is the distilled version of a personal job application repository built in Cursor with Claude.

The post that goes with this: [link]
