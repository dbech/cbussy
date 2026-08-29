# Occupant UI

What occupants and installers see after objects exist.

## Visualization

Configurator Vis. structure and Visualization. Levels and plans for PC/Tablet (`/scada-vis`) and Smartphone (`/scada-vis/touch`). Plan editor places objects, links, labels, images, frames, gauges, cameras, graphs. Control type on an object element picks slider, shutter, and so on.

Smartphone visualization does not host schedulers.

## Scenes

Configurator Scenes: trigger group plus components and object values. Run, save live values, duplicate, local vs remote scene control. Wall-plate scenes are stored locally in the plate; controller scenes are separate. HomeKit scenes are one button per scene.

## Clocks

**Schedulers** (UG ch.8) are date/time on an object. Configurator → Schedulers → Schedulers (not Holidays). Add scheduler, then Events. Specific time, sunrise, or sunset. Day of week / month filters. Lighting off at 22:00 Friday is target 0, ramp 0 s.

Click the scheduler **name** to edit it, including after Duplicate (`… copy`). Holidays is an exception calendar (no effect / skip / holidays only).

The home-page Scheduler module edits times on schedulers that already exist. Occupants cannot add objects there.

**Timers** (UG ch.7) run a duration then return a value. Not a daily clock. Max about 30.

**Automations** (UG ch.9) combine object conditions, time conditions, periods, and actions. Separate app module.

Controller clock/timezone must be correct.

## Trends

Trend logs store selected object data in controller memory and sync it to the internal microSD card. Add and edit them in Configurator → Trend logs; occupants can change views but cannot create logs.

Choose Absolute for actual values or a Counter mode for deltas. Set display resolution, decimal places for floating-point objects, and retention for resolution data (up to 5 years) and daily data (up to 10 years). Trends support day, week, month, year, current/previous, single/multiple, graph/data, direct links, and visualization frames. They are not supported in Smartphone Visualization.

## User access

Configurator → User access supports unrestricted access, a common PIN, or individual logins. Per module, grant None, Partial, or Full access; Partial selects individual visualization pages, schedulers, trends, emergency-light groups, Manager rooms, or apps.

NAC2 is designed for up to 50 visualization users subject to CPU load; AC2 is limited to 8. Login is 2–20 characters using letters, digits, hyphen, or underscore. Passwords require at least 8 characters with uppercase, lowercase, and a digit. Admin access is separate from occupant module access.

## Manager and cloud

Manager Config: floors, rooms, widgets bound to objects. Manager is the occupant view of that structure.

Cloud: install Cloud connector, IoT 3rd Party API, Management, Manager. Enable Cloud connector and the IoT API checkboxes. Management → Cloud Access → occupant account. Pair Controller only in the first five minutes after boot. Phone app is Clipsal C-Bus Manager on that same account. Empty Config means empty app. Cloud needs gateway and DNS.

LAN without cloud: `/scada-vis` and `/scada-vis/touch`.

## HomeKit

Store app Homekit (`homekit-cbus`). Add Device or Bulk, set Type of Control (Light Switch, Light Dimmer, …), Save to HomeKit, Apply changes, QR code.

Phone and controller on the same Wi-Fi for first pair. Home owner adds the accessory. Controller is a bridge. Uncertified → Add Anyway. Local control after pairing is Wi-Fi. Remote and Home automations need HomePod or Apple TV 4th gen+. Names: room + function, for Siri.

HomeKit is not Matter. IoT API is not HomeKit.
