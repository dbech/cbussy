# Integration

## BACnet

IP server. NAC 2000 points. Objects on the controller are the BACnet points. Settings are in FlashSYS / Network BACnet pages and WB p.260.

## Modbus

RTU on RS-485 (up to 31 devices in the datasheet) and Modbus TCP. Profiles are JSON. Map registers to objects. User Parameter objects (application 250) are the usual holding pens. WB p.374–401 is the worked example.

## Lua

Kinds: event-based, resident, scheduled, start-up. Editor has Helpers and object lists. Event scripts fire on object change. Resident scripts loop. Scheduled scripts fire on a time. Prefer resident over a tight scheduled poll when CPU matters.

Weather API in the workbook is a resident script writing Measurement and User Parameter objects.

## CNI and other interfaces

The controller can act as a C-Bus Network Interface for commissioning and maintenance. CNI is enabled by default on TCP port 10001 and can be disabled or moved in the controller configuration. In Toolkit use type CNI, the controller IP address, and the configured port. The documented defaults are Ethernet `192.168.0.10`, USB-B `192.168.254.10`, and port `10001`.

Toolkit projects can be imported as CGL files. Controller objects can also be populated by the sniffer or added manually. USB-B and Ethernet can operate together.

IoT 3rd Party API is REST. Cloud connector is the Schneider cloud tunnel. MRA/MTC and Security application objects are UG 4.7.6–4.7.7.
