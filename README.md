# Raspberry Pi 5 PoE Hat Troubleshooting

If you want to boot a Pi 5 from a SATA SSD instead of MMC then you will need to make these changes. First use Pi Imager, install the preferred image on an SD FLASH, and boot from that MMC with AC adapter. 

## WaveShare PoE Hat

If booting from a USB drive instead of MMC while using this PoE hat you may need to add this line to /boot/firmware/config.txt:

```bash
sudo vi /boot/firmware/config.txt
```

```bash
usb_max_current_enable=1
```

Now shutdown, install the PoE hat, and plug into PoE switch again to boot. 
