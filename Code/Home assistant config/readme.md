Instructions:

As of version [3.2.0](https://github.com/visualapproach/WiFi-remote-for-Bestway-Lay-Z-SPA/releases/tag/v3.2.0) the spa is automatically added as a device in Home Assistant by [MQTT discovery](https://www.home-assistant.io/docs/mqtt/discovery/).

Add the following to you `configuration.yaml`:
```
homeassistant:
  packages: !include_dir_named packages
```
Create `packages` directory in your Home Assistant configuration directory (where your `configuration.yaml`is located) and save `layzspa.yaml` inside.
Restart Home Assistant.

If you make any changes in `layzspa.yaml` in the future, you can reload your changes without restarting by navigating to `Configuration -> Settings` and then click on `Manually configured MQTT entities`.

There are two 4-wire error state sensors which must be uncommented in `layzspa.yaml` in order to use.
