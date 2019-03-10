# Was wird gebraucht

Grundaufgabe:

Konzeption einer Netzwerk und Serverstruktur einer Fakultät und Aufbau via Ansible Playbooks

weietere Details:

Verbindung zur Hochschule über Dark Fiber
eigene Dienste wie Web-Auftritt, Mail, evtl Code-Hosting-Dienst

weitere Anforderungen:

alle Instanzen sollen über snmp durch incinga, zabbix oder ganglia überwacht werden können

## Aufteilung in einzelne Konzepte

### Bau-Konzept

nicht notwendig bei diesem Projekt

### Konzept des Netzwerkes an sich und der In-House Kommunikation

### VoIP-Konzeption

### Internet-Anbindung und Anbindung an die restliche Universität

Über Dark Fiber (eigentlich tote, aber gmietete Leitung)

### Management-Konzept

- Ansible-Playbooks
- Überwachung über snmp durch incinga, zabbix oder ganglia

### Sicherheitskonzept

- Server für Website, Mail und Code-Hoster stehen in der DMZ
- Die Anbindung der Clients erfolgt über ein anderes Netz als die Anbindung der Daten-Server oder Ähnlichem
- mehrere Firewlls, je nach "Sicherheitsstufe"
