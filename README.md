# esphome-AC-fan-controller
ESPHome Standalone 120 Volt AC Blower/Fan Speed Controlled by temperature range
# ESPHome Components for Wood pellet Stove Fan Control

This repository contains ESPHome configurations and components for controlling a stove fan using an ESP32. The setup includes a Dallas temperature sensor and an AC dimmer to manage the fan speed based on the temperature readings.

## Features

- **Temperature Monitoring**: Uses a Dallas temperature sensor to monitor the temperature.
- **Fan Speed Control**: Adjusts the fan speed using an AC dimmer based on the temperature.
- **Automated Reboot**: Reboots the ESP32 device a few times a day if the fan has been off for at least 10 minutes.
- **Web Server**: Provides a web interface for direct access and control.

Web portal:

<img src="https://github.com/stovedoctor/esphome-AC-fan-controller/blob/main/images/fan_ui_to_off.png" alt="AC dimmer module with blower and temperature sensor" width="50%">

HA dashboard and History:

<img src="https://github.com/stovedoctor/esphome-AC-fan-controller/blob/7ab314c0d0507d17723182830243cc7774a72c06/images/Ha%20pelet%20fan%20dashboard.png" alt="HA Dashboard" width="50%">
<img src="https://github.com/stovedoctor/esphome-AC-fan-controller/blob/6cf52e9fb5becb033ed536f8697a4a8b93ec1e61/images/ha%20fan%20histiory%20to%20off.png" alt="HA Dashboard" width="50%">

## Components

- **ESP32**: The microcontroller used for this project.
- **Dallas Temperature Sensor**: Measures the temperature to control the fan speed.
- **AC Dimmer**: Controls the fan speed based on temperature readings.
<img src="https://github.com/stovedoctor/esphome-AC-fan-controller/blob/d08dee3497813c8e713638efe107744abf9ffa9a/images/Prototypeacdimmer.png" alt="AC dimmer module prototype" width="50%">
<img src="https://github.com/stovedoctor/esphome-AC-fan-controller/blob/cbb32cb0735898e6e77d7a7884a12dd11342f0ee/images/ds18b20_connections.png" alt="AC dimmer module with blower and temperature sensor" width="50%">

## Configuration

The main configuration file is `esp32-test.yaml`. Below is a summary of the configuration:

- **WiFi Configuration**: Connects the ESP32 to your WiFi network.
- **API and OTA**: Allows integration with Home Assistant and over-the-air updates.
- **AC Dimmer**: Controls the fan speed.
- **Dallas Temperature Sensor**: Monitors the temperature.
- **Automations**: Includes an automation to reboot the device if the fan has been off for 10 minutes.

## Setup

1. **Clone the Repository**:
   ```sh
   git clone https://github.com/stovedoctor/esphome-components.git
   cd esphome-components
   Configure Secrets:

2: **Create a `secrets.yaml` File**
Create a `secrets.yaml` file in the same directory with your WiFi credentials:
```yaml
wifi_ssid: "YOUR_WIFI_SSID"
wifi_password: "YOUR_WIFI_PASSWORD"

   

