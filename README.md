---
created: 2026-07-12, 12:42
modified: 2026-07-12, 13:38
---
# Cowork Planning System — Starter Kit

A personal planning system powered by Claude and Cowork. It gives you a daily check-in, a running task log, a project tracker, and a weekly review — all connected, all in one place. Once it's set up it mostly runs itself.

This kit includes everything you need to get started: an onboarding session that builds your files from scratch, example files so you can see what the end result looks like, and template prompts for three scheduled tasks.

---

## What this system does

**Day-to-day:**
- A morning check-in maps your day from your calendar and task list
- You track tasks in a daily work log using a simple checklist format
- An end-of-day capture closes out the day and updates the log

**Weekly:**
- A Friday review summarizes what got done, checks the project pulse, and looks ahead

**Projects:**
- Two project files keep your active work organized: a clean view for you and a dense context file for Claude
- Status entries are dated and appended, not overwritten — so you have a running history

**Planning sessions:**
- Open a Cowork planning session any time to work on a project, draft something, or think through a problem. Claude has the context it needs from your project files.

---

## What you need before you start

1. **Obsidian (strongly recommended)** — free, local-first notes app. Your planning files are plain markdown and the system works without it, but Obsidian is what makes the checkboxes clickable, completion dates automatic, and the tasks dashboard render. **If you haven't used Obsidian before, read `obsidian-setup.md` first** — it walks you through installation, vault setup, and the one plugin this system uses (Tasks). Takes about 10 minutes. You can also skip it for now and add it once the system has proven itself.

2. **Cowork desktop app** — installed and running

3. **Google Calendar connected** in Cowork (for the scheduled tasks)
   - If you use Apple Calendar or Outlook instead, the scheduled tasks can still work, but you'll need to adjust the calendar steps in the prompts
   - **If your workplace blocks connecting Claude to its systems** (common on Microsoft/Outlook campuses): route around it with calendar subscriptions. In Outlook, publish/share your work calendar to get an ICS link; in a personal Google Calendar, add it under "Other calendars → From URL." Do the same for any other calendar you want visible. Then connect that Google account to Cowork. Claude sees everything in one place. Two caveats: subscribed calendars are read-only (fine — this system only reads them), and the sync can lag by a few hours, so same-day changes may not show in the morning check-in.

4. **A folder on your computer** for your planning files — this becomes both your Obsidian vault and your Cowork workspace. The easy way: **copy the `vault-template/` folder** from this kit to wherever you want it (e.g. `~/Documents/Planning`) and rename it. It comes with all the planning files as ready skeletons plus the tasks dashboard — see its `START-HERE.md`. Or create an empty folder and let onboarding build the files from scratch. Either way, don't use a folder that already has unrelated files in it.

5. **About 30 minutes** for Obsidian setup + the onboarding session

---

## Which Claude model?

Model names change, so think in tiers rather than names. The **deep sessions** — onboarding, the voice profile, and any substantial drafting or thinking work — deserve the most capable model your plan offers: they're one-time or high-stakes, and the quality difference shows. The **daily rhythm** — morning check-ins, end-of-day captures, weekly reviews — is routine reading and summarizing; a mid-tier model handles it well and costs less of your usage limit. If a scheduled task's output starts feeling thin or careless, that's the sign to bump it up a tier.

---

## What's in this kit

```
cowork-starter-kit/
├── README.md                          ← you are here
├── obsidian-setup.md                  ← start here if Obsidian is new to you
├── onboarding-instructions.md         ← paste this into your Cowork setup project
├── voice-session-instructions.md      ← optional; do this after a week of using the system
├── vault-template/                    ← ready-to-go vault: copy, open in Obsidian, done
│   ├── START-HERE.md
│   ├── +-2026-work-log.md
│   ├── +-projects.md
│   ├── +-projects-context.md
│   ├── +-Tasks.md
│   └── archive/
├── examples/                          ← a FILLED-IN system, so you can see the destination
│   ├── work-log-example.md            ← what your work log will look like in use
│   ├── projects-example.md            ← what your projects file will look like in use
│   └── projects-context-example.md    ← what Claude's context file will look like in use
└── task-prompts/
    ├── daily-checkin-prompt.md        ← morning task prompt (fill in your details)
    ├── end-of-day-prompt.md           ← end-of-day task prompt
    └── friday-review-prompt.md        ← Friday weekly review prompt
```

Take a look at the example files first to understand what you're building toward, then follow the setup steps below.

---

## How to set up

### Step 1 — Create the onboarding project

Open Cowork. Create a new project. Name it something like "Planning Setup."

- Select your planning folder as the workspace
- Paste the contents of `onboarding-instructions.md` into the Project Instructions field
- Start the session

### Step 2 — Run the onboarding Q&A

Claude will walk you through a series of questions: your name and role, your current projects, your calendar, and whether you want scheduled tasks. Answer honestly — the more detail you give, the better the files will be.

At the end, Claude will:
- Create your work log file
- Create your projects file (your view)
- Create your projects context file (Claude's reference)
- Create your tasks dashboard (a live all-tasks view for Obsidian)
- Generate project instructions for your ongoing planning session

Review each file before Claude writes it. You can ask for changes.

### Step 3 — Create your ongoing planning session

Open Cowork. Create a new project. Name it something like "Work Planning."

- Select the same planning folder as the workspace
- Paste the project instructions Claude generated in Step 2 into the Project Instructions field
- This is your daily planning session going forward

### Step 4 — Set up scheduled tasks (optional but recommended)

If you ran the onboarding session, Claude already generated customized prompts for the tasks you asked for — use those. The files in `task-prompts/` are the manual fallback: open each one, fill in your details (name, file paths, calendar ID), and use that text instead.

Either way:

1. In Cowork, go to Scheduled Tasks
2. Create a new task
3. Paste the prompt text
4. Set the time you want it to run
5. Enable it

Do this for each of the three tasks you want.

**Finding your Google Calendar ID:**
In Google Calendar, click the three dots next to a calendar name → Settings → scroll to "Integrate calendar" → copy the Calendar ID. It looks like `abc123@group.calendar.google.com` or just your Gmail address for the main calendar.

---

## The four files

Once onboarding is done, you'll have four files in your planning folder:

**`+-YYYY-work-log.md`** — Your daily task log. One entry per workday. Tasks use a simple checkbox format with due dates. The scheduled tasks read and update this file automatically.

**`+-projects.md`** — Your project view. One section per active project: a one-line description, dated status entries (newest at the bottom), and a next action. Look at this on Fridays and update it. Takes about five minutes.

**`+-projects-context.md`** — Claude's reference file. You don't need to read this regularly. It holds all the background detail — history, stakeholders, constraints, context — that would clutter your view but that Claude needs to give you good help. Update it when something significant changes on a project.

**`+-Tasks.md`** — Your tasks dashboard. A single Obsidian view of every task across your notes: in progress, overdue, due today, this week, upcoming. You don't write in this file — it builds itself from your work log via the Tasks plugin. (Obsidian only; the ready-made copy is in `vault-template/+-Tasks.md`.)

---

## Day-to-day usage

**Morning:** The daily check-in runs automatically and sends you a day plan. Reply if you want to discuss something; otherwise just use it as a map for the day.

**During the day:** Open your planning session any time to work on something — draft an email, think through a decision, update a project, add tasks to the work log.

**End of day:** The end-of-day capture asks what got done. Reply with a sentence or two and it updates the log.

**Friday:** The weekly review runs automatically. Read it, reply with how the week felt, and you're done.

**As needed:** Open your planning session to do a project check-in, update the projects files, or work on something that came up.

---

## Tips

- **Capture tasks the moment you think of them.** Don't hold a task in your head — put it in the work log as a checkbox with a due date, even if it's for weeks from now. The tasks dashboard (`+-Tasks.md`) pulls every open task into one view, so nothing gets lost no matter which day's entry it lives in. The one thing checkboxes are *not* for: work you already did that was never a task — that goes as a narrative note, so the log stays an honest record of what happened.
- **Keep the projects file short.** Background detail goes in the context file. If your projects view is getting long, move the detail.
- **Update project status weekly, not constantly.** The Friday review is a natural prompt for this.
- **Tag tasks by project.** A simple hashtag on the task line (`#grant-project`, `#website`) makes tasks groupable in the weekly review and filterable in the tasks dashboard. Pick short, stable tags — one per project is plenty.
- **Plan for growth.** A year of daily entries makes the work log large, and the scheduled tasks re-read it every day. Every quarter or so, move past months into a file in `archive/` (e.g. `archive-2026-Q1-work-log.md`) — the Tasks plugin still sees open tasks in archived files, so nothing disappears from the dashboard. Same for projects: keep the last 2–3 status entries per project and prune older ones during the Friday pass; when a project finishes, move its section to an Archive section at the bottom of `+-projects.md`.
- **One home per fact.** When detail lives in a dedicated file (an event logistics doc, a research context file), the projects context file should point to it, not copy it. Duplicated detail costs double to read and drifts out of sync. Keep volatile facts in one canonical place and let everything else reference it.
- **Deadlines become work sessions.** A task sitting on its own deadline date is a wish — the system stays silent until the day it's due. When a multi-day deliverable comes up, Claude proposes dated work sessions before the deadline, including which parts Claude can do outright. You should never do the decomposition yourself.
- **Chase every outbound request.** Every email awaiting a reply, quote request, or review ask gets a follow-up task with a date a few business days out — captured at send time, proposed automatically by the end-of-day task. Requests shouldn't live in your head.
- **Park honestly.** Projects deliberately on hold go in a Parked section with a re-entry trigger (a date, or "when X happens"). The Friday review checks triggers only. An honest projects file with three active projects beats an aspirational one with ten.
- **Hand Claude the work, not just the typing.** Analysis, site builds, data pulls, report drafts, applications drafted from source documents — the pattern is "hand Claude X; Claude produces Y; you review." Your time goes to judgment, relationships, and the work only you can do.
- **The planning session works best when Claude has context.** The first time you work on something, give a little background. After that, it's in the context file and you won't need to repeat yourself.
- **Scheduled tasks can be paused anytime.** If you're on vacation or the timing isn't working, disable a task in Cowork and re-enable it when you're back.
- **After a week or two, consider the voice session.** `voice-session-instructions.md` walks through a short optional interview that helps Claude write professional emails and documents in your voice. It takes about 20 minutes and is worth doing once you know what you want Claude to write for you. A deeper version is also possible if you want Claude to handle more substantial writing — the file explains what that looks like.
