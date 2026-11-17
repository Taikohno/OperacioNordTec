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
![Screenshot_20261013_094152.png](imatge-inicial-xarxa) 

Aquest model de xarxa permet ampliació facil afegint switches per abaix del primari per a cada area de la empresa

Hi ha un Firewall entre la xarxa y el router actuant com una DMZ per una seguretat mes avançada

**Com configurar un ordinador en la xarxa**

S'ha instalat un servei DHCP per la configuracio facil i en massa de les maquines clients

**Exemple en Linux**

sudo nano /etc/netplan/01-network-manager-all.yaml 

![Screenshot_20261013_095128.png](imatge-exemple-yaml)

## Configuracións de les maquines

**Firewall/Router**

```
network:
    ethernets:
        enp1s0:
            dhcp4: true
        enp2s0:
            dhcp4: true
      #kali
        enp3s0:
            addresses:
              - 10.0.0.1/24
      #dmz
        enp4s0:
            addresses:
              - 192.168.10.1/24
      #lan
        enp5s0:
            addresses:
              - 192.168.20.1/24
```
**Server Ubuntu**

```
network:
    ethernets:
        enp1s0:
            dhcp4: false
            addresses:
              - 192.168.10.10/24
            routes:
              - to: default
                via: 192.168.10.1
    version: 2
```

**Desktop Ubuntu**

```
network:
    version: 2
    renderer: NetworkManager
    ethernets:
        enp1s0:
            dhcp4: false
            addresses:
              - 192.168.20.10/24
            routes:
              - to: default
                via: 192.168.20.1
            nameservers:
              addresses:
               - 8.8.8.8
               - 1.1.1.1
```

