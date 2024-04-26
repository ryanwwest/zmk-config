## Rollow Firmware

I think you only need to flash the dongle now, not the splits.

When split flashes are needed, must first flash with the settings_reset which completely turns off bluetooth and allows master and peripheral BT connection to be made, but I believe all 3 device must be flashed into this followed by flashed with their regular firmware (for left peripheral use that one and not just the left one as that's master, and we only want master for the xiao dongle).

To get firmware, just commit something to Github and a Github action will run there and if no errors, produce a Firmware.zip artifact. Download that, and just drag the appropriate firmwares onto the splits/dongle after resetting them (double click reset button when plugged into USB).
- DO NOT send the settings_reset to anything if both halves are communicating with with dongle. It is very annoying to get both halves connected. After initial connection, it seems they just work, including after dongle firmware is updated. Just don't touch the splits unless to charge.

Don't use any repos that are just called 'zmk'. When I used zmk a few years back, I used this repo directly with much more content and compiled directly on my computer, but now github actions handles entire toolchain so I just need the zmk-config repo. zmk one is out of date.


config-clog/ is from the old clog zmk repo but it's not set up. Would need to change build.yaml to compile it as well if want to.

TODO encoders on rollow are working as buttons (push down) but not when moving left/right. Need to fix.
