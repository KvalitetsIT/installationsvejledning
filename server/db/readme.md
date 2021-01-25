# VM specifikation
Maskinen har følgende diske:
- disk_1: 40G
  - root partition, mountpoint: /
- disk_2: 40G
  - data partition til database, mountpoint: /data

# Installer Ubuntu 20.04

## Vælg sprog
Vi vælger Engelsk som standard

[![](../../video/gif/language.gif)]

## Setup keyboard
Vi vælger Dansk som standard.

[![](../../video/gif/keyboard.gif)]

## Netværksinstillinger
Vi disabler netværk her, da vi manuelt sætter det op efter installationen.

[![](../../video/gif/network.gif)]

## Proxy
Vi benytter ikke en proxy for at få forbindelse til internettet.

[![](../../video/gif/proxy.gif)]

## Ubuntu mirror
Vi benytter standard mirror som foreslået.

[![](../../video/gif/mirror.gif)]

## Setup storage
Vi vælger først "*disk_1*", så boot-partitionen og bootloader installeres herpå når vi vælger automatisk opsætning af LVM for hele disken.
<br>
Først er vi nødt til at unmounte og slette root partitionen (/), for at kunne tilføje *disk_2* til den oprettede *LVM volume group* (ubuntu-vg).
<br>
Herefter kan vi oprette og tilføje data partitionen som *LVM logical volume* (db-lv), og til sidst oprettes root partitionen igen (ubuntu-lv).

[![](../../video/gif/disk_db-server.gif)]

## Setup profile
Konfigurering af default bruger, der har sudo rettigheder, og serverens hostname.

[![](../../video/gif/profile_db-server.gif)]

## SSH
Vi vil gerne have installeret SSH server.

[![](../../video/gif/ssh.gif)]

## Installation
Herefter kører installationsprocessen, og når den er færdig genstarter vi maskinen.

[![](../../video/gif/install_complete.gif)]