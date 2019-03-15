# Beleg im Modul NSM für INM

## Details

Semester: WS 2018/2019

Bearbeiter: Tom Wegener

## Aufgabe

Grundaufgabe:

Konzeption einer Netzwerk und Serverstruktur einer Fakultät und Aufbau via Ansible Playbooks

weitere Details:

Verbindung zur Hochschule über Dark Fiber
eigene Dienste wie Web-Auftritt, Mail, evtl Code-Hosting-Dienst

weitere Anforderungen:

alle Instanzen sollen über snmp durch incinga, zabbix oder ganglia überwacht werden können

## Konzept

### Router

- r1 - Kernrouter
- r2 - Dark-Fiber-Router (tap-Interface)
- r3 - DMZ-Router
- r4 - Server-side Router (DBs usw)
- r5 - Client-Netzwerk-Router

### Sektion: DMZ

- S1
- S2
- S3

### Sektion: Server-Netzwerk

### Sektion Client-Netzwerk

## TODOs

(ohne Reihenfolge)

- [] Konzeption des Netzwerkes
- [] Lernen von Ansible
- [] Implementation
- [] Dokumentation

## Cheat-sheet

### Fix routing

to reach the vms from your host:
`sudo route add -net 10.0.0.0/16 gw 193.168.233.2 dev nk_tap_luca`

### Ansible

#### CMD

Select host-file: `-i ./hosts`

Ping the host local: `ansible -i ./hosts  local -u root  -m ping`

run command as root `ansible -i ./hosts  local -u root  -m`

#### Playbooks

run Playbook: `ansible-playbook playbook.yml -i ./hosts -u root`


### NK-Machines

- vstart: starts a new virtual machine
- vlist: lists currently running virtual machines
- vlist: lists currently running virtual machines
- vconfig: attaches network interfaces to running vms
- vhalt: gracefully halts a virtual machine
- vcrash: causes a virtual machine to crash
- vclean: “panic command” to clean up all netkit

### NK-Labs

- lstart: starts a netkit lab
- lhalt: gracefully halts all vms of a lab
- lcrash: causes all the vms of a lab to crash
- lclean: removes temporary files from a lab directory
- linfo: provides information about a lab without starting it
- ltest: allows to run tests to check that the lab is working properly