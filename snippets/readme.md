# Snippets

ESPhome snippets are designed to be only one object which can be included when needed multiple times to reduce duplication and cluttering.

A Snippet can have other snippets as dependency, never other [packages](../packages/readme.md)

## Example include yaml

```yaml
...
  <object_path>:
    !include /config/snippets/*/<snippet_name>.yaml
```
