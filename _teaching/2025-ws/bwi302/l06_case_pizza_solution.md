---
permalink: /bwi302/l06_case_pizza_solution/
title: "BWI302 Prozessmanagement - Interaktiver Part"
author_profile: false
hide_pagination: true
share: false
redirect_from: 
  - /bwi302/l06_case_pizza_solution.html
---

Eine mögliche Lösung können Sie anschauen, wenn Sie folgende Spezifikation unter (https://www.bpmn-sketch-miner.ai/index.html)[BPMN Sketch Miner] einfügen.

```
Kunde:
Send Bestellung
(receive Bestellung bestätigen)
(Receive Storno Info)

Restaurant:
(receive Bestellung)
Send Bestellung bestätigen
Zutaten vorhanden?
Zutaten nicht vorhanden
Send Storno Info
(timer 5min)
Bestellung storieren

...
Zutaten vorhanden?
Zutaten voranden
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
(receive Bestellung bestätigen)
(receive Lieferung angekommen)
Send Erhalt Info
```

