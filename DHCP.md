# Cheatsheet DHCP
- DHCP = Dynamic Host Configuration Protocol <br>
- DHCP Alway uses UDP Broadcasts <br>
- DHCP Server Port = 67<br>
- DHCP Client Port = 68<br>

---
## DORA
DHCP Discover (D): <br>
- Client:68 -> Server:67
- 0.0.0.0 -> Server:255.255.255.255

DHCP Offer (O): <br>
- Server:67 -> Client:68
- DHCP Server schickt packet mit folgendem Inhalt zurück:
  - MAC Adresse des Clients
  - mögliche IP-Adresse
  - IP Leasetime
  - Subnetzmaske
  - IP-Adresse des DHCP Servers
  - Default DNS Adress
  - Default Gateway

DHCP Request (R): <br>
- Client:68 -> Server:67
- Client wählt sich eine offärte (von evtl mehreren DHCP Servern) aus und schickt an dem eine Positive Meldung

DHCP Acknowledge (A): <br>
- Server:67 -> Client:68
- DHCP Server Antwortet mit einer Bestätigung
- Zusätzlich können noch ein paar weitere Daten angehängt werden.
  - MAC Adresse des Clients
	- IP-Adresse
	- IP Leasetime
	- Subnetzmaske
	- IP-Adresse des DHCP Servers
	- Default DNS Adress
	- Default Gateway
  - Broadcast Adresse

---
## APIPA
- APIPA = Automatic Private IP Addressing
- APIPA IP Range = 169.254.0.0/16
- Erlaubt es Windows Geräten auf einem Netzwerk ohne DHCP Server zu kommunizieren.
- Ein PC geht in den "APIPA Modus" wen er keine Antwort auf seinen DHCP Request bekommt.
---
