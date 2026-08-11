# Herkunftsnachweis von Unlimitec AI

Hier liegt der öffentliche Teil eines Registers, das festhält, wann bei
Unlimitec AI Inhalte durch künstliche Intelligenz entstanden sind. Jeden Tag
wird der aktuelle Stand dieses Registers mit einem unabhängigen Zeitstempel
versehen, der sich später von jedem nachprüfen lässt — auch von uns nicht mehr
veränderbar.

**Was hier nicht steht:** keine Kundendaten, keine Texte, keine Fingerabdrücke
einzelner Inhalte, keine Geschäftszahlen. Aus einer Prüfsumme lässt sich nichts
zurückrechnen.

---

## Was Sie hier sehen

Zwei Ordner, einer je Register: `content` für Texte, `voice` für Sprachaufnahmen.

Darin liegt für jeden Tag ein **Paar aus zwei Dateien**, und beide werden
gebraucht:

| Datei | Beantwortet die Frage |
|---|---|
| `2026-08-10.txt` | **Was** wurde beglaubigt — der Stand des Registers an diesem Tag, im Klartext lesbar |
| `2026-08-10.txt.ots` | **Wann** hat es existiert — der Zeitnachweis, verankert in der Bitcoin-Blockchain |

Die `.ots`-Datei enthält den Inhalt selbst nicht, nur seinen Fingerabdruck. Ohne
die zugehörige `.txt` wäre sie ein Zeitstempel für etwas Unbekanntes. Deshalb
gehören beide zusammen.

---

## Einen Nachweis prüfen

Das Verfahren heißt **OpenTimestamps** und ist offen dokumentiert; die Software
stammt nicht von uns.

```
ots verify content/2026-08-10.txt.ots
```

Wurde an der `.txt` auch nur ein Zeichen verändert, passt der Nachweis nicht
mehr — die Prüfung schlägt fehl.

**Zwei Hinweise, damit die Prüfung nicht an einer Formalie scheitert:**

Der Zeitnachweis wird in zwei Stufen fertig. Unmittelbar nach dem Erstellen
bestätigt ihn zunächst ein Kalenderdienst; die endgültige Verankerung in der
Bitcoin-Blockchain folgt einige Stunden später und wird von uns automatisch
nachgetragen. Der Nachweis des laufenden Tages kann deshalb noch „nur"
kalenderbestätigt sein.

Für die vollständige Prüfung gegen die Blockchain greift `ots verify` auf einen
Bitcoin-Knoten zu. Wer keinen betreibt, sieht eine entsprechende Meldung. Der
Nachweis ist deswegen nicht ungültig — er lässt sich alternativ über einen
öffentlichen Block-Explorer nachvollziehen.

---

## Korrekturen

Was bei Prüfungen dieses Registers gefunden und behoben wurde, steht in
[PRUEFUNGEN.md](PRUEFUNGEN.md) — mit Datum und Themengebiet.

Ein Register, das nie eine Korrektur zeigt, wurde entweder nie geprüft oder
verschweigt sie.

---

## Mehr dazu

<https://www.unlimitecai.com/ki-transparenz>
