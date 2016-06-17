
## Software von Gl.Inet

Die Software (Firmware) wird ständig weiter-entwickelt, um neue Funktionieren hinzuzufügen, Fehler zu beheben, und um das allgemeine Anwendererlebnis zu verbessern
Wir stellen aktualisierte Software regelmäßig bereit, daher kann es vorkommen wenn Sie den Router erhalten, dass evtl eine veraltete Version installiert ist, sollte dies der Fall sein
empfehlen wir eine aktualisierung der Software

1. Ist eine aktualisierung verfügbar, erscheint ein "New" Symbol im Webinterface
2. Klicken Sie auf das Firmware Symbol, hier haben Sie verschiedene Möglichkeiten, die installierte Version wird angezeigt.
3. Sie können die Option der automatischen Firmware aktualisierung nutzen, so aktualisiert sich der Router eigenständig (Option Standardmäßig deaktiviert)
4. Sollte eine neue Firmware vorhanden sein, erscheint der "Download" Button, Mit diesem können Sie den Download starten.



![Lan IP](src/firmware.png)

## Firmware aktualisieren per Webinterface

Klicken Sie den "Download" Button um die aktualisierung der Firmware zu beginnen, dieser Vorgang kann einige Zeit dauern jeh nach der Internetverbindung

![Lan IP](src/firmware1.png)

Sobald der Download abgeschlossen ist, prüft das Gerät die Firmware, sobald die Prüfung erfolgreich war erscheint der `upgrade` Button 
**Es wird empfohlen die Checkbox "Keep Settings" abzuwählen, um eine saubere installation zu haben**

*Wenn es ein Problem gab mit der Einstellung "keep settings" (Router nicht erreichbar o.ä) drücken sie mindestens Acht Sekunden lang den Reset-Schalter**

![Lan IP](src/firmware2.png)

## Eine eigene Firmware hochladen

Ehe wir eine neue Firmware veröffentlichen, stellen wir diese erst zum testen bereit die Adresse lautet: http://www.gl-inet.com/firmware/testing

Sie können auch ihre eigene Firmware erstellen (OpenWRT, LEDE)

1. Klicken Sie auf "Upload Firmware" es erscheint eine Dropbox wo Sie die Datei hochladen können.

Warnung: Sie sind dafür verantwortlich, dass die Firmware kompatibel ist, sie können Ihren Router "bricken" und müssen Ihn dann neu flashen (u-boot Reset)

![Lan IP](src/firmware3.png)

##  Mit der aktualisierung beginnen

Nachdem Sie die Firmware heruntergeladen haben, können Sie mit dem Upgrade beginnen. klicken Sie dazu auf "Upgrade"

1. Nach ungefähr drei Minuten ist die aktualisierung abgeschlossen
2. **Nicht vom Strom trennen.** falls dies passiert, ist unter Umständen das Gerät defekt "gebricked".
3. Nach der aktualisierung müssen Sie sich erneut verbinden, Evtl wird das WLan Kennwort zurückgesetzt auf das standard Kennwort.

![Lan IP](src/firmware4.png)

## Gerät auf Werkseinstellungen zurücksetzen (webinterface)

Wenn Sie Probleme mit einigen Einstellungen haben (z.B Repeater Modus, und können sich nun nicht mehr verbinden) so können Sie den Router auf Werkseinstellungen zurücksetzen.

**Werkseinstellung** bedeutet dass alle Einstellungen auf die Standard-Einstellungen gesetzt werden, eine Werkseinstellung stellt keine alte Firmware wieder her.

1. Um die Einstellungen auf die Werkseinstellungen zu setzen drücken Sie den "Revert to Factory Default" Button.
2. Lesen Sie die Warnungen und klicken Sie auf "Revert Now" , dieser vorgang dauert 1-2 Minuten.

![Lan IP](src/firmware5.png)

### Werkseinstellungen wiederherstellen (reset Taster)

**Nachdem das System gestartet ist**, Sie können den Reset Taster für acht Sekunden drücken. Die LEDS blinken in einem Muster um zu signalisieren dass der Werksreset geklappt hat. 

Diese Funktion funktioniert  in der Original-Firmware, für andere Firmware ist dies nicht sichergestellt

## Einen "gebrickten" Router wiederherstellen

Manchmal kann es vorkommen dass der Router "gebrickt" ist, also unbenutzbar und nicht reagiert, dies kann insbesonderen auftreten bei eigener Firmware, oder bei veränderter Dritt-Firmware

Alle unsere Router besitzen ein seperates Web-Interface um einen nicht mehr funktionierenden Router wiederherstellen zu können
(U-Boot)

Sie können die Original Anleitung hier lesen: http://www.gl-inet.com/how-to-enter-the-uboot-web-ui/ 

1. Verbinden Sie ein Netzwerkkabel mit dem Router (Nur eine Netzwerkschnitstelle benutzen)
2. Den Reset Taster feste gedrückt halten; danach Strom anschließen 
3. Die LEDS fangen das blinken an, Siehe Videos für Details (Reset Taster gedrückt halten)
4. Den Reset taster loslassen sobald die Leds `5` mal geblinkt haben für die Modelle: AR150, AR300M and 6416. Für den MT300N und MT300A, blinken die Leds dreimal,danach ist das u-Boot Webinterface geladen
5. Vergeben Sie manuell die Ip-Adresse am Rechner: `192.168.1.2`
6. Benutzen sie Google Chrome oder Firefox und rufen Sie die Webseite auf: `http://192.168.1.1`
7. Wählen Sie die original Firmware
8. Warten Sie 3 Minuten, Gerät nicht vom Strom trennen während des Vorgangs.

AR150:

[](https://youtu.be/vuMCaIub7K8)

MT300N und MT300A

[](https://youtu.be/RETQdRS1cLY)

GL.iNet6416 und vollständiger aktualisierungs Prozess

[](https://youtu.be/-E8EvDnJq0c)
