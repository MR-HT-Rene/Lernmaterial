# Selbstlernmaterial: Netzwerkadressierung für Einsteiger

## Einführung

Dieses Selbstlernmaterial ergänzt das Seminar "Grundlagen der Netzwerkadressierung" und bietet Ihnen die Möglichkeit, das Gelernte zu vertiefen und zu wiederholen.

### Wie Sie dieses Material nutzen sollten:
1. Wiederholen Sie die Grundkonzepte regelmäßig
2. Führen Sie die praktischen Übungen auf Ihrem eigenen Computer durch
3. Nutzen Sie die Selbsttests zur Wissensüberprüfung
4. Konsultieren Sie die weiterführenden Ressourcen für vertiefendes Lernen

## 1. Grundlegende Netzwerkkonzepte

### Was ist ein Netzwerk?
Ein Netzwerk ist eine Gruppe von miteinander verbundenen Computern und anderen Geräten, die Daten austauschen können. Netzwerke können klein sein (wie ein Heimnetzwerk mit wenigen Geräten) oder sehr groß (wie das Internet, das Milliarden von Geräten verbindet).

### Warum brauchen wir Adressierung?
- **Eindeutige Identifikation:** Jedes Gerät im Netzwerk muss eindeutig identifizierbar sein
- **Zustellung von Daten:** Der Absender muss wissen, wohin die Daten gesendet werden sollen
- **Routing:** Für den Transport von Daten über mehrere Netzwerke hinweg

### Das Grundprinzip der Kommunikation
So wie ein Brief sowohl einen Absender als auch einen Empfänger braucht, benötigt jede Netzwerkkommunikation:
- Eine Quelladresse (woher die Daten kommen)
- Eine Zieladresse (wohin die Daten gehen sollen)

## 2. Physische Adressierung: MAC-Adressen

### Was ist eine MAC-Adresse?
Die Media Access Control (MAC)-Adresse ist eine einzigartige Kennung, die fest mit der Netzwerkhardware (z.B. WLAN-Karte oder Ethernet-Adapter) eines Geräts verbunden ist.

### Eigenschaften:
- 48 Bit (6 Byte) lang
- Dargestellt in Hexadezimal, z.B.: `00:1A:2B:3C:4D:5E`
- Die ersten 3 Bytes (Organisationally Unique Identifier, OUI) identifizieren den Hersteller
- Die letzten 3 Bytes sind eine einzigartige Seriennummer für das Gerät

### Praktische Übung:
Ihre eigene MAC-Adresse finden:
1. Öffnen Sie die Kommandozeile (CMD) als Administrator
2. Geben Sie `ipconfig /all` ein und drücken Sie Enter
3. Suchen Sie nach "Physische Adresse" oder "Physical Address"
4. Notieren Sie sich diese Adresse und identifizieren Sie den Hersteller Ihrer Netzwerkkarte

### Grenzen von MAC-Adressen:
- Funktionieren nur im lokalen Netzwerk
- Nicht hierarchisch strukturiert
- Nicht für Routing über verschiedene Netzwerke geeignet

## 3. Logische Adressierung: IP-Adressen

### Was ist eine IP-Adresse?
Eine Internet Protocol (IP)-Adresse ist eine logische Adresse, die einem Gerät in einem Netzwerk zugewiesen wird. Im Gegensatz zur MAC-Adresse kann sie sich ändern und wird vom Netzwerk verwaltet.

### IPv4 vs. IPv6:
| IPv4 | IPv6 |
|------|------|
| 32 Bit (4 Bytes) | 128 Bit (16 Bytes) |
| Dargestellt in Dezimal mit Punkten | Dargestellt in Hexadezimal mit Doppelpunkten |
| Beispiel: 192.168.1.1 | Beispiel: 2001:0db8:85a3::8a2e:0370:7334 |
| Ca. 4,3 Milliarden Adressen | 340 Undezillion Adressen (3,4×10^38) |

### Praktische Übung:
Ihre eigene IP-Adresse finden:
1. Öffnen Sie die Kommandozeile (CMD)
2. Geben Sie `ipconfig` ein und drücken Sie Enter
3. Suchen Sie nach "IPv4-Adresse" und "IPv6-Adresse"
4. Besuchen Sie eine Website wie "whatismyip.com", um Ihre öffentliche IP-Adresse zu sehen

## 4. IPv4 im Detail

### Struktur einer IPv4-Adresse:
- 4 Oktette (Bytes), getrennt durch Punkte
- Jedes Oktett hat einen Wert zwischen 0 und 255
- Beispiel: 192.168.1.1

### Private vs. Öffentliche IP-Adressen:

#### Private IP-Bereiche:
- **Klasse A:** 10.0.0.0 bis 10.255.255.255
- **Klasse B:** 172.16.0.0 bis 172.31.255.255
- **Klasse C:** 192.168.0.0 bis 192.168.255.255

Diese Adressen sind für private Netzwerke reserviert und können nicht direkt über das Internet erreicht werden.

#### Öffentliche IP-Adressen:
Alle anderen IPv4-Adressen (außer spezielle Bereiche) sind öffentlich und im Internet eindeutig.

### Spezielle IPv4-Adressen:
- **127.0.0.1:** Loopback/Localhost (eigenes Gerät)
- **0.0.0.0:** Unspezifizierte Adresse
- **255.255.255.255:** Broadcast-Adresse
- **169.254.x.x:** APIPA (Automatic Private IP Addressing) - wird zugewiesen, wenn kein DHCP verfügbar ist

### Praktisches Beispiel:
Eine typische Heimnetzwerk-Konfiguration könnte so aussehen:
- Router: 192.168.1.1 (Gateway zum Internet)
- Computer 1: 192.168.1.2
- Computer 2: 192.168.1.3
- Smartphone: 192.168.1.4
- Öffentliche IP-Adresse (vom ISP zugewiesen): 203.0.113.42

## 5. IPv6-Grundlagen

### Warum IPv6?
IPv6 wurde entwickelt, um die Erschöpfung der IPv4-Adressen zu beheben und zusätzliche Verbesserungen einzuführen.

### Struktur einer IPv6-Adresse:
- 8 Blöcke zu je 16 Bit, getrennt durch Doppelpunkte
- Jeder Block wird in Hexadezimal dargestellt (0-9, A-F)
- Beispiel: 2001:0db8:85a3:0000:0000:8a2e:0370:7334

### Vereinfachte Schreibweise:
- Führende Nullen innerhalb eines Blocks können weggelassen werden
- Eine Folge von Null-Blöcken kann durch :: ersetzt werden (nur einmal pro Adresse)
- Beispiel: 2001:db8:85a3::8a2e:370:7334

### Praktische Übung:
1. Öffnen Sie die Kommandozeile (CMD)
2. Geben Sie `ipconfig /all` ein
3. Suchen Sie nach "IPv6-Adresse"
4. Falls keine vorhanden, ist IPv6 möglicherweise nicht konfiguriert

## 6. Subnetting und Subnetzmasken

### Was ist Subnetting?
Subnetting ist die Unterteilung eines IP-Netzwerks in mehrere kleinere Netzwerke (Subnetze).

### Warum Subnetting?
- Bessere Organisation großer Netzwerke
- Erhöhung der Sicherheit durch Isolation
- Effizientere Nutzung des Adressraums
- Reduzierung des Broadcast-Verkehrs

### Subnetzmasken verstehen:
- Eine Subnetzmaske definiert, welcher Teil einer IP-Adresse das Netzwerk und welcher den Host identifiziert
- Format ähnlich einer IP-Adresse: z.B. 255.255.255.0
- In Binär dargestellt ist sie eine Folge von 1en (Netzwerkteil) gefolgt von 0en (Hostteil)

### CIDR-Notation:
- Alternative Darstellung der Subnetzmaske
- Gibt die Anzahl der Netzwerk-Bits an
- Beispiele:
  - /24 entspricht 255.255.255.0
  - /16 entspricht 255.255.0.0
  - /8 entspricht 255.0.0.0

### Einfaches Beispiel:
- IP-Adresse: 192.168.1.50
- Subnetzmaske: 255.255.255.0 (/24)
- Netzwerk-ID: 192.168.1.0
- Broadcast-Adresse: 192.168.1.255
- Nutzbare Host-Adressen: 192.168.1.1 bis 192.168.1.254

## 7. Nützliche Netzwerkbefehle

### Windows-Befehle:
- **ipconfig:** Zeigt grundlegende IP-Konfiguration an
- **ipconfig /all:** Zeigt detaillierte Netzwerkinformationen (inkl. MAC-Adressen)
- **ping [Ziel]:** Testet die Verbindung zu einem Ziel
  - Beispiel: `ping google.com` oder `ping 8.8.8.8`
- **tracert [Ziel]:** Zeigt den Pfad zu einem Ziel
  - Beispiel: `tracert google.com`
- **nslookup [Domain]:** Zeigt DNS-Informationen an
  - Beispiel: `nslookup google.com`

### Linux/Mac-Befehle (falls relevant):
- **ifconfig / ip addr:** Zeigt Netzwerkkonfiguration an
- **ping [Ziel]:** Funktioniert wie in Windows
- **traceroute [Ziel]:** Äquivalent zu tracert in Windows
- **dig [Domain]:** Detaillierte DNS-Informationen

## 8. Selbsttest

### Grundlagen:
1. Was ist der Unterschied zwischen einer MAC-Adresse und einer IP-Adresse?
2. Warum reichen MAC-Adressen für das Internet nicht aus?

### IPv4:
3. Welche der folgenden IP-Adressen sind privat?
   - 192.168.0.1
   - 8.8.8.8
   - 10.0.0.1
   - 172.32.0.1

4. Was bedeutet es, wenn Ihr Computer eine IP-Adresse im Bereich 169.254.x.x hat?

### Subnetting:
5. Bei einer Subnetzmaske von 255.255.255.0, wie viele Hosts können in diesem Netzwerk maximal sein?

6. Was ist die Netzwerk-ID für einen Host mit der IP 192.168.10.25 und der Subnetzmaske 255.255.255.0?

### IPv6:
7. Welche der folgenden IPv6-Adressen ist korrekt gekürzt?
   - 2001:0db8:0000:0000:0000:ff00:0042:8329
   - 2001:db8::ff00:42:8329
   - 2001:db8:0:0:0:ff00::8329

## 9. Weiterführende Ressourcen

### Online-Kurse:
- Cisco Networking Academy: "Introduction to Networks"
- YouTube-Kanal "NetworkChuck" - Einsteigerfreundliche Netzwerktutorials
- Khan Academy: Grundlegende Internetkonzepte

### Bücher:
- "Netzwerke für Dummies" - Doug Lowe
- "TCP/IP-Grundlagen" - Eric Chou

### Praktische Tools:
- Wireshark: Netzwerkverkehr analysieren (für Fortgeschrittene)
- Angry IP Scanner: Netzwerk-Scanning
- Advanced IP Scanner: Geräte im Netzwerk finden

### Nützliche Websites:
- whatismyip.com - Zeigt Ihre öffentliche IP-Adresse an
- subnettingpractice.com - Übungen zum Subnetting
- ipv6-test.com - Testet Ihre IPv6-Konnektivität

## 10. Lösungen zum Selbsttest

### Grundlagen:
1. Eine MAC-Adresse ist eine physische, fest eingebrannte Hardware-Adresse, während eine IP-Adresse eine logische, zuweisbare Adresse ist. MAC-Adressen bleiben normalerweise konstant, IP-Adressen können sich ändern.

2. MAC-Adressen sind nicht hierarchisch strukturiert und können nicht geroutet werden. Das Internet benötigt ein hierarchisches Adresssystem für effizientes Routing zwischen verschiedenen Netzwerken.

### IPv4:
3. Private IP-Adressen: 192.168.0.1, 10.0.0.1
   Öffentliche IP-Adressen: 8.8.8.8, 172.32.0.1

4. Eine IP-Adresse im Bereich 169.254.x.x (APIPA) bedeutet, dass Ihr Computer keine IP-Adresse von einem DHCP-Server erhalten konnte und sich selbst eine zugewiesen hat. Dies deutet normalerweise auf ein Netzwerkproblem hin.

### Subnetting:
5. Mit einer Subnetzmaske von 255.255.255.0 (/24) können maximal 254 Hosts im Netzwerk sein (2^8-2, da die erste und letzte Adresse reserviert sind).

6. Die Netzwerk-ID für 192.168.10.25 mit Subnetzmaske 255.255.255.0 ist 192.168.10.0.

### IPv6:
7. Die korrekt gekürzte IPv6-Adresse ist: 2001:db8::ff00:42:8329