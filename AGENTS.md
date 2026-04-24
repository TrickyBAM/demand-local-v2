# Demand Local V2 Agent Notes

## Project
Demand Local V2 is a static fork of the Demand Local redesign for automotive marketing and LinkOne positioning. It keeps the one-page dealership advertising story but localizes more assets, including team imagery.

## Stack
- Static `index.html` with inline CSS and JavaScript.
- Local `images` directory for site media.
- Vercel static hosting via `vercel.json` with an empty build command and repo-root output.

## Gotchas And Quirks
- This repo is intentionally simple: no package manager, no build step, and nearly everything lives in `index.html`.
- A recent commit removed a catch-all route so images load correctly. Be careful with Vercel routing changes because static image paths depend on root hosting.
- The PageSpeed call is made from public browser JavaScript and includes an API key in the HTML. Treat anything in this file as public and rotate keys if this matters.
- Because this is a fork of the earlier redesign, verify whether a content change belongs here, in V3/V4, or in the older redesign before copying edits across repos.

## How Brian Works
- Brian describes what he wants in plain English. Do the actual implementation, testing, and GitHub work for him.
- Do not hand Brian snippets to paste or ask him to read code. Make the change, verify it, and summarize in plain English.
- Read the README, recent commits, `AGENTS.md`, and `CLAUDE.md` before assuming project context.
- Ask only for real product direction, source-of-truth choices, or destructive/live-production actions. For normal branch work, proceed.
- Prefer the existing stack and npm where applicable. Do not add new frameworks or major libraries without a clear reason.
