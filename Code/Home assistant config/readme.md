# Introduction

As of version [3.2.0](https://github.com/visualapproach/WiFi-remote-for-Bestway-Lay-Z-SPA/releases/tag/v3.2.0) the spa is automatically added as a device in Home Assistant by [MQTT discovery](https://www.home-assistant.io/docs/mqtt/discovery/).
The YAML-files included in this directory consists of optional sensors, automations, and ideas that are not exposed by default.
The [build instructions](https://github.com/visualapproach/WiFi-remote-for-Bestway-Lay-Z-SPA/blob/master/Build-instructions-Bestway-WiFi-remote.pdf) contains an overview of the available MQTT topics.

# Instructions

### MQTT Discovery

After entering the credentials of your MQTT broker under MQTT config, the spa with entities will be registered in Home Assistant. Ensure that MQTT Discovery is enabled in Home Assistant with `homeassistant` as discovery prefix.


### YAML
Add the following to your `configuration.yaml`:
```
homeassistant:
  packages: !include_dir_named packages
```
Create `packages` directory in your Home Assistant configuration directory (where your `configuration.yaml`is located) and save the YAML-files inside.
Restart Home Assistant.

If you make any changes in the YAML-files in the future, you can reload your changes without restarting by navigating to `Configuration -> Settings` and then click on `Manually configured MQTT entities` and `Template entities`.
