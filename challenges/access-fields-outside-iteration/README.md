---
tags:
  - iteration
---

# Access Fields outside Iteration

The possibility, within a specific iteration, to access fields outside that iteration.
Typically to build unique identifiers using ids at different hierarchical levels.

## Extensions

- This is not only relevant for parent-(grand)child-like relationships, but also for 'neighbours'. See `output.ttl`.
- What if this is combined with a join? See `input-2`.

This is also related to, e.g., handling multiple values (so for `output.ttl`, `ex:hasCar` could also return use rdf:List), but that's a different challenge.

## Discussion

- At what point is this a part of the reference formulation, or of the mapping language specification?
