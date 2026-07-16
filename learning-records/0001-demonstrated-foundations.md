# Demonstrated foundations in arrays, pointers, and strings

Across the files in this directory (`arrays.c`, `recall.c`, `strings.c`, the `exer_*` and `vowel_*` family), the user has shown working command of: one-dimensional arrays and indexed iteration; the equivalence `arr[i]` ≡ `*(arr+i)`; taking addresses with `&`; pointer arithmetic over both `int` and `char` arrays; null-terminated C strings and indexing to `'\0'`; and the standard `<string.h>` trio `strlen`/`strcpy`/`strcat`/`strstr`.

Notably strong signals: they re-implemented `mystrlen` **three ways** — index counting, `*(ptr+i)` traversal, and pointer-difference (`end - start`) — the last being a genuinely non-trivial insight (pointer subtraction yields an element count, not a byte count). They also wrote `count_vowels` twice (nested-loop char search, then a `switch` fallthrough), which shows deliberate exploration rather than copying. This sets the floor for what not to re-teach.

## Evidence
- `exer_strlen_pointers_arithmetic_1.c` — returns `(input - start)` correctly
- `recall.c` — prints `&x`, `px`, and `&px` distinctly, demonstrating the three-level distinction (value / address-of / address-of-pointer)
- `vowel_c2.c` — clean `switch` fallthrough for vowel classification

## Implications
The next frontier is **memory safety**, not more syntax. Specifically: the pointer-vs-array storage distinction (an uninitialized pointer points nowhere; `strcat` can overflow a too-small buffer). This is the single highest-value lesson given current competence and observed bugs in `exercise_concatinate_inputs.c` and `common_str_ops.c`.
