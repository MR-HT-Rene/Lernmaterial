# Visuelle Elemente für das Seminar "Grundlagen der Netzwerkadressierung"

## Übersicht der benötigten Visualisierungen

Diese Visualisierungen sollten für die PowerPoint-Präsentation und die Handouts erstellt werden.

### 1. Grundlegende Konzepte

#### 1.1 Stadt ohne Adressen
**Beschreibung:** Eine Zeichnung einer einfachen Stadt, in der die Häuser keine Nummern oder Straßennamen haben.
**Text:** "Wie findet der Briefträger den richtigen Empfänger?"
**Einsatz:** Einstiegs-Analogie

#### 1.2 Einfaches Netzwerk
**Beschreibung:** Schematische Darstellung eines kleinen Netzwerks mit Router, Computer, Laptop, Smartphone und Drucker.
**Beschriftung:** Jedes Gerät mit Symbol und Namen kennzeichnen
**Einsatz:** Grundkonzept Netzwerk

#### 1.3 Hierarchie der Netzwerke
**Beschreibung:** Verschachtelte Kreise oder Blasen, die verschiedene Netzwerkebenen darstellen:
- Innerster Kreis: Lokales Netzwerk (LAN)
- Mittlerer Kreis: Unternehmens-/Campusnetzwerk (WAN)
- Äußerer Kreis: Internet
**Einsatz:** Netzwerkhierarchie erklären

### 2. Physische Adressierung

#### 2.1 MAC-Adresse Struktur
**Beschreibung:** Eine MAC-Adresse (z.B. 00:1A:2B:3C:4D:5E) mit farbiger Kennzeichnung:
- Erste 3 Bytes (00:1A:2B) in blau markiert und als "Hersteller-ID" beschriftet
- Letzte 3 Bytes (3C:4D:5E) in grün markiert und als "Geräte-ID" beschriftet
**Einsatz:** MAC-Adressaufbau erklären

#### 2.2 MAC-Kommunikation
**Beschreibung:** Darstellung von 3-4 Computern in einem lokalen Netzwerk mit ihren MAC-Adressen. Pfeile zeigen die Kommunikation zwischen den Geräten.
**Einsatz:** Lokale Kommunikation via MAC

#### 2.3 CMD-Screenshot: MAC-Adresse
**Beschreibung:** Screenshot der CMD-Ausgabe von `ipconfig /all` mit hervorgehobener MAC-Adresse ("Physische Adresse")
**Einsatz:** Praktische Demonstration

### 3. Logische Adressierung

#### 3.1 Postanalogie
**Beschreibung:** Illustration eines Briefs mit korrekter Adressierung:
- Name (Person) → MAC-Adresse
- Straße, Hausnummer → Host-ID
- Stadt, PLZ → Netzwerk-ID
- Land → Domain
**Einsatz:** Hierarchische Adressierung erklären

#### 3.2 MAC vs. IP Vergleichstabelle
**Beschreibung:** Einfache Tabelle mit Vergleich:

| Eigenschaft | MAC-Adresse | IP-Adresse |
|-------------|-------------|------------|
| Typ | Physisch | Logisch |
| Länge | 48 Bit | 32 Bit (IPv4) / 128 Bit (IPv6) |
| Format | Hexadezimal | Dezimal mit Punkten / Hexadezimal mit Doppelpunkten |
| Veränderbarkeit | Fest | Zuweisbar |
| Gültigkeitsbereich | Lokales Netzwerk | Weltweites Internet |
| Beispiel | 00:1A:2B:3C:4D:5E | 192.168.1.1 / 2001:db8::1428:57ab |

**Einsatz:** Unterschiede verdeutlichen

#### 3.3 Routing zwischen Netzwerken
**Beschreibung:** Illustration von zwei separaten Netzwerken, die über Router verbunden sind. Pfeile zeigen den Weg eines Datenpakets von einem Netzwerk zum anderen.
**Einsatz:** Notwendigkeit logischer Adressierung

### 4. IPv4-Adressierung

#### 4.1 IPv4-Adressstruktur
**Beschreibung:** Eine IPv4-Adresse (z.B. 192.168.1.100) mit farbiger Markierung der einzelnen Oktette. Darunter die binäre Darstellung.
**Einsatz:** IPv4-Struktur erklären

#### 4.2 Private vs. Öffentliche IP-Bereiche
**Beschreibung:** Grafische Darstellung der privaten IP-Bereiche als farbige Blöcke in einem Zahlenstrahlendiagramm von 0.0.0.0 bis 255.255.255.255:
- 10.0.0.0 - 10.255.255.255 (blau)
- 172.16.0.0 - 172.31.255.255 (grün)
- 192.168.0.0 - 192.168.255.255 (orange)
- Rest (öffentliche IPs) in grau
**Einsatz:** Private IP-Bereiche erklären

#### 4.3 NAT-Prinzip
**Beschreibung:** Schematische Darstellung eines Heimnetzwerks mit Router und mehreren Geräten (192.168.1.x) auf der einen Seite und dem Internet mit einer öffentlichen IP auf der anderen Seite.
**Einsatz:** Network Address Translation erklären

#### 4.4 Browser mit IP-Adresse
**Beschreibung:** Screenshot eines Browsers mit eingetippter IP-Adresse (z.B. 142.250.186.78) in der Adressleiste, der die Google-Startseite zeigt.
**Einsatz:** Praktische Demonstration

### 5. IPv6-Grundlagen

#### 5.1 IPv4 vs. IPv6 Adressraum
**Beschreibung:** Visuelle Größenvergleich-Darstellung:
- Kleine Box beschriftet mit "IPv4: 4,3 Milliarden Adressen"
- Daneben viel größere Box beschriftet mit "IPv6: 340 Undezillion Adressen"
**Einsatz:** Größenunterschied verdeutlichen

#### 5.2 IPv6-Adressstruktur
**Beschreibung:** Eine IPv6-Adresse (z.B. 2001:0db8:85a3:0000:0000:8a2e:0370:7334) mit farbiger Markierung der verschiedenen Teile:
- Globales Präfix
- Subnetz-ID
- Interface-ID
**Einsatz:** IPv6-Struktur erklären

#### 5.3 IPv6-Verkürzung
**Beschreibung:** Drei Beispiele der gleichen IPv6-Adresse:
1. Vollständig: 2001:0db8:0000:0000:0000:0000:0370:7334
2. Ohne führende Nullen: 2001:db8:0:0:0:0:370:7334
3. Vollständig gekürzt: 2001:db8::370:7334
**Einsatz:** IPv6-Kurzschreibweise erklären

### 6. Subnetting und Subnetzmasken

#### 6.1 Subnetzmaske Grafik
**Beschreibung:** Darstellung einer IP-Adresse (192.168.1.100) und einer Subnetzmaske (255.255.255.0) in binärer Form untereinander. Markierung, wie die Subnetzmaske die IP-Adresse in Netzwerk- und Host-Teil trennt.
**Einsatz:** Funktion der Subnetzmaske erklären

#### 6.2 Subnetzbeispiel
**Beschreibung:** Schematische Darstellung eines Netzwerks (192.168.1.0/24) mit mehreren Geräten:
- Router: 192.168.1.1
- Netzwerk-ID: 192.168.1.0
- Broadcast: 192.168.1.255
- Nutzbare Adressen: 192.168.1.2 - 192.168.1.254
**Einsatz:** Subnetz-Komponenten erklären

#### 6.3 CIDR-Notation Tabelle
**Beschreibung:** Einfache Tabelle mit äquivalenten Darstellungen:

| CIDR | Subnetzmaske | Anzahl Hosts |
|------|--------------|--------------|
| /8   | 255.0.0.0    | 16.777.214   |
| /16  | 255.255.0.0  | 65.534       |
| /24  | 255.255.255.0| 254          |
| /28  | 255.255.255.240 | 14        |

**Einsatz:** CIDR-Notation erklären

#### 6.4 Netzwerksegmentierung
**Beschreibung:** Darstellung eines Unternehmens mit verschiedenen Abteilungen als Subnetze:
- Verwaltung: 192.168.1.0/24
- Entwicklung: 192.168.2.0/24
- Produktion: 192.168.3.0/24
- Server: 192.168.10.0/24
**Einsatz:** Praktischen Nutzen von Subnetting zeigen

### 7. Zusammenfassung und Praxis

#### 7.1 Netzwerkdiagnose-Flussdiagramm
**Beschreibung:** Einfaches Flussdiagramm zur Netzwerkproblembehebung:
- Start: "Keine Internetverbindung"
- Verzweigungen für verschiedene Prüfschritte
- Lösungsansätze an den Endpunkten
**Einsatz:** Praktische Problemlösungsstrategien

#### 7.2 Befehlsübersicht
**Beschreibung:** Zusammenstellung der wichtigsten CMD-Befehle mit kurzen Erklärungen und Beispiel-Screenshots
**Einsatz:** Praxisreferenz

#### 7.3 IP-Checkliste
**Beschreibung:** Übersichtliche Liste mit den wichtigsten IP-bezogenen Informationen zum Nachschlagen
**Einsatz:** Schnellreferenz für Teilnehmer