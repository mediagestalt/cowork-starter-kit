# Daily Check-in — Task Prompt Template

Paste this into the prompt field when creating your daily check-in scheduled task. Replace all `[PLACEHOLDER]` values with your own information before saving.

---

## PROMPT TEXT

OBJECTIVE
Each weekday morning, announce [YOUR_NAME]'s day: pull today's calendar, gather overdue and due-today tasks from the work log, check the project pulse, and send the day's shape — an announcement, not a schedule.

COORDINATION
You are not the only writer of these files — a live planning session and sibling scheduled tasks read and write them too. Before adding any task, note, completion, or chase, check whether it already exists for the relevant date. If it does, do not add a second copy — skip it, or update the existing entry in place. Only add what is genuinely missing.

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
[YOUR_STANDING_BLOCKS — protected time, named in the day's shape in priority order (e.g. "daily: ~45 min reading" or "Mon + Wed: ~2 hrs deep work"). The announcement names them; their clock placement happens later, in the live planning session's time block.]

STEP 5 — Compose the morning announcement: the day's SHAPE, not a schedule. Include:
- Today's meetings with times — the only clock times in the message
- The day's priorities in order, opening with a named first move: one small, concrete on-ramp task (10–15 minutes) so starting requires no decision
- One deep-work outcome: the single thing that, if it moves today, makes the day a win
- What's overdue or due today (tasks), chases first
- Standing blocks (if configured) named as items in the shape
- A triage line: "Running behind? Cut in this order: …" (2–3 items, your judgment)

Do NOT build a clock-by-clock timed plan. The timed plan is built in the live planning session when [YOUR_NAME] actually sits down, and lives in +-time-block.md — never in the work log, and not in this thread. If [YOUR_NAME] replies that they're starting work, don't build the plan here; point them to their planning session.

Keep it tight. No preamble. If the day is clear, say so — don't invent urgency.

CONSTRAINTS
- Read only. Do not modify any files unless [YOUR_NAME] explicitly asks.
- Read the live work log only. Do not read files in archive/ — archived months are not relevant to today's plan.
- Do not ask clarifying questions during the automated run. Just produce the day plan.
