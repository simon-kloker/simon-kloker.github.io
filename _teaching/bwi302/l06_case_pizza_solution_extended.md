---
permalink: /bwi302/l06_case_pizza_solution_extended/
title: "BWI302 Prozessmanagement - Interaktiver Part"
author_profile: false
hide_pagination: true
share: false
redirect_from: 
  - /bwi302/l06_case_pizza_solution_extended.html
---

Eine optimierte Lösung können Sie anschauen, wenn Sie folgende Spezifikation unter [BPMN Sketch Miner](https://www.bpmn-sketch-miner.ai/index.html) einfügen.

```
Kunde:
Send Bestellung
(receive Bestellung bestätigen)
Warten
(Receive Storno Info)

...
Warten
(deadline 90min)

Restaurant:
(receive Bestellung)
Zutaten prüfen
(exception Nicht vorhanden)
Send Storno Info
(timer 5min)
Bestellung storieren

...
Zutaten prüfen
Send Bestellung bestätigen
Pizza backen
(timer 20min)
Send Info Lieferung anfragen
(receive Erhalt Info)

Lieferant:
(receive Info Lieferung anfragen)
Lieferung vorbereiten
Lieferung ausliefern
(send Lieferung angekommen)

...
Kunde:
Warten
Receive Lieferung angekommen
Send Erhalt Info
```

