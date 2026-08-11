# Herkunftsnachweis von Unlimitec AI™

Wenn eine KI für Sie schreibt, sollten Sie belegen können, wann das geschah.

Hier liegt der öffentliche Teil meines Registers. Es hält fest, wann bei
Unlimitec AI Inhalte durch künstliche Intelligenz entstanden sind. Der Stand dieses Registers
wird täglich mit einem unabhängigen Zeitstempel versehen. Ist er einmal in der
Bitcoin-Blockchain verankert, kann ihn auch ich nicht mehr verändern.

Das gilt für den Zeitnachweis selbst: Die `.ots`-Datei hängt an der Blockchain,
nicht an dieser Seite. Wer sie einmal heruntergeladen hat, kann sie prüfen,
unabhängig davon, was hier später steht.

Die Reihe beginnt am 10.08.2026 und ist im Aufbau. Wie weit sie trägt, sehen Sie
an den vorhandenen Dateien, nicht an dieser Beschreibung.

**Was hier nicht steht:** keine Kundendaten, keine Texte, keine Fingerabdrücke
einzelner Inhalte, keine Geschäftszahlen. Aus einer Prüfsumme lässt sich nichts
zurückrechnen.

## Was Sie hier sehen

Zwei Ordner, einer je Register. `content` für Texte, `voice` für Sprachaufnahmen.

Die Ordner heißen genau so, in Kleinbuchstaben. Zeigt Ihr Browser stattdessen
"Inhalt" und "Stimme" an, übersetzt er die Seite automatisch. Für die Prüfung
zählen die echten Namen, also `content` und `voice`.

Darin liegt für jeden Tag ein Paar aus zwei Dateien. Beide werden gebraucht:

| Datei | Beantwortet die Frage |
|---|---|
| `2026-08-10.txt` | **Was** wurde beglaubigt. Der Stand des Registers an diesem Tag, im Klartext lesbar |
| `2026-08-10.txt.ots` | **Wann** hat es existiert. Der Zeitnachweis, verankert in der Bitcoin-Blockchain |

Die `.ots`-Datei enthält den Inhalt selbst nicht, nur seinen Fingerabdruck. Ohne
die zugehörige `.txt` wäre sie ein Zeitstempel für etwas Unbekanntes. Deshalb
gehören beide zusammen.

## Einen Nachweis prüfen

Das Verfahren heißt OpenTimestamps. Es ist offen dokumentiert, und die Software
stammt nicht von mir.

```
ots verify content/2026-08-10.txt.ots
```

Wurde an der `.txt` auch nur ein Zeichen verändert, passt der Nachweis nicht
mehr und die Prüfung schlägt fehl.

Zwei Hinweise, damit die Prüfung nicht an einer Formalie scheitert:

Der Zeitnachweis wird in zwei Stufen fertig. Direkt nach dem Erstellen bestätigt
ihn ein Kalenderdienst. Die endgültige Verankerung in der Bitcoin-Blockchain
folgt einige Stunden später und wird automatisch nachgetragen. Der Nachweis des
laufenden Tages kann deshalb noch allein kalenderbestätigt sein.

Für die vollständige Prüfung gegen die Blockchain greift `ots verify` auf einen
Bitcoin-Knoten zu. Wer keinen betreibt, sieht eine entsprechende Meldung. Der
Nachweis ist deswegen **nicht ungültig**. Er lässt sich ohne Knoten in drei
Schritten nachvollziehen:

```
ots info content/2026-08-10.txt.ots
```

Die Ausgabe nennt für jede Bestätigung die Blocknummer und den zugehörigen
Merkle-Root, zum Beispiel:

```
verify BitcoinBlockHeaderAttestation(961896)
# Bitcoin block merkle root 9383179a8ad7467cf2cbb0e6e57aa3a3d798c3d7914e02aa578132aaed5c93ed
```

Diese Blocknummer in einem beliebigen Block-Explorer aufrufen und den dort
angezeigten Merkle-Root mit dem obigen vergleichen. Stimmen beide überein, ist
belegt: Die Datei existierte, bevor dieser Block entstand.

Der Nachweis vom 10.08.2026 trägt drei solcher Bestätigungen aus
unterschiedlichen Blöcken.

## Warum ich das mache

Ich habe den Verhaltenskodex der Europäischen Kommission zur Transparenz
KI-erzeugter Inhalte unterzeichnet, in der ersten Runde der Unterzeichner. Die
Liste ist öffentlich einsehbar:

<https://digital-strategy.ec.europa.eu/en/news/strong-backing-code-practice-transparency-ai-generated-content>

Eine Unterschrift ist eine Absichtserklärung. Dieses Register ist der Teil, der
sich nachprüfen lässt.

## Korrekturen

Was bei Prüfungen dieses Registers gefunden und behoben wurde, steht in
[PRUEFUNGEN.md](PRUEFUNGEN.md), mit Datum und Themengebiet.

Ein Register, das nie eine Korrektur zeigt, wurde entweder nie geprüft oder
verschweigt sie.

## Mehr dazu

<https://www.unlimitecai.com/ki-transparenz>
