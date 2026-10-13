# Operació Nord Tec
## Tagdh O'Hare Davis ASIX 1B
**Index**
* Estat del projecte
* Arquitectura de xarxa
* Configuracions
* Incidencies i solucions
* Decisions tècniques i reflexions
## Estat de projecte

* Fet

Arquitectura de xarxa

* Per fer

Configuracions

Incidencies i solucions

Deciosions tècniques i reflexions

## Arquitectura de xarxa

La Arquitectura inicial de la xarxa es la seguent:
![/home/tagdh/Pictures/Screenshot_20261013_094152]

Aquest model de xarxa permet ampliació facil afegint switches per abaix del primari per a cada area de la empresa

Hi ha un Firewall entre la xarxa y el router actuant com una DMZ per una seguretat mes avançada

**Com configurar un ordinador en la xarxa**

S'ha instalat un servei DHCP per la configuracio facil i en massa de les maquines clients

**Exemple en Linux**

sudo nano /etc/netplan/01-network-manager-all.yaml 

![/home/tagdh/Pictures/Screenshot_20261013_095128]
