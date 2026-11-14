# C Resources

Curated, high-trust sources. Knowledge should be drawn from these, not from parametric memory. Wisdom comes from the communities.

## Knowledge

- [Beej's Guide to C Programming](https://beej.us/guide/bgc/)
  Approachable, complete, free, conversational. Use for: pointers, memory models, the stuff textbooks make dry. Often the clearest first stop.
- [cppreference — C reference](https://en.cppreference.com/w/c.html)
  The authoritative standard library + language reference. Use for: exact semantics of any function (`scanf`, `strcat`, `strlen`…), return values, parameter types, and the precise wording on undefined behavior. Dry but unfakeable.
- [comp.lang.c FAQ (c-faq.com)](https://c-faq.com/)
  Decades-old, veteran-curated answers to classic C gotchas. Use for: null pointers, array/pointer decay, `scanf` pitfalls, the questions every C learner eventually asks.
- ["What Every C Programmer Should Know About Undefined Behavior"](https://blog.llvm.org/2011/05/what-every-c-programmer-should-know.html) — LLVM blog (3-part series)
  Explains why UB is *worse than "it just crashes"* — compilers exploit it. Use for: building the instinct that UB is a correctness problem, not a robustness one.
- _A Little Book of C_
  User's current primary text and the spine of their study. Confirm author/edition.

## Wisdom (Communities)

- [r/C_Programming](https://www.reddit.com/r/C_Programming/)
  Well-moderated, knowledgeable, hostile to bro-science. Use for: code critique, conceptual questions, and seeing how working C programmers reason.
- [Stack Overflow — `[c]` tag](https://stackoverflow.com/questions/tagged/c)
  High volume, good signal if you filter to highly-voted answers. Use for: specific "why does X behave like Y" questions — usually already asked.

## Gaps
- No embedded/systems-specific resource yet — add when mission moves toward tools/hardware.
- No debugging/tooling resource yet (gdb, valgrind, AddressSanitizer) — will need one before the user builds anything substantial. Add when we reach the "build a real program" milestone.
