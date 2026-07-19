# Obsidian Setup Guide

This planning system is built to work inside **Obsidian** — a free, local-first notes and knowledge app for Mac, Windows, and Linux. Your files live on your own computer as plain markdown files, not in the cloud. Obsidian is how you'll read and edit them.

This guide walks you through installing Obsidian, connecting your planning folder, and installing the one plugin this system needs.

---

## What Obsidian is (and why this system uses it)

Obsidian is a markdown editor that works on a folder of files you own. There's no proprietary format — every note is a plain `.md` file you can open in any text editor. Obsidian adds a lot on top of that: a two-pane editor, search, backlinks, a graph view, and a rich plugin ecosystem.

This system uses Obsidian for two reasons:
1. **The Tasks plugin** — makes the work log's checkboxes, due dates, and completions work correctly, and lets you query tasks across all your notes in one view
2. **Plain files** — your planning files are just markdown. Claude (via Cowork) reads and writes them directly. No sync issues, no API, no accounts.

You don't need to become an Obsidian power user. You need it running, one plugin installed, and a vault pointed at your planning folder. That's it.

---

## Step 1 — Download and install Obsidian

Go to **https://obsidian.md** and download the version for your operating system. It's free. Install it like any app.

---

## Step 2 — Open your planning folder as a vault

When Obsidian opens for the first time, it will ask you to open a vault.

1. Click **Open folder as vault**
2. Navigate to the folder you set up as your Cowork workspace (your planning folder)
3. Select it and click Open

That folder is now your Obsidian vault. Every `.md` file in it is a note. Your planning files (`+-YYYY-work-log.md`, `+-projects.md`, etc.) will appear in the left sidebar as soon as Claude's onboarding session creates them.

> **Note:** If Obsidian asks you whether to trust the author of the vault, click Trust. This just means you're allowing community plugins to run, which you'll need in Step 3.

---

## Step 3 — Install the Tasks plugin

The Tasks plugin is what makes the work log's checkbox format work properly. It's how Obsidian understands due dates, completion dates, and task status.

1. In Obsidian, open **Settings** (gear icon in the bottom left)
2. Go to **Community plugins**
3. If community plugins are disabled, click **Turn on community plugins**
4. Click **Browse**
5. Search for **Tasks**
6. Click on "Tasks" by Clare Macrae — it's the most-downloaded result
7. Click **Install**, then **Enable**

Once it's enabled, close Settings. The Tasks plugin is now running.

**What it does:** Whenever you put a checkbox in a note using the format `- [ ] Task description [due:: 2026-07-15]`, the plugin understands it as a task with a due date. Checking it off automatically adds a completion date. It also powers the tasks dashboard (`+-Tasks.md`) — a file of "query blocks" that pulls every task from all your notes into one live view: overdue, due today, this week, upcoming. The ready-made copy is in `vault-template/+-Tasks.md`; the onboarding session puts it in place if you didn't start from the vault template.

---

## Step 4 — (Optional) Install the Linter plugin

The Linter plugin auto-updates the `modified:` timestamp in your files' frontmatter whenever you save. This keeps the file metadata current without you having to touch it.

Install it the same way as Tasks: Settings → Community plugins → Browse → search "Linter" → install and enable.

Once Linter is running, go to its settings and make sure "Update modified date on save" is turned on under **General** or **YAML fields**. You can leave everything else at the default.

---

## How this system's files work in Obsidian

Once the onboarding session creates your files, here's what you'll have and how they behave:

### The work log (`+-YYYY-work-log.md`)

This is the most active file. It has a section for each week and a dated entry for each workday. Tasks look like this:

```
- [ ] Write project update for manager [due:: 2026-07-14]
- [x] Team meeting [completion:: 2026-07-11]
- [/] Draft quarterly report
```

In Obsidian, the checkboxes are clickable. When you check one off, the Tasks plugin automatically adds `[completion:: today's date]`. You can also type task entries directly — Obsidian will format them as you go.

The `+-` prefix on the filename is a naming convention: it sorts these files to the top of the file list in alphabetical order, so your planning files are always easy to find.

### The projects file (`+-projects.md`)

Your at-a-glance project list. You'll look at this weekly, usually on Fridays. It's plain prose — no special plugin behaviour. Just read it, update the status log entries by appending new ones, and update the next action.

### The projects context file (`+-projects-context.md`)

Claude's reference file. You don't need to open this often. When something significant changes on a project — a new deadline, a key decision, a new person involved — you or Claude will update the relevant section. The file is there so Claude can give you informed help without you having to re-explain your situation every session.

---

## Navigating Obsidian day-to-day

- **Left sidebar:** Your file list. All your planning files appear here. Click to open.
- **Ctrl/Cmd + P:** Command palette — search for any Obsidian command. Useful if you want to do something and can't find the button.
- **Ctrl/Cmd + O:** Quick open — jump to any file by name.
- **Ctrl/Cmd + E:** Toggle between editing and reading mode.

That's all you need to know to use this system in Obsidian. The rest of the app — graph view, backlinks, templates, all of it — is there if you want to explore, but this system doesn't depend on any of it.

---

## A note on Cowork and Obsidian together

Cowork and Obsidian access the same folder. When Claude's scheduled tasks update your work log at the end of the day, you'll see the changes the next time you open (or switch to) the file in Obsidian. If you have the file open, just click into it — Obsidian will refresh automatically.

You don't need to have Obsidian open for Cowork to work. The files are just files — Cowork reads and writes them directly.
