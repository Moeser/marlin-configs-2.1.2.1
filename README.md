# My Fork Info:
I made my changes to the `release-2.1.2.1` branch.  Look for the new config dir in that branch
`config/examples/Creality/CR-10/BigTreeTech SKR Mini E3 3.0` .  I used mostly defaults from
the SKR Mini E3 2.0 configs, with some tuning to match my specific CR-10 setup.  I also added
poop emojis to the boot screen and status screen because I'm an immature geek like that, and the
toilet humor makes me chuckle every time the CR-10 boots up.  I made the images by hand, and
it took me a while to get them looking right, so if you're just here to copy the emojis for your
own Marlin fw, I humbly ask you to mention me somewhere so I get some credit for it. :)

I added configs for the BigTreeTech SKR Mini E3 V3 board for the old CR-10 hardware with BLTouch.
(Not CR-10S or v2 or v5 or whatever, just plain old CR-10)
This means the power supply is expected to be 12v, as are the heat bed, fans, hotend, etc.
The bed is expected to be 300x300 (or I guess 310x310?)

The BLTouch is expected to be the split connector where 3 pins are connected to the probe port and
two pins connected to the Z End Stop on the board.  **If you are plugging all 5 pins into the probe port
you'll need to edit the configs.**  The provided BLTouch offsets are tuned for mounting on the left side
of the extruder, but you'll still need to adjust them to match your exact setup.  Everyone's offsets
are slightly different.  (Look for `NOZZLE_TO_PROBE_OFFSET` if you want to hardcode it in the firmware)

Remember to reset the EEPROM, restore defaults, and save settings after flashing the new firmware.

If (like me) you're upgrading your old CR-10 with old BLTouch:
You might find that the 3-pin dupont connector on the BLTouch is wired incorrectly for the SKR Mini.
If that's the case you'll notice that the board won't even boot up unless the BLTouch is disconnected.
The dupont connector is fairly easy to re-arrange by hand.  No need to cut wires or solder or anything.
Just look up some youtube videos about removing pins on dupont connectors.  If your 3pin connector is
Red-Blue-Yellow or Red-Brown-Yellow, then you probably suffer from this issue too.  If your 3pin
connector is already Blue-Red-Yellow or Brown-Red-Yellow then you're probably fine.  Make sure to
double check any wiring changes with readily available diagrams and pinouts to be sure.

And now the disclaimer:
Of course all of these files and info are provided as-is.  You are responsible for double checking
all configs, wiring, advice, etc.  You assume all risk for any damage, problems, or other negative
events caused by using these configs or following any info I've mentioned.  While these configs and
tips worked for me, your experience may vary.  You agree to hold me liable for nothing.

Use at your own risk.

(boilerplate stock Marlin readme.md follows)

# Configurations
Pre-tested Configurations for Marlin Firmware. Links below…

> [!IMPORTANT]
> Before downloading configurations in ZIP format using the CODE button above you must select the correct branch for your version of Marlin.

## Branches

- **Release** branches will apply to most users. Select the branch for your version of Marlin.
  Version|File Tree|Download
  ---|---|---
  2.1.2.1|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.1.2.1))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.1.2.1.zip))
  2.1.2|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.1.2))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.1.2.zip))
  2.1.1|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.1.1))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.1.1.zip))
  2.1|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.1))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.1.zip))
  2.0.9.7|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.9.7))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.9.7.zip))
  2.0.9.6|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.9.6))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.9.6.zip))
  2.0.9.5|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.9.5))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.9.5.zip))
  2.0.9.4|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.9.4))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.9.4.zip))
  2.0.9.3|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.9.3))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.9.3.zip))
  2.0.9.2|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.9.2))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.9.2.zip))
  2.0.9.1|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.9.1))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.9.1.zip))
  2.0.9|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.9))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.9.zip))
  2.0.8.3|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.8.3))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.8.3.zip))
  2.0.8.2|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.8.2))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.8.2.zip))
  2.0.8.1|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.8.1))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.8.1.zip))
  2.0.8|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.8))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.8.zip))
  2.0.7.3|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.7.3))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.7.3.zip))
  2.0.7.2|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.7.2))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.7.2.zip))
  2.0.7.1|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.7.1))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.7.1.zip))
  2.0.7|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.7))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.7.zip))
  2.0.6.2|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.6.2))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.6.2.zip))
  2.0.6.1|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.6.1))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.6.1.zip))
  2.0.6|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.6))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.6.zip))
  2.0.5|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.5))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.5.zip))
  2.0.4|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.4))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.4.zip))
  2.0.3|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.3))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.3.zip))
  2.0.2|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.2))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.2.zip))
  2.0.1|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.1))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.1.zip))
  2.0.0|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-2.0.0))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-2.0.0.zip))
  1.1.9|([Browse](//github.com/MarlinFirmware/Configurations/tree/release-1.1.9))|([Download ZIP](//github.com/MarlinFirmware/Configurations/archive/release-1.1.9.zip))

- **Development** branches are also maintained here.
  - [bugfix-2.1.x](//github.com/MarlinFirmware/Configurations/tree/bugfix-2.1.x) contains unpublished features under development.
  - [bugfix-2.0.x](//github.com/MarlinFirmware/Configurations/tree/bugfix-2.0.x) contains upcoming patches for Marlin 2.0.x.
  - [import-2.1.x](//github.com/MarlinFirmware/Configurations/tree/import-2.1.x) is for new contributions. Submitted pull requests must be based on this branch.
  - [import-2.0.x](//github.com/MarlinFirmware/Configurations/tree/import-2.0.x) is for patches to Marlin 2.0.x configurations.
