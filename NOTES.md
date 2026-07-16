# Notes

## Workspace layout
- Teaching workspace lives at `a-little-book-of-c/teaching_C_workspace/`. All `lessons/`, `reference/`, `learning-records/`, `MISSION.md`, `RESOURCES.md`, and this file live here.
- **Source code under study** lives one directory up, at `../arrays/` (relative to this workspace) — the user's `.c` files and `common-pitfalls.md`. Lessons cite these by filename only (e.g. "your `exercise_concatinate_inputs.c`"); resolve them under `../arrays/`.

## User
- Hobby programmer; learning C for foundations, not for a job (yet)
- Comfortable reading C and writing small programs independently
- Native Polish speaker (uses Polish identifiers/comments occasionally, e.g. `tekst`, `szukane`, `wynik`)
- Likes to write the same thing multiple ways to internalize it (did `mystrlen` three ways) — encourage this

## Lessons so far
- `0001-pointer-vs-array-storage.html` — the One Principle: storage must exist AND be big enough. Targets the bare-pointer `scanf` and undersized `strcat` bugs.
- `0002-strcat-unrolled.html` — studying a hand-rolled `strcat` from the book. Teaches the three-act structure (find end → lockstep copy → re-seal) and the two-pointer copy idiom `*p = *q; p++; q++;` (plus its compact form `*p++ = *q++`). Hands-on: wrap it as `mystrcat()`.
- `0003-const-qualifier-matrix.html` — the three const positions around a pointer. `const char *p` (data locked), `char * const p` (pointer locked), `const char * const p` (both). The two-question shortcut. const on function params as a seatbelt.
- `0004-postfix-dereference-idiom.html` — unpacking `*p++ = *q++`. Postfix `++` binds tighter than `*`. The 7-step unroll. Six forms at a glance. The classic one-liner strcpy trick.
- `0005-hand-rolled-mystrcpy.html` — four versions of mystrcpy: index form, expanded pointer, compact pointer, one-liner. Compare line counts. The only difference from strcat: no Act 1.
- `0006-malloc-free-and-the-heap.html` — heap memory, malloc/calloc/realloc/free. The three heap sins. Stack vs heap decision. Hands-on: build mystrdup.
- `0007-memory-errors-and-defensive-programming.html` — the four heap sins (leak, dangling pointer, double-free, use-after-free), ownership rule, undefined behavior, Valgrind & ASan. Hands-on: write buggy programs, detect with Valgrind, fix them.

## Where the user is right now
- On page 89 of *A Little Book of C* — Memory leaks/UB (ch 26) done, starting const/volatile (ch 27). Lessons 0001–0007 are written.
- The user has read through chapter 26 (memory errors & defensive techniques) and requested a lesson for it.
- After completing lesson 7, the next frontier is `volatile` qualifier (ch 27, partially new — `const` already covered in lesson 3) or function pointers (ch 28).
- After completing these lessons, the next frontier is deeper malloc practice (dynamically-growing buffers) or whatever the book covers next after dynamic memory.

## Open questions
- Weekly time budget not yet specified — calibrate lesson density once known.
- Confirm details of "A Little Book of C" (author/edition) for RESOURCES.md citation.
- How did lessons 0003–0006 feel? Any recalibration needed for future lessons.
- The user is on page 89 — const/volatile qualifiers. Future lessons should track book progression.

## Style preferences (emerging)
- Tolerates, even enjoys, multiple formulations of one concept — keep offering "index form vs pointer form" parallels
