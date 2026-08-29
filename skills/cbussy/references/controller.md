# Controller

Web programming of 5500NAC2 (Network Automation Controller) and 5500AC2 (Application Controller). Same firmware family. NAC2 adds emergency and exit lighting.

## Access

Factory Ethernet IP is `192.168.0.10`. Hostname access is supported; factory hostnames are `5500NAC2` and `5500AC2`. USB-B is a second IP interface with a fixed address. The login page title follows the configured hostname. Cert is self-signed. The form encrypts credentials in the browser.

Configurator `/scada-main`. Apps `/apps/` on firmware 2.x. System/FlashSYS `/flashsys`.

Date and time: Utilities → Date and time, plus NTP in FlashSYS.

## Firmware and apps

From 2.0.0 an upgrade needs `*.img` and `*.sig`. Upgrade cannot be reversed. After 2.x the start page is `/apps/`. AC2 may pre-install Manager at 2.1.0+. NAC2 does not.

Install apps from Configure apps on the store. Store packages are Verified. A local IPK without its Schneider `.sig` fails with signature not valid. Typical apps: Cloud connector, IoT 3rd Party API, Management, Manager, Homekit, Automation, Timers.

## Objects

C-Bus group addresses are Objects. Bring them in via Controller Sync (Commission IP layer Transfer/Retrieve), CGL import from Toolkit, Add new object, or the bus sniffer.

Lighting: target 255 on, 0 off. Applications include lighting, trigger, enable, measurement, emergency, security, unit parameters, user parameters (250), MRA/MTC, error.

Tag map stores names. Save project after edits. Backup is Utilities → Backup → `*.tar.gz`.

## Commission layers

In a Commission project the controller is three layers: PC (C-Bus network interface), SYS (the controller), IP (project connection data only). A live scan shows PC and SYS. Give PC and SYS different unit addresses.

## HTTPS

Custom certificates: SEC guide in this folder. Generate root, CSR, service cert, install on the controller (FlashSYS SSL certificate) and on PCs/phones. HTTPS-only and non-default ports are in that guide.
