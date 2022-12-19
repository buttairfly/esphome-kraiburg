# packages

ESPhome packages are designed to be independent, interchangeable and orthogonal.

packages may require a certain board, sensor or both to work correctly.

A package should always be included as a ESPhome [local-package](https://esphome.io/guides/configuration-types.html#local-packages).

A package always specifies a full ESPhome object with path, never only an object.

This way, it can be merged with other packages.

A package may need [snippets](../snippets/readme.md) or other packages as dependencies.

## Example include yaml

```yaml
packages:
  ${package-name}: !include packages/${package-file}.yaml
```
