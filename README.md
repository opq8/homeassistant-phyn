# homeassistant-phyn

Home Assistant custom component for interfacing with [Phyn](https://www.phyn.com) Smart Water Assistant.

This integration currently provides the following capabilities:

Phyn Plus (PP1, PP2):
- Daily water usage (compatible with Energy dashboard)
- Average water temperature, pressure, and flow (realtime not available)
- Shutoff valve control
- Away mode control

Phyn Smart Water Sensor (PW1):
- Coming soon!

# Installation

## Installation via HACS

This custom component can be integrated into [HACS](https://github.com/hacs/integration), so you can track future updates. If you have do not have have HACS installed, please see [their installation guide](https://hacs.xyz/docs/installation/manual).

1. Select HACS from the left-hand navigation menu.

2. Click _Integrations_.

3. Click the three dots in the upper right-hand corner and select _Custom Repositories_.

4. Paste "https://github.com/opq8/homeassistant-phyn/tree/development" into _Repository_, select "Integration" as _Category_, and click Add.

5. Close the Custom repositories dialog after it updates with the new integration.

6. "Phyn Smart Water Assistant" will appear in your list of repositories. Click to open, click the following Download buttons.

## Manual installation (experts only)

If you do not use HACS, you can still manually install the integration.

1. Download a copy of aiophyn from rsocko's repo: https://github.com/rsocko/aiophyn/tree/get_away_mode

2. Copy the aiophyn/ folder to your Home Assistant config folder (e.g. config/aiophyn/)

3. Download a copy of this integration (homeassistant-phyn) from my repo: https://github.com/opq8/homeassistant-phyn/tree/development

4. Copy the phyn/ folder to your Home Assistant custom_components folder (e.g. config/custom_components/phyn/)

5. Restart Home Assistant to pick up the new phyn plugin and aiophyn dependency.

## Configuration

Configuration is done via the Home Assistant UI as an Integration and as Devices.

* In the Home Assistant UI, go to Settings > Devices & services, go to the Devices tab, and click "+ Add Device" on the bottom right.

* Search for and select "Phyn".

* A prompt will appear for you to enter your Phyn Account username and password. (This could sometimes take 2-3 minutes, or longer)

# Changelog

_2023.01.00_ (from [@MizterB](https://github.com/MizterB/homeassistant-phyn))

- Initial release

_2023.08.00_ (from [@rsocko](https://github.com/rsocko/homeassistant-phyn))

- Added away mode control

_2023.10.00_

- Fixed integration to for setups with water sensors