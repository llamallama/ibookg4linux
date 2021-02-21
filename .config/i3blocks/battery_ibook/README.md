# iBook G4 Battery Monitor

Custom i3block battery monitor for iBook G4 (and possibly other) PMU based PowerPC Macintosh laptops.

## Why
Most battery monitors use the standard `acpi` command for their battery stats. Unfortunately, `acpi` isn't aware of the non-standard sys filesystem path for Apple PMU based batteries. That path is `/sys/class/power_supply/PMU_battery_0`.

This script queries `/sys/class/power_supply/PMU_battery_0/uevent` directly. It is capable of displaying the current charge and whether or not the machine is plugged in or not.

## Requirements
* i3blocks
* Font Awesome


## Config

```
[battery_ibook]
command=$SCRIPT_DIR/battery_ibook
markup=pango
interval=30
```