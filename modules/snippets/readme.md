# Snippets

ESPhome snippets are designed to be only one object which can be included when needed multiple times to reduce duplication and cluttering.

A Snippet can have other snippets as dependency, never other [modules](../readme.md)

## Example include yaml

```yaml
...
  <object_path>:
    !include ./snippets/*/<snippet_name>.yaml
```

## Naming scheme for snippets
The same naming [scheme as for modules](../readme.md#Naming_scheme_for_modules) applies.
