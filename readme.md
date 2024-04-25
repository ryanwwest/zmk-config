## Rollow Firmware

I think you only need to flash the dongle now, not the splits.

When split flashes are needed, must first flash with the settings_reset which completely turns off bluetooth and allows master and peripheral BT connection to be made, but I believe all 3 device must be flashed into this followed by flashed with their regular firmware (for left peripheral use that one and not just the left one as that's master, and we only want master for the xiao dongle).

To get firmware, just commit something to Github and a Github action will run there and if no errors, produce a Firmware.zip artifact. Download that, and just drag the appropriate firmwares onto the splits/dongle after resetting them (double click reset button when plugged into USB).
