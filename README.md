# electrical-meter

## esphome
### initialize new boad config
```podman run --rm -v /home/keks/code/esp/electrical-meter:/config -it docker.io/esphome/esphome:2022.11 wizard electrical-meter.yaml```

### upload initially via device
```podman run --rm -v "${PWD}":/config --device=/dev/ttyUSB0 -it docker.io/esphome/esphome:2022.11 run electrical-meter.yaml```

### upload initially via ota
```podman run --rm -v "${PWD}":/config -it docker.io/esphome/esphome:2022.11 run electrical-meter.yaml```

## esphome assistant
this is for debugging without having [home assistant](https://www.home-assistant.io/)

```podman run --rm --net=host -v "${PWD}":/config -it docker.io/esphome/esphome:2022.11```

# board pinouts
![az-delivery esp32 v4](./az-delivery-esp32-v4_pinout.png)