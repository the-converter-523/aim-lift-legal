# RELEASE_NOTES.md

**The running record of every "What's new" text AIM Lift has shipped to Google Play, newest first.**

Created 2026-08-04 at Jon's request, at the bug-settings-scrollbar-large-font closeout. Until now the notes lived scattered through PROJECT.md — the current round's copy sat under "Submission & Closed Testing Plan" and older ones were overwritten as each round replaced them. **This file is now where they accumulate; PROJECT.md keeps only the current round's draft.**

## How to use this file

- **Newest at the top.** One section per `versionCode`, since that is what Play actually distinguishes builds by.
- **The code block is the paste-ready copy** — exactly what goes in Play Console's "What's new" field, nothing else.
- 🔴 **Play Console pre-fills "What's new" with the PREVIOUS release's notes.** It does not present an empty required field, so a release can ship carrying the wrong build's notes without anyone noticing. **versionCode 5 shipped with versionCode 4's notes for exactly this reason.** Always rewrite rather than assuming the field is empty and blocking.
- **PSC drafts these unprompted for every AAB build** (Jon, 2026-08-03), delivered in a code block alongside the AAB path. Jon never composes them at the console.
- **Each section header carries an upload date where one is known** — the date the AAB was actually uploaded to Play Console, not the round's closeout/build date, except where noted otherwise on that specific entry. *(release-notes-mirror-and-docs-update, 2026-08-04.)*
- 🔴 **This file is mirrored to a clean, user-facing `CHANGELOG.md` in the public `aim-lift-legal` repo** (`https://the-converter-523.github.io/aim-lift-legal/CHANGELOG`) — version, upload date, and the bullet list only, no meta-commentary. **Every time this file gets a new versionCode section, regenerate and push `CHANGELOG.md` to `aim-lift-legal` in the same step.** Every future "What's new" draft ends with a standing line — `Full changelog: https://the-converter-523.github.io/aim-lift-legal/CHANGELOG` — pointing at that file, never at this one. *(release-notes-mirror-and-docs-update, 2026-08-04 — full convention in DEV_CONVENTIONS.md.)*

## Tone — terse changelog, not marketing (Jon, 2026-08-03)

Flat bullets, almost curt, professional. It reads like a developer's release log: the change stated, nothing else.

- **No warmth, no second person, no explaining the benefit.** "Workout scroll position now persists when minimizing" — never "Your place is now kept so you don't have to scroll back down."
- **No lead-in sentence, no sign-off, no exclamation marks.**
- **But no programming jargon either** — the reader is a tester, not a maintainer. Name the thing on screen (Previous column, Finish button, exercise card), never the implementation (provider, chokepoint, wire border, flavor, isar).
- **Keep it short.** A handful of bullets. Padding it out is worse than brevity.
- 🔴 **Real bullet characters — `•`, one per line (Jon, 2026-08-04).** Play Console's "What's new" is a **plain-text field with no markdown rendering**, so the glyph you type is the glyph the user sees. `•` is the only way to get an actual bullet. **Not `-`**, which was the format for about an hour on 2026-08-04 before Jon changed it: a leading hyphen can read as a dash or a stray typo, especially when Play wraps a long bullet and the second line sits flush under it. **Do not deliver bare unprefixed lines either.** *(versionCodes 7 and earlier were delivered as bare lines — recorded as shipped, not as the model.)*
  - **One change per bullet, and let Play do the wrapping** — do not hard-wrap a bullet across lines in this file, or the line breaks travel into the field.
  - ⚠️ **The field caps at 500 characters per language.** Bullets are cheap at three or four items; they get expensive fast if the copy runs long. Check the count before pasting anything substantially longer than a versionCode-8-sized entry.
- **Rule 12 applies** — this is user-facing copy, delivered as a draft for Jon to accept or change.
- **If a round produced nothing a user can perceive** (doc-only, refactor), say so plainly rather than inventing a user-facing benefit.

---

## versionCode 9 — Uploaded 2026-08-04

*Round: `eyebrow-fittedbox-fix`, bundling everything queued since versionCode 8 (`round-a11y-truncation-fixes` + follow-ups). Closed testing - Alpha, fourth in-window update. Fork: RELEASE NOW. Confirmed uploaded and live (Jon, 2026-08-04) — this is the actual Play Console upload date.*

```
• Set row column headers no longer cut off at large font sizes.
• Shortened the Previous column header to PREV in the active workout.
• Fixed a duplicate SET header on the workout creation and edit screens.
• The PR badge on the workout summary now stays inside the exercise card at large font sizes.
• Fixed the My Workouts, History and Exercises titles stacking one letter per line at large font sizes.
• Fixed the app name eyebrow text wrapping to three lines at large font sizes.
• Full changelog: https://the-converter-523.github.io/aim-lift-legal/CHANGELOG
```

---

## versionCode 8 — 2026-08-04 (closeout date, not a verified upload timestamp)

*Round: `bug-settings-scrollbar-large-font`. Closed testing - Alpha, third in-window update. Fork: RELEASE NOW.*

```
• Fixed the bottom navigation bar pushing the Profile button off screen at large system font sizes, which made Settings unreachable.
• Settings now scrolls when its content does not fit the screen.
• Fixed the Settings title overlapping the screen edge at large system font sizes.
```

---

## versionCode 7 — 2026-08-03 (closeout date, not a verified upload timestamp)

*Round: `round2-dark-themes-and-view-workout`. Closed testing - Alpha, second in-window update. Fork: RELEASE NOW.*

```
Red, Blue and Yellow dark themes now use a matte dark grey
background instead of near black.
Cards are now clearly separated from the background on all
dark themes.
Reduced the yellow tint on the Yellow dark theme background.
Added a View Summary button to the home screen after
completing a split workout.
```

---

## versionCode 6 — 2026-08-03 (closeout date, not a verified upload timestamp)

*Round: `round1-active-workout-polish` (+ the Finish-button follow-ups). Closed testing - Alpha, first in-window update.*

> ⚠️ **The actual "What's new" text for this release was never recorded, and is not recoverable from this repo.** Searched: PROJECT.md, HISTORY.md and the full git history of both. **The convention that PSC writes and stores the notes for every AAB was established at this very round's closeout** (commits `4d48954` / `50cfae8`, 2026-08-03), so it post-dates the copy itself. **Do not reconstruct it — a plausible guess in this file would be indistinguishable from the real record.**

**What the build actually carried** (from PROJECT.md → Release Build, for reference only — *not* the shipped notes):

- The `(F)` marker on the PREVIOUS column for a set logged as a failure
- The equipment type shown beside the body part on the exercise card
- Workout scroll position retained across minimize and reopen
- The surface-filled Finish button

---

## versionCode 5 — 2026-08-02 (closeout date, not a verified upload timestamp)

*Round: `app-check-lift-aab`. The first lift artifact carrying Firebase App Check; added to the Closed testing - Alpha track via "Add from library".*

> ⚠️ **This release shipped carrying versionCode 4's notes** — nobody edited the pre-filled field. This is the incident that produced the standing warning at the top of this file. Harmless on a testing track; it would not have been at production, where the notes are public.

**Separately, the copy entered for the closed-testing submission itself** (PROJECT.md → Firebase App Check → Closed-testing submission, 2026-08-02):

```
Welcome to the AIM Lift closed test! Thanks for helping us test before launch — log workouts, try the split scheduler, and let us know if anything feels off or breaks.
```

> **Note the tone conflict, deliberately preserved rather than tidied:** this predates the terse-changelog convention (2026-08-03) and breaks nearly all of it — warmth, second person, an exclamation mark, a lead-in. **It is recorded as shipped, not as a model.** It also reads as a testing-programme welcome rather than a changelog, which is what it was.

---

## versionCode 4 — 2026-08-01 and earlier

*The build that was live on the internal testing track. Predates Firebase App Check entirely.*

> ⚠️ **No release-notes text is recorded for this build anywhere in the repo.** What is known is only indirect: versionCode 5 inherited these notes via Play's pre-fill, so whatever they said went out twice. The content itself is not in PROJECT.md, HISTORY.md or git history.

---

## Gaps, stated plainly

Two of the five releases above have no recoverable notes text (**4** and **6**). Both predate the 2026-08-03 convention that PSC writes and stores this copy for every AAB. **Nothing is missing from versionCode 7 onward**, and this file exists so that stays true.
