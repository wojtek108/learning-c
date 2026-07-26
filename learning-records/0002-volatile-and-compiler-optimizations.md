# `volatile` and Compiler Optimizations

Worked through Exercise 2 from the "Try It Yourself" section on page 93 of *A Little Book of C*: declared a variable with and without `volatile`, incremented it in a loop, and compared the generated assembly at `-O2`.

Key insight: `volatile` forces the compiler to issue a real memory read and write on every access, preventing loop elimination and register caching. At `-O2`, the non-`volatile` version had its loop completely removed — the compiler pre-computed the final value and passed it directly to `printf`. The `volatile` version retained the full loop with memory round-trips per iteration.

Also noted the importance of optimization level: at `-O0` (default), both versions look nearly identical because the compiler doesn't analyze or eliminate code.

## Evidence
- `constant_volatile/ex21.c` / `ex21.s` — no `volatile`, with `-O2`, loop eliminated
- `constant_volatile/ex22.c` / `ex22.s` — with `volatile`, with `-O2`, loop preserved
- `lessons_learned/04_volatile_and_compiler_optimizations.md` — post-session write-up

## Next Up
Exercise 3, page 93: create a function with `const char *msg` and try to modify it — explores why `const` on a `char*` parameter is prohibited.
