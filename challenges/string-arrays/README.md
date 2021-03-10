---
tags:
  - iteration
---

# Iterating over an array of strings

In hierarchical documents, it should be possible to iterate over arrays of string values using `@` to refer to the current node. 

This should be standard and acknowledged in the RML specifications.

## Extensions

* This acknowledged in the RML specifications and RML testing cases to make sure RML implementations are properly supporting JSONPath.

## Discussions

- https://github.com/RMLio/rmlmapper-java/issues/95

* See this YARRRML mapping as example:

```yaml
prefixes:
  grel: "http://users.ugent.be/~bjdmeest/function/grel.ttl#"
  rdfs: "http://www.w3.org/2000/01/rdf-schema#"
  fo: "http://purl.org/ontology/fo/"
mappings:
  ingredients:
    sources:
      - ['ingredients.json~jsonpath', "$.[*].ingredients[*]"]
    s: fo:ingredient/$(@)
    po:
      - [rdfs:label, $(@)]
      
  recipes:
    sources:
      - ['ingredients.json~jsonpath', "$.[*]"]
    s: fo:recipe/$(id)
    po:
      - [fo:ingredients, $(ingredients)]
```

## Conclusions
