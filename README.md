# pi-httpboot-uefi
EEPROM with setting for http booting UEFI. 

Boots into uefi from https if ethernet cable is inserted. normal sd/usb boot if there is no ethernet. 

Install with `rpi-eeprom-config --edit signed-pieeprom.bin`     

Or rename signed-pieeprom.bin and signed-pieeprom.sig to pieeprom.bin and pieeprom.sig and then try overwriting files on normal eeprom instalation methods https://github.com/raspberrypi/rpi-eeprom/releases

EEPROM contains this settings shown below and a signing key that matches boot.img and its signature.

```
[all]
BOOT_ORDER=0xf417
HTTP_HOST=github.com
HTTP_PATH=/Marcinoo97/pi-httpboot-uefi/raw/master/UEFI-boot/pi5/
NET_INSTALL_ENABLED=0
```
