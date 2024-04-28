# Raspberry Pi 5 PoE Hat Troubleshooting

If your hat powers the Pi 5 but doens't allow link or otherwise network access then this is the fix for you. The official Raspberry Pi 5 PoE hat is not yet released at the time of this writing so a few other manufacturers have produced hats. If you boot from USB instead of MMC you may run into an issue where while introducing the aftermarket hats, the Pi will no longer boot. You simply need to set a firmware option to leverage more power on the USB side of things to fix this. Follow the details below to make the change and the Pi will then power on from PoE and also boot from a USB drive thus being available on the network.

## WaveShare PoE Hat

If booting from a USB drive instead of MMC while using this PoE hat you may need to add this line to /boot/firmware/config.txt:

```
usb_max_current_enable=1
```

Now shutdown, install the PoE hat, and plug into PoE switch again to boot. 
