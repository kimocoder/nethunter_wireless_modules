# nethunter_wireless_modules


## How to add to kernel
Add to your drivers/net/wireless/realtek/Kconfig:

```
source "drivers/net/wireless/realtek/rtl8822bu/Kconfig"<br>
source "drivers/net/wireless/realtek/rtl8812au/Kconfig"<br>
source "drivers/net/wireless/realtek/rtl8188eus/Kconfig"<br>
```

And add to your drivers/net/wireless/realtek/Makefile:

```
obj-$(CONFIG_RTL8822BU)         += rtl8822bu/<br>
obj-$(CONFIG_88XXAU)            += rtl8812au/<br>
obj-$(CONFIG_RTL8188EU)         += rtl8188eus/<br>
```

## Notes om using all modules

Only 1 driver may be added inline/built-in of rtl8812au or rtl8822bu
The rtl8188eus must always be a module.
