# Echtzeituhr als Modul installieren (RTC) am Beispiel des GL-AR150

![AR150 RTC](src/ar150-rtc1.jpg)
## Die Kernel Module installieren

Wenn Sie unsere Standard-Firmware benutzen, installieren Sie die Pakete mit `opkg`

```
opkg update
opkg install kmod-i2c-gpio-custom
opkg install kmod-rtc-ds1307
```

Wenn Sie ihre eigene Firmware erstellen möchten, müssen Sie folgende Pakete auswählen
```
Kernel modules  --->  I2C support  --->  kmod-i2c-gpio-custom
Device Drivers  --->  Real Time Clock  --->  Dallas/Maxim DS1307/37/38/39/40, ST M41T00, EPSON RX-8025
```

## Anschließen des Moduls

Das Modul lässt sich sehr leicht installieren, Einfach aufstecken und die nachfolgenden Pins löten: `GND, VCC, SDA and SCL`.

![AR150 RTC](src/ar150-rtc2.jpg)

![AR150 RTC](src/ar150-rtc3.jpg)

## Software

Dies sind die GPIO Pins die vom Modul genutzt werden:

`SDA` <--> `GPIO1`
`SCL` <--> `GPIO17`

Nun müssen wir die Kernel Module laden, dies machen wir mit

```
insmod /lib/modules/3.18.29/i2c-gpio-custom.ko bus0=0,1,17
echo ds1307 0x68 > /sys/bus/i2c/devices/i2c-0/new_device
```

Um die Uhrzeit der Echtzeituhr auszulesen
```
hwclock -r
```

Um die Uhrzeit der Echtzeituhr mit dem Gl.Inet Router zu synchronisieren
```
hwclock -s
```

Um die Uhrzeit des Routers in Echtzeit-Modul zu schreiben
```
hwclock -w
```

