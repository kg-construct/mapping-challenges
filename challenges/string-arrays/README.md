---
tags:
  - iteration
---

# Iterating over an array of strings

In hierarchical documents, it is currently not possible to iterate over a array of string values. The current mechanism requires to provide a key to retrieve values when iterating on an array, it is not possible to reference the value of the object we are iterating on (in our case a string)

## Extensions

* 

## Discussions

- https://github.com/RMLio/rmlmapper-java/issues/95

* It has been discussed to be able to reference the root of a relative JSONPath using `$` , but still keeping the existing mechanism when `$` is not provided. See this YARRRML mapping as example:

```yaml
prefixes:
  grel: "http://users.ugent.be/~bjdmeest/function/grel.ttl#"
  rdfs: "http://www.w3.org/2000/01/rdf-schema#"
  fo: "http://purl.org/ontology/fo/"
mappings:
  ingredients:
    sources:
      - ['ingredients.json~jsonpath', "$.[*].ingredients[*]"]
    s: fo:ingredient/$($)
    po:
      - [rdfs:label, $($)]
      
  recipes:
    sources:
      - ['ingredients.json~jsonpath', "$.[*]"]
    s: fo:recipe/$(id)
    po:
      - [fo:ingredients, $(ingredients)]
```

## Conclusions
