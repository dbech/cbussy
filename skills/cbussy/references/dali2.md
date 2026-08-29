# DALI-2 gateway

C-Bus talks to DALI fittings through a DALI-2 gateway. Commission owns scan, addressing, and reconcile.

## Addressing

DALI short addresses and DALI groups are on the DALI line. C-Bus group addresses are separate. Broadcast on DALI is a line-wide command.

## Scan and reconcile

Scan the DALI line from the gateway in Commission. Identify fittings, then Reconcile with project devices. After reconcile, C-Bus input units see the fitting by Object ID. Readdressing the DALI short address later does not hide a reconciled fitting.

## Colour

CCT and Hue/Saturation are mapped C-Bus → DALI. Workbook has dedicated C-Bus to CCT and C-Bus to Hue/Saturation exercises. Controller schedulers can apply circadian control to those groups.

## Health

Missing devices vs Discover Faults: Faults looks for duplicate short addresses, missing comms, and broken fittings when the gateway fault status is stale. That scan can take a while.

Measurement uses Device ID and Channel ID like other C-Bus units.

Emergency DALI fittings continue into the controller's emergency-lighting workflow after gateway commissioning.
