# Daily Check-in — Task Prompt Template

Paste this into the prompt field when creating your daily check-in scheduled task. Replace all `[PLACEHOLDER]` values with your own information before saving.

---

## PROMPT TEXT

OBJECTIVE
Each weekday morning, map out [YOUR_NAME]'s day: pull today's calendar, surface overdue and due-today tasks from the work log, check the project pulse, and send a focused day plan.

FILES
- Work log: [YOUR_WORK_LOG_PATH]
- Projects (your view): [YOUR_PROJECTS_PATH]
- Projects (context): [YOUR_PROJECTS_CONTEXT_PATH]

CALENDAR
Calendar system: [YOUR_CALENDAR_NAME]
Calendar ID(s): [YOUR_CALENDAR_ID]

STEP 1 — Pull today's calendar events. List all events for today with their times, titles, and any location or joining info. Note anything back-to-back, conflicts, or events requiring prep.

STEP 2 — Check the work log. Scan for:
- Tasks marked [ ] (incomplete) with a due date of today or earlier (overdue)
- Tasks marked [/] (in progress)
List them with their due dates. Name overdue chase tasks (follow-ups on outbound requests) first — they're quick wins. Flag anything that's been overdue for more than three days.

STEP 3 — Check +-projects.md. Note the "Next action" line for any project that seems active or time-sensitive right now.

STEP 4 — Check +-projects-context.md for any upcoming deadlines or open threads that are relevant today.

STANDING BLOCKS (optional — delete this section if unused)
[YOUR_STANDING_BLOCKS — protected time that appears in every day plan as a fixture, not a suggestion. E.g. "8:00–8:45 daily: reading" or "Mon + Wed 10:00–12:00: deep work on current writing project." If a meeting collides with a block, say so and propose where the block moves today.]

STEP 5 — Compose a short, direct day plan message. Include:
- Today's calendar events in time order, with the standing blocks placed as fixtures
- What's overdue or due today (tasks), chases first
- Any project next actions that are relevant today
- One deep-work outcome: the single thing that, if it moves today, makes the day a win

Keep it tight. No preamble. No bullet points for the sake of bullet points. If the day is clear, say so — don't invent urgency.

CONSTRAINTS
- Read only. Do not modify any files unless [YOUR_NAME] explicitly asks.
- Read the live work log only. Do not read files in archive/ — archived months are not relevant to today's plan.
- Do not ask clarifying questions during the automated run. Just produce the day plan.
