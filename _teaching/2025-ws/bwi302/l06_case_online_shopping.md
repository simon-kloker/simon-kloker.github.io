---
permalink: /bwi302/l06_case_online_shopping/
title: "BWI302 Prozessmanagement - Interaktiver Part"
author_profile: false
hide_pagination: true
share: false
redirect_from: 
  - /bwi302/l06_case_online_shopping.html
---

Modellieren Sie folgenden Prozess in BPMN 2.0.

### 1. Start
Kunde löst Bestellvorgang aus (z. B. durch Klick auf „Jetzt kaufen“).

### 2. Benutzeraufgabe
Kunde füllt Bestellformular aus (Name, Adresse, Zahlungsmethode).

### 3. Serviceaufgabe
System prüft Lagerbestand und reserviert das Produkt.

### 4. Transaktion (inkl. Kompensation)
Transaktionsstart: Zahlungsabwicklung (z. B. Kreditkartenbelastung).

- Erfolgspfad: Zahlung erfolgreich → Bestellung wird bestätigt.
- Fehlerpfad: Zahlung fehlgeschlagen → Kompensation: Reservierung wird storniert, Kunde erhält Fehlermeldung.

### 5. Terminierung
Ereignis: Bestellung wird nach 14 Tagen automatisch abgeschlossen, wenn keine Rückgabe erfolgt.

### 6. Ereignis-Teilprozess

Ereignis: Kunde löst Rückgabe aus (z. B. durch Klick auf „Rückgabe starten“).

Ablauf:
- Kunde füllt Rückgabeformular aus (User Task).
- System generiert Rücksendeetikett (Service Task).
- Nach Erhalt der Ware wird die Zahlung rückerstattet (Service Task).

