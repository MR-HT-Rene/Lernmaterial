# Präsentationsstruktur: Grundlagen der Netzwerkadressierung

## Übersicht der PowerPoint-Folien

### Einführung (Folien 1-5)

1. **Titelfolie**
   - Titel: "Grundlagen der Netzwerkadressierung"
   - Untertitel: "Ein Seminar für Quereinsteiger"
   - Name des Dozenten
   - Datum

2. **Agenda**
   - Zeitplan mit Modulen und Pausen
   - Hinweis auf interaktive Elemente und praktische Übungen

3. **Lernziele**
   - Auflistung der 5 Hauptlernziele des Seminars

4. **Die Adress-Analogie**
   - Grafik: Stadt ohne Adressen vs. Stadt mit Adressen
   - Kernpunkte der Analogie als Bullet Points

5. **Grundkonzept: Was ist ein Netzwerk?**
   - Einfache Grafik eines Netzwerks (Computer, Router, Internet)
   - Definition: "Ein Netzwerk ist..."
   - Warum wir Adressierung brauchen

### Physische Adressierung (Folien 6-11)

6. **Was ist eine MAC-Adresse?**
   - Definition und Zweck
   - Beispiel-MAC-Adresse mit farbiger Markierung
   - Bild einer Netzwerkkarte mit Hinweis auf eingebrannte Adresse

7. **Aufbau einer MAC-Adresse**
   - Grafik: 6 Bytes, aufgeteilt in Hersteller-ID und Geräte-ID
   - Beispiele verschiedener Hersteller-IDs (z.B. Apple, Intel)

8. **Wie MAC-Adressen funktionieren**
   - Grafik: Lokale Kommunikation zwischen Geräten
   - ARP-Prozess vereinfacht dargestellt
   - Broadcast vs. gezielte Kommunikation

9. **MAC-Adressen in der Praxis**
   - Screenshot: ipconfig /all Ausgabe mit hervorgehobener MAC-Adresse
   - Wo Sie die MAC-Adresse finden können
   - Anwendungsfälle (WLAN-Filter, etc.)

10. **Grenzen der MAC-Adressierung**
    - Grafik: Zwei getrennte Netzwerke
    - Problem: MAC-Adressen funktionieren nur im lokalen Netzwerk
    - Überleitung zur logischen Adressierung

11. **Praktische Übung: MAC-Adresse finden**
    - Schritt-für-Schritt Anleitung für CMD
    - Alternative Methoden (Netzwerkeinstellungen, etc.)

### Logische Adressierung (Folien 12-17)

12. **Von der MAC zur IP**
    - Grafik: Briefpost-Analogie (Name vs. Adresse)
    - Warum wir mehr als MAC-Adressen brauchen
    - Hierarchisches Adressierungssystem

13. **Was ist eine IP-Adresse?**
    - Definition und Zweck
    - Unterschied zwischen IPv4 und IPv6 (kurz)
    - Eigenschaften: veränderbar, hierarchisch, routbar

14. **Internet vs. Intranet**
    - Grafik: Netzwerke im Netzwerk
    - Öffentliche vs. private Adressräume
    - Router als Vermittler

15. **Analogie: Postsystem**
    - Bildliche Darstellung: Straße→Stadt→Land→Kontinent
    - Parallele zu Netzwerk→Subnetz→Domain→Internet
    - Hierarchische Struktur verdeutlichen

16. **Vergleich: MAC vs. IP**
    - Vergleichstabelle: Physische vs. logische Adressierung
    - Einsatzbereiche beider Adresstypen
    - Zusammenspiel im Netzwerk

17. **Zwischenfazit & Überleitung**
    - Zusammenfassung der bisherigen Konzepte
    - Überleitung zu IPv4 im Detail

### IPv4-Adressierung (Folien 18-27)

18. **IPv4-Grundlagen**
    - Format: 32 Bit, vier Oktette
    - Notation: Dezimal mit Punkten (192.168.1.1)
    - Mögliche Werte: 0-255 pro Oktett

19. **IPv4-Adresse verstehen**
    - Grafische Darstellung einer IP-Adresse mit farbiger Markierung
    - Netzwerk- und Host-Anteil
    - Binäre Grundlagen (sehr vereinfacht)

20. **Klassen von IP-Adressen**
    - Übersicht der Klassen A, B, C (vereinfacht)
    - Typische Einsatzbereiche
    - Hinweis: heute meist classless (CIDR)

21. **Private IP-Bereiche**
    - Tabelle der privaten Bereiche
    - Grafik: Router verbindet privates mit öffentlichem Netz
    - NAT (Network Address Translation) vereinfacht erklärt

22. **Besondere IPv4-Adressen**
    - Loopback: 127.0.0.1
    - APIPA: 169.254.x.x
    - Broadcast: 255.255.255.255
    - Anwendungsfälle und Bedeutung

23. **IP-Adresszuweisung: DHCP**
    - Grafik: DHCP-Prozess vereinfacht
    - Dynamische vs. statische Adresszuweisung
    - Typische DHCP-Server im Alltag (Router)

24. **Praktische Demo: Browser & IP**
    - Screenshot: Eingabe einer IP-Adresse im Browser
    - Bekannte Webseiten und ihre IPs
    - DNS als Übersetzer (Vorschau)

25. **Probleme mit IPv4**
    - Adressknappheit visualisiert
    - Lösungsansätze (NAT, private Netze)
    - Überleitung zu IPv6

26. **Praxistipps: IP-Adressen im Alltag**
    - Wann Sie Ihre IP-Adresse kennen sollten
    - Häufige IP-bezogene Probleme und Lösungen
    - Tools zur IP-Diagnose

27. **Übung & Zusammenfassung**
    - Kurze Wiederholung der Hauptpunkte
    - Überleitung zur Pause oder IPv6

### IPv6-Grundlagen (Folien 28-32)

28. **Warum IPv6?**
    - Grafik: IPv4-Adresserschöpfung
    - Vorteile von IPv6 (größerer Adressraum, vereinfachte Konfiguration)
    - Einführungsstatus weltweit

29. **IPv6-Adressen verstehen**
    - Format: 128 Bit, acht Blöcke
    - Notation: Hexadezimal mit Doppelpunkten
    - Beispiel mit Erklärung der Teile

30. **IPv6-Kurzschreibweise**
    - Regeln zur Verkürzung (führende Nullen, Doppeldoppelpunkt)
    - Beispiele vor und nach der Kürzung
    - Übungsbeispiel

31. **IPv4 vs. IPv6**
    - Vergleichstabelle der wichtigsten Unterschiede
    - Koexistenz beider Standards
    - Was bedeutet das für Anwender?

32. **Praktisches IPv6**
    - Screenshot: IPv6-Adresse am eigenen PC
    - Übergangsszenarien (Dual-Stack, Tunneling)
    - Alltagsrelevanz für normale Anwender

### Subnetting und Subnetzmasken (Folien 33-40)

33. **Was ist Subnetting?**
    - Definition und Zweck
    - Analogie: Postleitzahlen in einer Stadt
    - Vorteile der Unterteilung (Organisation, Sicherheit, Effizienz)

34. **Subnetzmasken verstehen**
    - Grafik: IP-Adresse und Subnetzmaske
    - Funktion: Trennung von Netzwerk- und Host-Anteil
    - Beispiel: 255.255.255.0

35. **Subnetzmasken in der Praxis**
    - Typische Subnetzmasken und ihre Verwendung
    - 255.0.0.0 (/8), 255.255.0.0 (/16), 255.255.255.0 (/24)
    - Einfache Anwendungsbeispiele

36. **CIDR-Notation**
    - Erklärung der Schrägstrich-Notation (/24)
    - Umrechnung zwischen Dezimal und CIDR
    - Beispiele: 192.168.1.0/24 = 192.168.1.0 mit 255.255.255.0

37. **Netzwerkadresse und Broadcast**
    - Bedeutung der Netzwerkadresse (erste IP im Subnetz)
    - Bedeutung der Broadcast-Adresse (letzte IP im Subnetz)
    - Nutzbare Adressen dazwischen

38. **Einfaches Subnetting-Beispiel**
    - Schritt-für-Schritt Berechnung eines Subnetzes
    - Grafische Darstellung des Adressbereichs
    - Praxisbeispiel: Heimnetzwerk

39. **Subnetting im Alltag**
    - WLAN-Konfiguration im Router
    - VLANs in Unternehmen (vereinfacht)
    - Wann Sie mit Subnetting in Berührung kommen

40. **Übung: Subnetze erkennen**
    - Interaktives Beispiel
    - Aufgaben für die Breakout-Räume
    - Lösungsansätze

### Abschluss (Folien 41-45)

41. **Zusammenfassung: Adressierungskonzepte**
    - Physische Adressierung (MAC)
    - Logische Adressierung (IP)
    - Subnetting als Organisationsprinzip

42. **Praktische Tipps**
    - Die wichtigsten Befehle im Überblick
    - Netzwerkprobleme diagnostizieren
    - Ressourcen zum Selbststudium

43. **Häufige Fragen**
    - Antworten auf typische Netzwerkfragen
    - Weiterführende Themen im Überblick
    - Wo Sie mehr erfahren können

44. **Nächste Schritte**
    - Anwendungsmöglichkeiten des Gelernten
    - Verwandte Themen für weitere Schulungen
    - Praktische Übungsmöglichkeiten

45. **Abschluss & Feedback**
    - Dank für die Teilnahme
    - QR-Code zur Feedback-Umfrage
    - Kontaktinformationen für Rückfragen