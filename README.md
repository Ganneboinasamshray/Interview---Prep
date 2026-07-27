# Interview---Prep — DSA-300 + Daily Tracker

A single-file, self-contained interview prep workspace that combines two tools in one dark, code-editor-themed UI:

DSA-300 — a curated, pattern-based roadmap of ~278 LeetCode problems across 16 core topics, with progress tracking, notes, and 8-week/12-week study plans.
Daily Tracker — a recurring daily task tracker (habits, prep routines, mock-interview checklists) with streaks, charts, and history.

Both live under one shared top navigation bar with two tabs, each showing its own live progress bar, so you can track solving problems and daily habits side by side.

Getting started

This is a single HTML file — no build step, no server, no install.

Download Prep-Suite-DSA300-plus-Tracker.html.
Open it in any modern browser (Chrome, Edge, Firefox, Safari) by double-clicking it, or by opening it via File → Open.

That's it. Everything — markup, styles, and logic for both apps — is bundled into that one file.

Using DSA-300
Click the DSA-300 tab in the top nav.
The left sidebar lists all 16 topics (Arrays, Strings, Linked Lists, Trees, Graphs, DP, etc.) with a live solved-count next to each.
Click a topic to see its problem list. Each row has:
A checkbox to mark a problem solved
A difficulty badge (Easy / Medium / Hard)
Company tags (indicative only — general reputation, not sourced from live hiring data)
A notes icon (✎) to jot your approach, complexity, or gotchas per problem
The Overview page shows your overall progress ring, an Easy/Medium/Hard breakdown, a GitHub-style activity heatmap by date, and a monthly progress chart.
The Study Plans page has two paced tracks (8-week sprint / 12-week deep track) mapping topics to weeks.
Use Export / Import in the sidebar footer to save or reload your solved-problem checkpoint (see Persistence below).
Using Daily Tracker
Click the Daily Tracker tab in the top nav.
Dashboard — today's stats (total/completed/pending tasks, streak, completion %) plus charts.
Tasks — your recurring task list for a given day. Add a task once with + New Task; it will automatically reappear every day going forward until you delete it (see below).
Each task row has edit (✎), duplicate, and delete buttons.
Deleting a task is a soft delete: it stops appearing from that point on, but your completion history for days it was already tracked is preserved.
History — look back at any previous day's completed tasks.
Analytics — streaks, weekly/monthly completion rates, a productivity heatmap, and Backup & Restore (Export CSV / Export JSON / Import JSON).
Settings — clear all tasks or clear logged history.

It comes pre-seeded with three starter tasks ("Solve 2 DSA-300 problems," "Review mistakes from yesterday," "Mock interview / explain solutions out loud") — edit or delete them freely.

Persistence — data is not saved automatically

Both apps keep their data in memory, in the current browser tab only. There is no server and no browser storage (localStorage) involved, so:

Refreshing the page, or closing the tab, clears your progress.
Progress does not sync across devices or browser tabs.

To keep your data across sessions:

App	Where	What it does
DSA-300	Sidebar → Export / Import	Saves/restores solved problems, notes, and solve dates as a .json file
Daily Tracker	Analytics → Backup & Restore	Export CSV (for spreadsheets) or Export/Import JSON (full round-trip of tasks + history)

Recommended habit: export a checkpoint from both apps at the end of each session, and import them back in next time you open the file.

Design notes
Both apps share one dark, monospace "code editor" visual theme (JetBrains Mono for headers/labels, Inter for body text) so they feel like one product rather than two tools stitched together.
The top nav's two progress bars update live: DSA-300 shows overall problems solved; Daily Tracker shows today's completion.
Company tags on DSA-300 problems are general/indicative, not pulled from any live data source — treat them as "commonly asked in this space," not verified statistics.
Known limitations
No accounts, no sync, no server — this is intentionally a local, offline-first tool.
Data lives per-tab; opening the file in a second tab starts fresh.
Export/Import is manual — there's no auto-save.
