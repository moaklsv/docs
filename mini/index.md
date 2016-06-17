## Einrichtung
Für die Stromversorgung ist ein micro-usb Kabel beigelegt, dies verbinden Sie bitte mit einem USB Netzteil (z.B von einem Handy)

eine Minute warten und der Router ist zur erstmaligen konfiguration bereit.

![Connections](src/connections1.png)

Um den Router mit ihrem existierenden Netzwerk zu verbinden, Schließen Sie ein Netzwerkkabel vom Lan Port ihres Routers (z.B der Fritzbox) an den Wan Port ihres Gl-Inets Routers


![Connections](src/connections.png)

Jetzt können Sie sich mit einem Netzwerkkabel verbinden (Lan Port) oder per W-Lan.

![Connections](src/connections3.png) 
![Connections](src/connections4.png)

Die  Wlan Kennung ihres Mini-Routers ist auf der Rückseite gedruckt, er sollte eines der folgenden Formate besitzen jeh nach Modell ihres Routers

```
GL-iNet-xxx
GL-AR150-xxx
GL-AR300M-xxx 
GL-MT300N-xxx
GL-MT300A-xxx
```

Das standard Kennwort für das Wlan lautet "goodlife"

## Konfiguration

Der Router muss erstmalig eingerichtet werden, hierzu öffnen Sie ihr Webbrowser (Wir empfehlen Google Chrome oder Mozilla Firefox) und öffnen Sie die Webseite
[http://192.168.8.1](http://192.168.8.1) 

Sie sehen die Willkommens-Seite , dort wählen Sie bitte ihre Sprache, momentan unterstützen wir `Chinese` und `English`.
 
![Connections](src/welcome.png)

Danach wählen Sie ihre Zeitzone (Dies können Sie über die Map oder über die Liste)

![Connections](src/region.png)

Als nächstes werden Sie aufgefordert ein Kennwort zu vergeben, Bitte beachten Sie Ihr Kennwort muss mehr als acht Zeichen besitzen.

**Dieses Kennwort dient nur für das Webinterface und als Root Zugang zum OpenWRT-System (SSH) ihr Wlan Kennwort bleibt unberührt.**

![Connections](src/password.png)

Als nächstes schließen Sie mit "Finish" die Einrichtung ab.
## Das Webinterface

Unser Webinterface ist sehr einfach und intuitiv zu nutzen

Oben finden Sie die Applikationen . auf der linken Seite sehen Sie die Einstellungen. das mittlere Feld ist das Hauptfeld.

![Connections](src/main_ui.png)

Wenn Sie auf das `Internet` Symbol klicken, sehen Sie die momentane Einstellung wie der Router sich zum Internet verbindet, standard ist DHCP, dies erfordert ein Netzwerkkabel welches mit ihrem Heimnetz und den Gl.Inet Router verbunden ist.


![Connections](src/internet_status.png)

## Schalter und die LEDS

Sie können auf den Reset-Taster drücken um W-Lan an/auszuschalten

Die standard Funktion des Seitenschalters ist um die W-Lan Kennung sichtbar (rechte Seite) oder unsichtbar (linke Seite) zu schalten.

![Connections](src/buttons.png)

Die linke Grüne LED ist die Stromanzeige, sie leuchtet sobald der Router mit strom versorgt ist.

Die mittlere LED hat keine Funktion, diese können Sie frei zuweisen im OpenWRT Menü (Im Webinterface auf Advanced Settings schalten)

die rechte rote LED zeigt den W-Lan Status an, sie leuchtet konstant Rot wenn das Wlan aktiviert ist, und blinkt, wenn Netzwerkverkehr über das Interface stattfindet.

![Connections](src/leds.png)

## Wlan Einstellungen

Sie sollten die standard Kennung vom Wlan ändern und ein anderes Kennwort vergeben, so dass ihr Router niemand anders benutzen kann ausser Sie selbst.
