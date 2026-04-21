---
permalink: /bwi302/l06_case_pizza_solution_extended_slice_dash/
title: "BWI302 Prozessmanagement - Interaktiver Part"
author_profile: false
hide_pagination: true
share: false
redirect_from: 
  - /bwi302/l06_case_pizza_solution_extended_lice_dash.html
---

Eine mögliche optimierte Lösung mit Slice Dash Lösung können Sie anschauen, wenn Sie folgende Spezifikation unter [BPMN Sketch Miner](https://www.bpmn-sketch-miner.ai/index.html) einfügen.


## Prozess 1
```
Slice Dash:
Send Anfrage Verfügbare Produkte
Receive Verfügbare Produkte
(publish Verfügbare Produkte)

Restaurant:
(Receive Anfrage Verfügbare Produkte)
Send Verfügbare Produkte
```

## Prozess 2
```
Kunde:
(notify Verfügbare Produkte)
Send Bestellung
(notify Statusupdates)
Warten
(notify Pizza erhalten)
(receive Bezahlabwicklung)
Send Bezahlung

...
Warten
(deadline 90min)

Slice Dash:
(receive Bestellung)
Send Auftrag
(receive Pizza started)
(publish Statusupdate Pizza started)
(receive Pizza finished)
(publish Statusupdate Pizza finished)
Send Info Lieferung anfragen
(receive Pizza abgeholt)
(publish Statusupdate Pizza unterwegs)
(receive Pizza ausgeliefert)
Send Bezahlabwicklung
Receive Bezahlung
(publish Bezahlabwicklung abgeschlossen)

Restaurant:
(receive Auftrag)
Pizza backen
(send Pizza started)
(timer 20min)
(send Pizza finished)
(notify Bezahlabwicklung abgeschlossen)

Lieferant:
(receive Info Lieferung anfragen)
Lieferung vorbereiten
Lieferung abholen
(send Pizza abgeholt)
Lieferung ausliefern
(send Pizza ausgeliefert)
```

