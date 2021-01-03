---
tags:
  - iteration
---

# Iterating over Multivalue References

In hierarchical documents, it is currently not completely clear how to support multivalue references: do you always create the cartesian product? What about when the logical source is the same? Do you need join conditions? What if you want to generate a 'tree of RDF triples' based on the hierarchy of the data source?

Relevant discussion:

- <https://github.com/RMLio/rmlmapper-java/issues/28#issuecomment-708337948>
- <https://github.com/RMLio/rml-implementation-report/issues/11#issuecomment-514961278>
- <https://github.com/carml/carml/issues/52>
- <https://ieeexplore.ieee.org/document/6882016>

## Extensions

- What if you need both options? i.e., you want to generate both the 'natural iteration' triples, but also be able to skip a level?

## Discussions

- This explicitly doesn't discuss the need to access data outside of the iteration, there is a specific challenge for that.

## Conclusions
