# ESPHome

ESPHome works great on the TTGO ESP32 T-Display and has drivers for all the necessary pieces.  Connect it
to HomeAssistant and let HomeAssistant log to InfluxDB and visualize long-term data with Grafana.

## Building And Flashing the Unit

### Step 1: Launch ESPHome Docker container

The dev image is currently necessary for the display to function.  The documentation for the next/dev
image is avaiable at [next.esphome.io](https://next.esphome.io/).

    docker run --name esphome --rm -it --network host --privileged -v /dev:/dev -v $PWD:/config esphome/esphome:dev

### Step 2: Load Web UI

Should be http://localhost:6052 by default

### Step 3: Create

Copy contents of `sniffer.template.yaml` into ESPHome `sniffer0.yaml` or similar.

Update the secrets file appropriately or use the provided template as a starting point.

### Step 4: Flash ESP32

Attach to USB port of system running the ESP32 Docker container and Upload the newly created config.

### Step 5: Iterations

Now you can run the Docker container without `--privileged -v /dev:/dev` as the over-the-air update will
work.
