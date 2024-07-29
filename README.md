# Raspberry Pi 5 PoE Hat Troubleshooting

When powered by PoE, booting from a 2.5" SATA SSD via USB draws more watts than the Pi defaults allow. To get up and running, start with a fresh Pi, install the Pi OS on the SATA drive using Imager, then boot using an AC adapter.

Then make the changes below over SSH. 

## WaveShare PoE Hat

The following is necessary with this particular PoE hat and maybe others.

```bash
sudo vi /boot/firmware/config.txt
```

```bash
usb_max_current_enable=1
```

Now shutdown, install the PoE hat, and plug into PoE switch again to boot. 
