# JSON-LD-star

## Talking points
- Mirrors support for [triple terms](https://www.w3.org/TR/rdf12-concepts/#dfn-triple-term), [reifying triples](https://www.w3.org/TR/rdf12-concepts/#dfn-reifying-triple), and [annotations](https://www.w3.org/TR/rdf12-turtle/#dfn-annotation-syntax) from RDF-star (RDF 1.2).
  - A Triple Term is introduced using the `@triple` keyword. It is generally _not_ intended for general use, see instead `@reifier`.
  - A Reifying Triple is introduced using the `@reifies` keyword.
    - Associates the identifier of the containing object with the triple(s) extracted from the value of `@refier`.
    - Allows multiple triples to be reified.
  - An annotation is introduced using the `@annotation` keyword.
    - The triple(s) extracted from the containing object are asserted, and the identifier of the object value of `@annotation` is used as the reifier for those triples; the other values of the annotation object as asserted against that reifier (as usual).
