# Teaching Workspace — Approach 2

This directory is governed by the **`teach` skill** (pi coding agent skill). It is a separate learning track from the exercise-driven approach used in the `a-little-book-of-c/` project (see that project's `AGENTS.md`).

## Core Separation

| | Approach 1 (`a-little-book-of-c/` AGENTS.md) | Approach 2 (this file) |
|---|---|---|
| **Output** | User writes code in the book project's subdirs. Agent guides, never writes code. Post-session summaries in the project's `_lessons_learned/`. | Agent creates beautiful, self-contained HTML lessons in `./lessons/`. Reference docs in `./reference/`. |
| **Exercises** | User writes their own exercise code. Agent explains, hints, asks questions. | Exercises appear inside lessons as examples — full solutions shown. The lesson teaches, the user reads and learns. |
| **Learning records** | Project's `_lessons_learned/` — concept summaries after each session. | `./learning-records/` — captures what the user demonstrated they know. |

## Structure 
- `teaching_C_workspace/lessons/` — standalone HTML lesson pages
- `teaching_C_workspace/index.html` — lesson index; **every new HTML lesson must be added here**
- `teaching_C_workspace/` is a git repo → `github.com/wojtek108/learning-c`
- Live site: `wojtek108.github.io/learning-c/`

## How This Workspace is Organised

- `lessons/` — HTML lessons created by the agent. One per file, sequentially numbered (`0008-*.html`).
- `index.html` — lesson index; **every new HTML lesson must be added here**.
- `reference/` — cheat sheets, glossaries, reference algorithms. Quick-lookup documents.
- `learning-records/` — ADR-style notes about what the user has demonstrated they understand.
- `assets/` — reusable components (shared stylesheets, JS widgets, etc.).
- `MISSION.md` — why the user is learning C.
- `RESOURCES.md` — curated high-trust resources.
- `NOTES.md` — scratchpad for preferences and observations.

## How to Use This Workspace

- Agent creates lessons in `lessons/` based on the `teach` skill rules: beautiful, short, self-contained, mission-tied. New lessons are added to `index.html`.
- Agent creates reference documents in `reference/` for quick lookup.
- Agent writes learning records when the user demonstrates genuine understanding of a concept.
- Agent never mixes Approach 1 output into this workspace (no post-session lessons, no exercise code).

The two approaches are independent. What happens in Approach 1 (coding exercises, guiding) stays there. What happens here (HTML lessons, reference docs) stays here.
