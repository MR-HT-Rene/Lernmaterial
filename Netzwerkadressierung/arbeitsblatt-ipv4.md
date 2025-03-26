# Arbeitsblatt: IPv4-Adressen verstehen

## Aufgabe 1: Private vs. Öffentliche IP-Adressen

Kreuzen Sie an, ob es sich um private (interne) oder öffentliche (externe) IP-Adressen handelt:

| IP-Adresse       | Privat | Öffentlich |
|------------------|--------|------------|
| 192.168.10.15    |        |            |
| 8.8.8.8          |        |            |
| 10.0.0.1         |        |            |
| 172.16.254.1     |        |            |
| 203.0.113.42     |        |            |
| 127.0.0.1        |        |            |
| 172.32.0.1       |        |            |
| 192.169.0.1      |        |            |

## Aufgabe 2: Besondere IP-Adressen

Beschreiben Sie kurz, wofür die folgenden speziellen IP-Adressen genutzt werden:

1. 127.0.0.1: ______________________________________________________

2. 0.0.0.0: _______________________________________________________

3. 255.255.255.255: _______________________________________________

4. 169.254.x.y: ___________________________________________________

## Aufgabe 3: IP-Adressen und Subnetzmasken

Bestimmen Sie für die folgenden IP-Adressen und Subnetzmasken:
- Die Netzwerk-ID
- Die Broadcast-Adresse
- Den Bereich der nutzbaren Host-Adressen (erste und letzte)

### Beispiel:
IP-Adresse: 192.168.1.50, Subnetzmaske: 255.255.255.0
- Netzwerk-ID: 192.168.1.0
- Broadcast: 192.168.1.255
- Nutzbare Hosts: 192.168.1.1 bis 192.168.1.254

### a) IP-Adresse: 10.0.0.25, Subnetzmaske: 255.0.0.0
- Netzwerk-ID: ___________________________________________________
- Broadcast: ____________________________________________________
- Nutzbare Hosts: _______________________________________________

### b) IP-Adresse: 172.16.5.10, Subnetzmaske: 255.255.0.0
- Netzwerk-ID: ___________________________________________________
- Broadcast: ____________________________________________________
- Nutzbare Hosts: _______________________________________________

## Aufgabe 4: CIDR-Notation

Geben Sie die äquivalente Subnetzmaske für folgende CIDR-Notationen an:

1. /24: _________________________________________________________

2. /16: _________________________________________________________

3. /8: __________________________________________________________

4. /28: _________________________________________________________

## Aufgabe 5: Praktische Anwendung

1. Sie sind für ein kleines Büronetzwerk verantwortlich. Welchen privaten IP-Bereich würden Sie verwenden und warum?

_________________________________________________________________
_________________________________________________________________
_________________________________________________________________

2. Nennen Sie zwei Möglichkeiten, wie Sie die IP-Adresse Ihres eigenen Computers herausfinden können:

_________________________________________________________________
_________________________________________________________________

-----

# Lösungen

## Aufgabe 1: Private vs. Öffentliche IP-Adressen

| IP-Adresse       | Privat | Öffentlich |
|------------------|--------|------------|
| 192.168.10.15    |   ✓    |            |
| 8.8.8.8          |        |     ✓      |
| 10.0.0.1         |   ✓    |            |
| 172.16.254.1     |   ✓    |            |
| 203.0.113.42     |        |     ✓      |
| 127.0.0.1        | Spezial (Loopback)  |
| 172.32.0.1       |        |     ✓      |
| 192.169.0.1      |        |     ✓      |

## Aufgabe 2: Besondere IP-Adressen

1. 127.0.0.1: Loopback-Adresse, verweist auf das eigene Gerät

2. 0.0.0.0: Standardroute/unspezifizierte Adresse

3. 255.255.255.255: Broadcast-Adresse für das lokale Netzwerk

4. 169.254.x.y: APIPA (Automatic Private IP Addressing), wird automatisch zugewiesen, wenn kein DHCP-Server verfügbar ist

## Aufgabe 3: IP-Adressen und Subnetzmasken

### a) IP-Adresse: 10.0.0.25, Subnetzmaske: 255.0.0.0
- Netzwerk-ID: 10.0.0.0
- Broadcast: 10.255.255.255
- Nutzbare Hosts: 10.0.0.1 bis 10.255.255.254

### b) IP-Adresse: 172.16.5.10, Subnetzmaske: 255.255.0.0
- Netzwerk-ID: 172.16.0.0
- Broadcast: 172.16.255.255
- Nutzbare Hosts: 172.16.0.1 bis 172.16.255.254

## Aufgabe 4: CIDR-Notation

1. /24: 255.255.255.0

2. /16: 255.255.0.0

3. /8: 255.0.0.0

4. /28: 255.255.255.240