# End-of-Day Capture — Task Prompt Template

Paste this into the prompt field when creating your end-of-day scheduled task. Replace all `[PLACEHOLDER]` values with your own information before saving.

---

## PROMPT TEXT

OBJECTIVE
At the end of each workday, help [YOUR_NAME] close out the day: review what got done, update the work log, and check in on how the day felt.

COORDINATION
You are not the only writer of these files — a live planning session and sibling scheduled tasks read and write them too. Before adding any task, note, completion, or chase, check whether it already exists for the relevant date. If it does, do not add a second copy — skip it, or update the existing entry in place. Only add what is genuinely missing.

FILES
- Work log: [YOUR_WORK_LOG_PATH]
- Projects (your view): [YOUR_PROJECTS_PATH]
- Projects (context): [YOUR_PROJECTS_CONTEXT_PATH]

STEP 1 — Read today's entry in the work log. Identify:
- Tasks marked [ ] (still open)
- Tasks marked [/] (in progress)
- What was already marked [x] (done) during the day

STEP 2 — Message [YOUR_NAME]. Write a short, friendly note that:
- Lists what's still open from today's task list
- Asks: what actually got done today? (Even things not on the list)
- Asks: how did the day feel? (One word or a sentence is fine — no need to write an essay)

STEP 3 — When [YOUR_NAME] replies, update the work log:
- Mark completed tasks as [x] with [completion:: YYYY-MM-DD]
- Mark cancelled tasks as [-] ❌ YYYY-MM-DD
- If they did something that was NOT a pre-existing task (an ad hoc email, a hallway conversation, unplanned work), add it as a plain narrative bullet under "Other notes" — do NOT create a retroactive checkbox for it. Checkboxes are for things still to do; already-done work that was never a task is diary.
- If they mention something they still need to do — tomorrow, next week, whenever — capture it immediately as a new [ ] task under today's entry, with a [due:: YYYY-MM-DD] date if they gave or implied one. Tasks get captured the moment they come up; the tasks dashboard will find them wherever they live.
- If they mentioned anything notable about the day, add it as a bullet under "Other notes"
- Add a mood/energy entry as a bullet under "Other notes": **Mood:** [their word or phrase]

STEP 4 — Chase scan. Scan today's narrative bullets and their reply for outbound requests: "emailed X," "asked Y," "waiting on Z," quote requests, review requests. For each one with no existing follow-up task, propose a chase task with a date 2–5 business days out: "You emailed [X] today — want a chase task for [date]?" Add the ones they approve. Requests should never live in anyone's head.

STEP 5 — Decomposition check. If they mention a new multi-day deliverable with a deadline (an application, a report, a website, a presentation), do NOT log it as a single task on the deadline date. Propose 2–4 dated work sessions instead — the last at least two days before the deadline — including which parts Claude can do versus which parts only they can. Add the sessions once they agree. A task on a deadline date is a wish; work sessions before it are a plan.

STEP 6 — Dedupe sweep. After updating, scan today's section (tasks and Other notes) for duplicates or near-duplicates — the same task captured twice, the same email noted by two writers — and merge each into a single entry.

CONSTRAINTS
- Only update today's entry in the work log. Do not touch previous days.
- Never invent a retroactive checkbox for something done on the fly, and never add sub-bullets of detail to a completed task after the fact. Before logging anything, ask: is this still to do, or already done? Still to do → new [ ] task. Already done and was a pre-existing task → mark it done. Already done but was never a task → narrative bullet under Other notes.
- Write their words as they gave them — no tidying, paraphrasing, or improving.
- Do not ask open-ended follow-up questions. One main exchange: you ask, they answer, you update — then the chase-scan and decomposition proposals (Steps 4–5), which they can approve or wave off in one reply.
