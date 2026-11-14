# Teaching Workspace — Approach 2

This directory is governed by the **`teach` skill** (pi coding agent skill). It is a self-contained, standalone learning track.

## Core Separation

| | Guided-exercise track (sessions elsewhere) | Teaching-site track (this file) |
|---|---|---|
| **Output** | User writes code in exercise directories. Agent guides, never writes code. Post-session summaries in that track's lesson notes. | Agent creates beautiful, self-contained HTML lessons in `./lessons/`. Reference docs in `./reference/`. |
| **Exercises** | User writes their own exercise code. Agent explains, hints, asks questions. | Exercises appear inside lessons as examples — full solutions shown. The lesson teaches, the user reads and learns. |
| **Learning records** | Concept summaries kept by the guided-exercise track. | `./learning-records/` — captures what the user demonstrated they know. |

## Structure 
- `lessons/` — standalone HTML lesson pages
- `index.html` — lesson index; **every new HTML lesson must be added here**
- This workspace is a git repo → `github.com/wojtek108/learning-c`
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
- Agent never mixes guided-exercise-track output into this workspace (no post-session lessons, no exercise code).

The two tracks are independent. Guided-exercise sessions (coding exercises, guiding) stay there; HTML lessons and reference docs stay here.
