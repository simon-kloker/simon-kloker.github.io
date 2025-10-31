---
permalink: /bwi302/l06_case_pizza/
title: "BWI302 Prozessmanagement - Interaktiver Part"
author_profile: false
hide_pagination: true
share: false
redirect_from: 
  - /bwi302/l06_case_pizza.html
---

Modellieren Sie folgenden Prozess in BPMN 2.0.

### 1. Bestellung aufgeben:
Der Kunde ruft das Pizzarestaurant an oder bestellt online. Die Bestellung wird als Nachrichtenereignis (Nachricht vom Kunden) ausgelöst.

### 2. Bestellung bestätigen:
Das Restaurant bestätigt die Bestellung per Nachricht (z. B. SMS oder E-Mail) an den Kunden.

### 3. Zutaten prüfen:
Das Restaurant prüft, ob alle Zutaten verfügbar sind:
- Falls Zutaten fehlen, wird der Kunde informiert und die Bestellung storniert (Zeitereignis: 5 Minuten Wartezeit, bevor Stornierung erfolgt).
- Falls Zutaten verfügbar sind, geht es weiter zur Zubereitung.

### 4. Pizza zubereiten:
Die Pizza wird zubereitet. Dies dauert 20 Minuten (angeheftetes Zeitereignis).

### 5. Lieferung vorbereiten:
Der Lieferfahrer wird informiert und macht sich auf den Weg.

### 6. Pizza ausliefern:
Die Pizza wird beim Kunden angeliefert. Der Kunde bestätigt den Erhalt per Nachricht (Nachrichtenereignis).

### 7. Prozessende:
Der Prozess ist abgeschlossen.


