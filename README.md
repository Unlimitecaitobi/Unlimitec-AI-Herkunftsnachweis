# Herkunftsnachweis von Unlimitec AI

Jeder Inhalt, der bei Unlimitec AI entsteht, wird in einem Herkunftsregister
erfasst. Hier veröffentliche ich täglich den Stand dieses Registers und lasse ihn
unabhängig mit einem Zeitstempel versehen. So lässt sich nachrechnen, dass später
nichts daran verändert wurde. Auch nicht von mir.

**Was hier nicht steht:** keine Kundendaten, keine Texte, keine Fingerabdrücke
einzelner Inhalte und keine Geschäftszahlen. Jede Datei enthält vier Zeilen, und
aus einer Prüfsumme lässt sich nichts zurückrechnen.

`anker/content` steht für erzeugte Texte, `anker/voice` für erzeugte
Sprachaufnahmen.

## Selbst prüfen

Zu jeder Datei gehört ein Zeitnachweis nach dem offenen OpenTimestamps-Verfahren:

```
pip install opentimestamps-client
ots verify anker/content/2026-08-10.txt.ots
```

Wurde an der Datei ein Zeichen verändert, passt der Nachweis nicht mehr.

## Mehr dazu

<https://www.unlimitecai.com/ki-transparenz>
