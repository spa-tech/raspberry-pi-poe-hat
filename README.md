# raspberry-pi-poe-hat

The official Raspberry Pi 5 PoE hat is not yet released at this time so a few other manufacturers have produced hats. This repo contains the changes required to make them work for some special cases such as booting from
USB instead of MMC which draws more power and requires a firmware setting change.

## WaveShare PoE Hat

If booting from a USB drive instead of MMC while using the PoE hat you may need to add this line to /boot/firmware/config.txt:

```
usb_max_current_enable=1
```
