
## LAN IP Adresse

Ab und zu kann es vorkommen dass Sie die LAN Ip Adresse ihres Mini Routers ändern müssen (z.B Wennn ihr Heimnetz die selbe IP Adresse verwendet) die standard Ip lautet: `192.168.8.1`. 


Viele Router benutzen eine der folgenden Ip´s `192.168.0.1`, `192.168.1,1`, `192.168.1.254`, `10.10.1.1` etc. und als subnet `255.255.255.0` (`/24`). Es ist wichtig, dass sich die Ip Adresse ihres Mini-Routers und ihres Heimnetzes unterscheiden, wenn Ihr Heim-Router die Ip `192.168.8.x` besitzt, müssen Sie die Ip-Adresse vom Mini Router ändern.

Sie können die Ip-Adresse ihress Original Routers im Webinterface des Routers entnehmen, oder benutzen Sie unser Webinterface

im folgenden Beispiel ist die Ip Adresse vom Wan Port des Mini Routers `192.168.9.243` (angenommen die Subnet-Maske ist`/24`), daher können wir `192.168.8.1` als LAN Ip anwenden.

![Lan IP](src/lan_ip.png)
