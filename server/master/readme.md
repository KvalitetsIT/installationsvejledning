# VM specifikation
Maskinen har følgende diske:
- disk_1: 40G
  - root partition, mountpoint: /

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
Vi har kun en enkelt disk i master serveren, så vi benytter automatisk opsætning af LVM for hele disken.
Vi skal blot lige ændre størrelsen, så hele disken bruges.

[![](../../video/gif/disk_master.gif)]

## Setup profile
Konfigurering af default bruger, der har sudo rettigheder, og serverens hostname.

[![](../../video/gif/profile_master.gif)]

## SSH
Vi vil gerne have installeret SSH server

[![](../../video/gif/ssh.gif)]

## Installation
Herefter kører installationsprocessen, og når den er færdig genstarter vi maskinen.

[![](../../video/gif/install_complete.gif)]