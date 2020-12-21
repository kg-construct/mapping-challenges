---
tags:
  - term-generation
---

# Datatype Map

The possibility to create a literal with a datatype,
where the datatype is derived from source data.

> Please see language map discussion, this feels heavily related

## Extensions

- What if we want to derive, e.g., 'xsd:integer' from 'int'? See `input-4`
  - should be provide "shortcuts" for prefixes? e.g what if we have `xsd:integer` in the data source? See `input-3`
    - if no prefix is included(e.g. `integer`), we can probably repurpose the templating to prepend the `http://www.w3.org/2001/XMLSchema#`? See `input-2`
  - related to data transformations?
- What if the data source already typehints the data?
  - e.g. SQL tables already have types, and in JSON you can already distinguish between strings, numbers, and booleans
    - Do we want to handle things such as
      - "if the JSON datatype of key `num` is number, assume it's xsd:integer, otherwise assume it's xsd:decimal" See `input-5`
- What if the datatype is in another data source?
  - related to joins, also see <https://github.com/kg-construct/mapping-challenges/issues/23>

## Conclusions

The datatype of a term SHOULD also be generated, similar to how values of terms are generated: constant, template, w/data transformation, joining from other data
