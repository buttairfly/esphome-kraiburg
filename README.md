# esphome setup

## esphome

Note: the esphome version is in the form `YYYY.MM` e.g. 2022.11 and should be present in [.env](./.env)
### initialize new boad config
```sh
./esphome [-s KEY VALUE] wizard ${board-config}.yaml
```

### upload via ota or /dev/
```sh
./esphome [--device=${device}] [-s KEY VALUE] run ${board-config}.yaml
```

specify device always, when the board is new, later you can omit the device flag to use wifi.
It can be used, when you want to rename the wifi or use the rename functionality of esphome.

## esphome assistant
this is for debugging without having [home assistant](https://www.home-assistant.io/)

```sh
source .env && podman run --rm --net=host -v "${PWD}":/config -it docker.io/esphome/esphome:${ESPHOME_TAG}
```

# configurations
A configuration specifies a type of sensor.

A `secrets.yaml` file is needed in order to be able to compile the configs to a uploadable file.
See `secrets.yaml.example` as an example file.

# further descriptions
* see [boards](./boards/readme.md)
* see [packages](./packages/readme.md)
* see [snippets](./snippets/readme.md)
