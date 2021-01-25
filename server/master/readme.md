# VM specifikation
Maskinen har følgende diske:
- disk_1: 40G
  - root partition, mountpoint: /

# Hent Ubuntu server
[https://ubuntu.com/download/server](https://ubuntu.com/download/server)
<br>
Vælg “Option 2 - Manual server installation” og “Download Ubuntu Server 20.04.1 LTS”

[![](../../video/gif/download.gif)]

## Upload fil til VMware
[https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-492D6904-7471-4D66-9555-9466CCCA6931.html](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-492D6904-7471-4D66-9555-9466CCCA6931.html
)

# Installer Ubuntu 20.04
Allerede installeret? Hop til [Konfigurer Ubuntu 20.04](#Konfigurer-Ubuntu-20.04)
<br>
Hvis ikke gennemgår vi installationsprocessen her.

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


# Konfigurer Ubuntu 20.04
Vi skal manuelt have konfigureret:
* netværk
* koblet maskinen på et AD domæne

## Netværk
Ubuntu 20.04 bruger *netplan* til netværkskonfiguration. Konfigurationsfilen er placeret i '/etc/netplan', og man kan finde eksempler på forskellige konfigurationer [på netplans hjemmeside](https://netplan.io/examples/)

Vi konfigurerer her i eksemplet en statisk IP på interface 'enp0s3'

[![](../../video/gif/config_network.gif)]