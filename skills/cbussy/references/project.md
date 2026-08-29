# Commission project

Commission is the current Windows programmer for C-Bus field devices. Toolkit remains relevant to older units and CGL exchange.

## Layout

Explorer, Devices in Project, Network Devices, Workspace, Properties, Deployment Queue. Reset Window Layout if the UI is scrambled.

C-Gate 3 is the connection service under Commission.

## Network and demonstration setup

A C-Bus network needs a clock (one unit with clock enabled) and a network burden. Power-supply units can enable an in-built C-Bus supply. Confirm those fundamentals before treating scan or communication failures as software faults.

For a training or demonstration case, identify the physical interface, power-supply unit, enabled clock, burden, and every unit address before programming. Keep the project model aligned with the wired devices rather than treating the case as a fixed template.

Scan from the interface (PCI, CNI, or a controller PC layer). **Open Using** can attach a temporary Ethernet interface by IP. Orange highlights mean a temporary interface is in use. The dialog remembers up to 20 successful hosts.

Factory default controller IP in the manuals is `192.168.0.10`; verify the actual address before connecting.

## Toolkit

Run one of Commission or Toolkit against a unit at a time. Simultaneous use yields Device Not Ready.

## Deploy

Scan live units into Network Devices and add intended units from the Library to Devices in Project. Use **Readdress to Match Network** when the project and live unit addresses differ. Select the corresponding project and network devices together, then Deploy. Properties Save with **Deploy to Network** writes the unit; clear it only for a project-only edit.

Factory reset of a C-Bus unit is a Commission/Toolkit unit action, not the controller web Factory reset.

## Copy

WB FAQ: copy/paste units in the project; watch phantom group addresses that exist in software only.
