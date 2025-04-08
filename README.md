# HA-ecowitt-local-rest-yaml
Alternative to integrate EcoWitt Weatherstation through REST local API to Home Assistant

To use this yaml example you will have to make sure your gateway has a fixed or reserved IP and you place it in the placeholder.

http://<gateway_ip>/get_livedata_info

when you open that url in the browser you will get the JSON and can check if it is working properly.

On your HA create a folder named integrations in the config folder. Place the ecowitt.yaml in that folder with the correct URL
To include the configuration file (if not yet existing) open the /config/configuration.yaml and add the following lines to it

homeassistant:
  packages: !include_dir_named integrations

last but not least restart your HA to get the new entities.

Be aware that the method used here is depending on the gateway type you have and might change when upgrading firmware as it is
not an officially supported and undocumented way to retrieve the values.

Lovelace example using additional cards from HACS

[custom:mini-graph-card](https://github.com/kalkih/mini-graph-card)
[custom:compass-card](https://github.com/tomvanswam/compass-card)
[custom:tempometer-gauge-card](https://github.com/SNoof85/lovelace-tempometer-gauge-card-deprecated)
[custom:uv-index-card](https://github.com/t1gr0u/uv-index-card)

![Top](https://github.com/bqzero/HA-ecowitt-local-rest-yaml/blob/main/top.png?raw=true)
![Bottom](https://github.com/bqzero/HA-ecowitt-local-rest-yaml/blob/main/bottom.png?raw=true)
