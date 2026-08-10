# Unlimitec AI, Herkunftsnachweis

Hier veröffentliche ich täglich den Kopf meiner Herkunftsketten und lasse ihn
unabhängig zeitstempeln. Wer wissen will, ob ich Einträge nachträglich verändert
habe, kann das hier selbst nachrechnen, ohne mir glauben zu müssen.

Unlimitec AI erzeugt Texte mit künstlicher Intelligenz. Jeder erzeugte Inhalt
wird im Moment seiner Entstehung in einem Herkunftsregister erfasst, mit einem
digitalen Fingerabdruck und dem Zeitpunkt. Die Einträge sind fortlaufend
miteinander verkettet: Jeder Eintrag trägt die Prüfsumme seines Vorgängers.
Diese Verkettung hat einen Kopf, und genau der steht hier.

## Was hier NICHT steht

Das ist mir wichtiger als alles andere auf dieser Seite:

- **Keine Kundendaten.** Kein Name, keine Firma, keine Kennung.
- **Keine Texte.** Weder ganz noch in Auszügen.
- **Keine Fingerabdrücke einzelner Inhalte.** Niemand kann hier einen Text
  abgleichen oder herausfinden, was erzeugt wurde.
- **Keine Geschäftszahlen.** Auch nicht, wie viele Einträge es gibt.

In jeder Datei stehen vier Zeilen: welche Kette, welches Datum, der Kopf-Hash
und die Version des Verfahrens. Aus einem SHA-256-Wert lässt sich nichts
zurückrechnen.

## Die zwei Ketten

- `anker/content/` — erzeugte Texte
- `anker/voice/` — erzeugte Sprachaufnahmen

## Selbst prüfen

Zu jeder Ankerdatei liegt eine `.ots`-Datei. Das ist ein Zeitnachweis nach dem
offenen OpenTimestamps-Verfahren, verankert in der Bitcoin-Blockchain. Er belegt,
dass die Ankerdatei zu diesem Zeitpunkt bereits genau so existierte. Prüfen kann
das jeder, auch ohne mich:

```
pip install opentimestamps-client
ots verify anker/content/2026-08-10.txt.ots
```

Wird an der Ankerdatei auch nur ein Zeichen verändert, meldet die Prüfung
`File does not match original!`.

## Warum das nötig ist

Ein Register, das nur der Betreiber führt, beweist wenig: Wer alle Rechte an der
Datenbank hat, könnte es umschreiben. Genau diese Lücke schließt die
Veröffentlichung. Der Zeitstempel entsteht außerhalb meines Zugriffs, deshalb
lässt sich nachträgliches Umschreiben erkennen, auch bei mir selbst.

## Hintergrund

Unlimitec AI hat den EU-Verhaltenskodex zur Transparenz KI-generierter Inhalte
unterzeichnet (Abschnitt 1, Anbieter). Wie die Kennzeichnung insgesamt
funktioniert, steht auf <https://www.unlimitecai.com/ki-transparenz>.

Dieses Verzeichnis wird automatisch befüllt. Fragen dazu:
<https://www.unlimitecai.com/kontakt>
