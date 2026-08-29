# Dimmers and relays

Digital dimmer channels default to Trailing Edge with load detection. Confirm each channel against the load before use. Channels must be powered.

## Front-panel confirm

Short press toggles the channel. Indicator colour is the mode: yellow Trailing Edge, green Leading Edge.

- Solid yellow: load matches Trailing Edge. Double-press. Rapid yellow flash confirms.
- Slow flashing red: iron-core load. Hold >10 s to Leading Edge. Rapid green flash confirms.
- Still flashing red after Leading Edge: the default load profile is wrong. Customise in Commission.

Confirm on a new unit, and again after returning a channel to Trailing Edge.

## Commission

Channel confirmation, dimming mode, warn-before-off, custom load profile, and custom dimming curve are Properties on the dimmer. Voltage-free relays: convert unit type, interlock channels.

## Measurement

Device ID uniquely identifies a unit on the Measurement application. Each analogue is a Channel ID. Create Measurement objects in Applications → Measurement. Broadcast interval and on-change threshold add C-Bus traffic.
