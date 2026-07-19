# Changelog

## v2.0 — 2026-07-19

Design lessons from running the system in practice. Two root problems drove every change: the kit assumed one writer, but real setups have several (a live planning session plus up to three scheduled tasks, all writing the same files); and timed day-plans were landing in the work log, bloating a record with predictions.

- **Coordination model.** Every task prompt now carries a "reconcile, never duplicate" rule: check whether an entry already exists before adding one. Lanes assign one owner per job — the live planning session is the in-day editor, the morning check-in announces (read-only), the end-of-day reconciles and runs a daily dedupe sweep, the Friday review maintains projects and dedupes weekly.
- **Plan and record separated.** New `+-time-block.md` in the vault template holds the daily timed plan — built in the live planning session when you actually sit down, times computed from your real start, overwritten each day, no guilt if the day diverges. The work log holds only what happened: meetings with notes, and task tracking.
- **Morning check-in reframed as an announcement.** It delivers the day's shape — meetings as the only clock times, ordered priorities, a named 10–15 minute first move, one deep-work outcome, and a "running behind? cut in this order" triage line. It no longer builds a clock-by-clock plan or writes anything.
- **Friday review now maintains the projects file.** Appends dated status entries from your updates, keeps the last 2–3 per project, prunes older ones, and runs the weekly dedupe.
- **Standing blocks rewording.** The check-in names them in the day's shape; the live session places them on the clock.

## v1.0 — 2026-07-12

Initial kit: README, Obsidian setup guide, onboarding session, voice profile session, three scheduled-task prompt templates, filled-in examples, and a ready-to-go vault template with tasks dashboard.
