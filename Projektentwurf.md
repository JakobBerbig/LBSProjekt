# Projektentwurf

#### Projektteam:

- Jakob Berbig
- Christof Nessler

Projektentwurf per Teams an Volgger gesendet (Jakob, 23.9.)

# Projektentwurf vom 23.09.2026:

- Auf Proxmox Virtualiserte umgebung mit Windows und Linux Servern + Clients
    - Monitoring mit Wazuh SIEM
    - PXE, Software Deployment und Management mit OPSI
    - Domain Controller und DNS mit SAMBA
    - Firewall
    - VPN (für gesicherten Zugriff von Außerhalb des Schulnetzwerks)

## Server und Hardware

Virtualisierung von Servern und Clients auf Server 1 mit Proxmox.
Backups per PBS (Proxmox Backup Server) auf Server 2.

#### Firewall

Als Firewall möchten wir einen Physische Firewall verwenden.
Sollte uns keine zur Verfügung stehen, wird eine Software Firewall verwendet werden.

#### Switches

- 

## Verwendete Software und Dienste

#### SIEM

- Als SIEM (Security Monitoring and Event Management) wird Wazuh verwendet.
    - Wazuh ist Open Source und benötigt keine Lizenzen.
    - Der Wazuh Agent könnte mit OPSI Paketiert und auf den Clients installiert werden.
    - https://documentation.wazuh.com/current/installation-guide/index.html

#### Softwareverteilung und PXE

- OPSI wird zur Softwareverteilung sowie als PXE Server eingesetzt
    - https://opsi.org/en/
    - https://docs.opsi.org/opsi-docs-de/4.3/index.html

#### Domain Controller, DNS und DHCP

- Als Domain Controller und DNS wird Samba 4 verwendet werden
    - https://www.samba.org/samba/
    - https://wiki.ubuntuusers.de/Archiv/Howto/Samba4-Server_als_Active-Directory_Domain-Controller/
    - https://wiki.samba.org
- Als DHCP wird ISC Kea DHCP verwendet werden.
    - ISC Kea DHCP
