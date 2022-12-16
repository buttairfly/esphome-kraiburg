# Modules

ESPhome modules are designed to be independent, interchangeable and orthogonal.

Modules may require a certain board, sensor or both to work correctly.

A module should always be included as a ESPhome [local-package](https://esphome.io/guides/configuration-types.html#local-packages).

A Module always specifies a full ESPhome object with path, never only an object.

This way, it can be merged with other modules.

A Module may need [snippets](./snippets/readme.md) or other modules as dependencies.

## Example include yaml

```yaml
packages:
  ${module-name}: !include modules/${module-file}.yaml
```

## Naming scheme for modules
A module has the following naming rule:
`${module-name}_${board-name}_[${peripheral-name}_...].yaml`

The `module-name`, `board-name` and `peripheral-name` can consist of several words, which are connected by `-`

A board dependency is represented by the `${board-name}` or `any` if it is available for all boards.

A peripheral dependency is represented by the `${peripheral-name}` or by `none` if it has no additional dependency. Multiple dependencies are listed by more underscores. Dependencies could be other modules or sensors.
