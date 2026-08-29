# Wall plates

Saturn, Saturn Zen, and eDLT keys are widgets. A key can hold one or more widget functions. An indicator can be assigned independently. Indicator behaviour follows the group on that widget.

## Key programming

Select the project unit → Properties. Set Function and Group per key widget (example: Toggle + lighting group). Set Indicator On Colour. Save with Deploy to Network. A C-Bus clock must be enabled somewhere on the network.

## Scenes on the plate

Up to 8 scenes, 64 scene items shared among them. Scene Manager is under Global.

Key functions: Scene Set, Scene Toggle, Scene Off, Scene Off/Down, Scene On/Up. Toggle/dim key functions only work for scenes stored in that same unit.

Large or occupant-editable scenes belong in a controller. The plate then sends a scene trigger.

## Profiles, sequences, timers

Profiles switch blocks of key behaviour. Sequences run ordered steps. Plate timers are local delays on the unit, not NAC Schedulers.

Linked widgets: one key can drive another widget or a duration.

## Join room

Model each divisible room zone with separate Lighting groups. Create a shared Trigger Control group with action selectors for joined-room scenes, plus an Enable group whose level selects the normal-room or joined-room profile.

Store matching all-on and all-off scenes in the participating plates, assign the same trigger group and selectors, then map each plate's keys per profile: local zone control in the normal profile and shared scene control in the joined profile. Program relay channels first, deploy every changed unit, and test both profile levels from each plate. The worked Commission sequence is WB p.347–373.

## Temperature and humidity

Integrated sensors broadcast on Measurement. Independently set interval and on-change. High/low alarms can switch lighting groups per profile. Install in the final location and power ≥1 hour before trusting temperature. Sensor lag can be up to 10 minutes. Temperature Offset calibrates the reading. Humidity needs a sane temperature offset.

Give the plate a unique Device ID, then create Measurement objects (temperature channel 0, humidity channel 1 is the workbook pattern).
