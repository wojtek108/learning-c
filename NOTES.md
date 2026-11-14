# Notes

## Workspace layout
- Teaching workspace lives at `007_C/teach_skill_C_workspace/`. All `lessons/`, `reference/`, `learning-records/`, `MISSION.md`, `RESOURCES.md`, and this file live here.

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
- `0008-const-and-volatile.html` — const/volatile as contracts with the compiler. The two-question pointer test, `const char *` params, assembly at -O2, the `const volatile` combo, all five book exercises.
- `0009-function-pointers-and-callbacks.html` — Chapter 28: functions have addresses (text segment), the parens-matter syntax, dispatch tables, callbacks, qsort comparators. Five book exercises. Companion: `reference/function-pointers.html`.

## Where the user is right now
- Page 93 of *A Little Book of C* — finished Chapter 27 (const/volatile).
- Completed Exercise 2 (volatile + assembly comparison) in session 0002.
- Lesson 0008 created covering Exercises 3, 4, 5 (const param, const pointer variants, const volatile).
- Lesson 0009 created (Chapter 28 — Function Pointers & Callbacks). User hasn't worked through it yet.
- Next: work through lesson 0009's five exercises, then Chapter 29 — Deep vs Shallow Copies (p. 96).

## Open questions
- Weekly time budget not yet specified — calibrate lesson density once known.
- Confirm details of "A Little Book of C" (author/edition) for RESOURCES.md citation.
- How did lessons 0003–0008 feel? Any recalibration needed for future lessons.
- Whether to keep producing companion reference sheets for every lesson (0009 got one — worth it?).

## Style preferences (emerging)
- Tolerates, even enjoys, multiple formulations of one concept — keep offering "index form vs pointer form" parallels
