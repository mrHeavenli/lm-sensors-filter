# cpu-temp-monitor

Displays the temperatures of the cpu cores, by filtering
the output of ```sensors``` to only display the temperatures.

Output of ```sensors``` typically looks like this:

```
ucsi_source_psy_USBC000:001-isa-0000
Adapter: ISA adapter
in0:           0.00 V  (min =  +0.00 V, max =  +0.00 V)
curr1:         3.00 A  (max =  +0.00 A)

dell_smm-virtual-0
Adapter: Virtual device
fan1:           0 RPM

iwlwifi_1-virtual-0
Adapter: Virtual device
temp1:        +46.0°C  

nvme-pci-e100
Adapter: PCI adapter
Composite:    +44.9°C  (low  =  -0.1°C, high = +82.8°C)
                       (crit = +84.8°C)

nouveau-pci-0100
Adapter: PCI adapter
temp1:            N/A  (high = +95.0°C, hyst =  +3.0°C)
                       (crit = +105.0°C, hyst =  +5.0°C)
                       (emerg = +135.0°C, hyst =  +5.0°C)

coretemp-isa-0000
Adapter: ISA adapter
Package id 0:  +47.0°C  (high = +100.0°C, crit = +100.0°C)
Core 0:        +42.0°C  (high = +100.0°C, crit = +100.0°C)
Core 1:        +42.0°C  (high = +100.0°C, crit = +100.0°C)
Core 2:        +44.0°C  (high = +100.0°C, crit = +100.0°C)
Core 3:        +43.0°C  (high = +100.0°C, crit = +100.0°C)

BAT0-acpi-0
Adapter: ACPI interface
in0:           8.27 V  
curr1:       1000.00 uA
```
A bit cluttered, isn't it?

The script filters through this and displays the temperatures on a loop.
Typical output:
```
Core 0:        +44.0°C
Core 1:        +41.0°C
Core 2:        +43.0°C
Core 3:        +41.0°C
```

## Requirements

You might have to install ```lm-sensors```

## To Do

I may or may not follow up on these.
- Add colours
- Warning notifications

