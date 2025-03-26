# Grundlagen der Netzwerkadressierung
## Handout für Teilnehmer

### 1. Wichtige Begriffe im Überblick

| Begriff | Erklärung |
|---------|-----------|
| **Netzwerk** | Verbund von Computern und anderen Geräten, die miteinander kommunizieren können |
| **MAC-Adresse** | Physische Adresse eines Netzwerkgeräts (z.B. 00:1A:2B:3C:4D:5E) |
| **IP-Adresse** | Logische Adresse eines Geräts im Netzwerk (z.B. 192.168.1.100) |
| **IPv4** | Internet Protocol Version 4 mit 32-Bit-Adressen (z.B. 192.168.0.1) |
| **IPv6** | Internet Protocol Version 6 mit 128-Bit-Adressen (z.B. 2001:0db8::1428:57ab) |
| **Subnetzmaske** | Definiert, welcher Teil einer IP-Adresse das Netzwerk und welcher den Host identifiziert |
| **DHCP** | Dynamic Host Configuration Protocol - vergibt automatisch IP-Adressen im Netzwerk |
| **Router** | Gerät, das verschiedene Netzwerke miteinander verbindet |
| **Gateway** | Eintrittspunkt in ein anderes Netzwerk (typischerweise der Router) |
| **DNS** | Domain Name System - übersetzt Domainnamen (z.B. google.com) in IP-Adressen |

### 2. Physische vs. Logische Adressierung

#### MAC-Adresse (Physical)
- Fest in der Netzwerkkarte eingebrannt (kann in Software überschrieben werden)
- 48 Bit (6 Bytes) lang, dargestellt in Hexadezimal
- Format: 00:1A:2B:3C:4D:5E
- Erste 3 Bytes: Hersteller-ID
- Letzte 3 Bytes: Eindeutige Gerätenummer

#### IP-Adresse (Logical)
- Wird dem Gerät im Netzwerk zugewiesen
- Kann sich ändern (dynamische IP)
- Hierarchisch aufgebaut (Netzwerkteil + Hostteil)
- Ermöglicht Routing zwischen verschiedenen Netzwerken

### 3. IPv4-Adressierung

#### Struktur
- 32 Bit (4 Bytes)
- Darstellung in Dezimal mit Punkten: 192.168.1.1
- Jede Zahl kann zwischen 0 und 255 liegen

#### Private IP-Bereiche
- 10.0.0.0 - 10.255.255.255 (10.0.0.0/8)
- 172.16.0.0 - 172.31.255.255 (172.16.0.0/12)
- 192.168.0.0 - 192.168.255.255 (192.168.0.0/16)

#### Spezielle IPv4-Adressen
- 127.0.0.1: Loopback/Localhost (eigenes Gerät)
- 169.254.x.x: APIPA (Automatic Private IP Addressing)
- 255.255.255.255: Broadcast (Nachricht an alle Geräte im lokalen Netzwerk)

### 4. IPv6-Grundlagen

#### Struktur
- 128 Bit (16 Bytes)
- Darstellung in Hexadezimal mit Doppelpunkten: 2001:0db8:85a3:0000:0000:8a2e:0370:7334
- Verkürzte Notation: Aufeinanderfolgende Nullen können durch :: ersetzt werden (nur einmal pro Adresse)
- Beispiel: 2001:0db8:85a3::8a2e:0370:7334

#### Vorteile
- Größerer Adressraum (2^128 Adressen)
- Verbesserte Sicherheit
- Vereinfachte Konfiguration
- Bessere Routing-Effizienz

### 5. Subnetting Grundlagen

#### Subnetzmaske
- Definiert, welcher Teil der IP-Adresse das Netzwerk und welcher den Host identifiziert
- Darstellung als IP-Adresse: 255.255.255.0
- Alternative CIDR-Notation: /24 (Anzahl der Netzwerk-Bits)

#### Standard-Subnetzmasken
- Klasse A: 255.0.0.0 (/8)
- Klasse B: 255.255.0.0 (/16)
- Klasse C: 255.255.255.0 (/24)

#### Beispiel-Subnetting
- IP-Adresse: 192.168.1.50
- Subnetzmaske: 255.255.255.0 (/24)
- Netzwerk-ID: 192.168.1.0
- Broadcast-Adresse: 192.168.1.255
- Verfügbare Hosts: 192.168.1.1 bis 192.168.1.254

### 6. Nützliche Befehle für die Netzwerkdiagnose

| Befehl | Funktion | Beispiel |
|--------|----------|----------|
| `ipconfig` | Zeigt Netzwerkeinstellungen an | `ipconfig` |
| `ipconfig /all` | Zeigt detaillierte Netzwerkinformationen an | `ipconfig /all` |
| `ping` | Prüft die Erreichbarkeit eines Hosts | `ping google.com` |
| `tracert` | Zeigt den Pfad zu einem Ziel | `tracert google.com` |
| `nslookup` | Zeigt DNS-Informationen an | `nslookup google.com` |

### 7. Checkliste bei Netzwerkproblemen

1. **Lokale Verbindung prüfen**
   - Sind alle Kabel angeschlossen?
   - Funktioniert WLAN/LAN?
   - Leuchten die Statusanzeigen am Router/Switch?

2. **IP-Konfiguration prüfen**
   - Mit `ipconfig` prüfen, ob eine gültige IP-Adresse zugewiesen wurde
   - Bei 169.254.x.x: DHCP-Problem (Automatic Private IP Addressing)

3. **Verbindung zum lokalen Netzwerk testen**
   - Router/Gateway anpingen (z.B. `ping 192.168.1.1`)
   - Anderen Computer im Netzwerk anpingen

4. **Internetverbindung testen**
   - Bekannte IP-Adresse anpingen (z.B. `ping 8.8.8.8` - Google DNS)
   - Domain anpingen (z.B. `ping google.com`)

5. **DNS-Probleme identifizieren**
   - Wenn IP-Ping funktioniert, aber Domain-Ping nicht: DNS-Problem
   - DNS-Server prüfen (`ipconfig /all`)
   - Alternative DNS-Server verwenden (z.B. 8.8.8.8, 8.8.4.4)

6. **Routing-Probleme untersuchen**
   - `tracert google.com` ausführen
   - Wo bricht die Verbindung ab?

7. **Bei anhaltenden Problemen**
   - Router neu starten
   - Netzwerkadapter deaktivieren und wieder aktivieren
   - DHCP-Lease erneuern (`ipconfig /release` gefolgt von `ipconfig /renew`)
   - Support kontaktieren