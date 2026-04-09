# Career Agent

A workflow for using AI to maintain an honest LinkedIn presence and generate job application materials — without inflating your resume.

## The problem this solves

AI can help you write a version of yourself that sounds coherent before it is actually true.

The fluency is the danger. A coding agent will polish your language until a reasonable inference sounds like a direct credential, and a stretch sounds like a fact. You may not notice until you're in an interview trying to defend something you wrote but didn't quite do.

This system adds friction on purpose. It makes you write your own story first, trace every claim to that story, and verify before you submit.

## How it works: the separation model

Most AI writing tools take a job description and a rough resume and fill in the gaps. This one doesn't. It keeps three things permanently separate:

**1. Your story** — `my-story.md`
You write this once, in your own words. What you've done, what you're good at, where you struggle, what you want. This file is the source of everything else. Claude never writes it for you; it only helps you get it out.

**2. The friction layer** — `claims.md` (per application)
Before any resume or cover letter exists, you build a claims register: every sentence that will appear in your materials, traced back to a specific passage in your story. Claims with no source don't get written. Weak connections get flagged.

**3. The outputs** — `resume.md`, `cover-letter.md`, LinkedIn drafts
Generated only from verified claims. Never from inference, never from the job description, never from thin air.

This structure means the AI is doing what it's good at — drafting, organizing, adapting tone — while the evidence stays with you.

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

**Applications mode** — builds a dedicated folder for each job:
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

The repository starts with two files. Everything else is created as you work.

```
career-agent/
├── CLAUDE.md                     ← the protocol (read this to understand the system)
├── README.md                     ← this file
├── my-story.md                   ← you write this; source of all claims
├── linkedin/
│   ├── profile.md                ← working draft of your LinkedIn profile
│   └── posts-pipeline.md         ← content pillars, idea backlog, active drafts
└── applications/
    └── <company-role>/
        ├── role.md               ← what is this role and why does it interest you
        ├── fit.md                ← honest assessment: where you fit and where you don't
        ├── claims.md             ← every claim sourced before materials are written
        ├── checklist.md          ← pre-submission gate
        └── materials/
            ├── resume.md
            └── cover-letter.md
```

## Credit

This system was built by Eric Allatta, a mid-career educator and data worker, after a close encounter with his own inflated resume. The `CLAUDE.md` is the distilled version of a personal job application repository built in Cursor with Claude.

The post that goes with this: [https://www.linkedin.com/posts/eric-allatta_github-mrallattacareer-agent-activity-7448117126663397377-uUi6?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAZ46-4B1ZJkcTJnRKiinGih5ku9XSbbfi4]
