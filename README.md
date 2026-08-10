# Herkunftsnachweis von Unlimitec AI

Wenn eine KI Texte für ein Unternehmen schreibt, sollte sich später nachvollziehen
lassen, woher sie stammen. Genau dafür ist dieses Verzeichnis da.

Bei Unlimitec AI wird jeder erzeugte Inhalt im Moment seiner Entstehung in einem
Herkunftsregister erfasst, mit einem digitalen Fingerabdruck und dem Zeitpunkt.
Die Einträge sind fortlaufend miteinander verbunden: Jeder trägt die Prüfsumme
seines Vorgängers, so wie Glieder einer Kette. Am Ende dieser Kette steht ein
einzelner Wert, der von allem davor abhängt. Diesen Wert veröffentliche ich hier
täglich und lasse ihn unabhängig mit einem Zeitstempel versehen.

Der Sinn dahinter ist einfach. Das Register liegt in meiner Datenbank, und wer
darauf vollen Zugriff hat, könnte es nachträglich verändern. Auch ich. Ein
veröffentlichter und extern datierter Wert schließt diese Lücke, denn er entsteht
außerhalb meines Zugriffs. Sie müssen mir also nicht glauben, Sie können es
nachrechnen.

## Was hier nicht steht

Das ist mir genauso wichtig wie der Nachweis selbst. In diesen Dateien finden
sich keine Kundendaten, keine Namen, keine Firmen. Es stehen dort auch keine
Texte, weder vollständig noch in Auszügen, und keine Fingerabdrücke einzelner
Inhalte. Niemand kann hier nachsehen, was für wen erzeugt wurde. Und es stehen
keine Geschäftszahlen darin, auch nicht, wie viele Einträge das Register führt.

Jede Datei enthält vier Zeilen: um welche Kette es geht, das Datum, den Wert am
Ende der Kette und die Version des Verfahrens. Aus einer solchen Prüfsumme lässt
sich nichts zurückrechnen.

## Die beiden Ketten

Unter `anker/content` liegen die Nachweise für erzeugte Texte, unter `anker/voice`
die für erzeugte Sprachaufnahmen.

## Wie Sie das selbst prüfen können

Zu jeder Ankerdatei gehört eine Datei mit der Endung `.ots`. Das ist ein
Zeitnachweis nach dem offenen OpenTimestamps-Verfahren, verankert in der
Bitcoin-Blockchain. Er belegt, dass die Ankerdatei zu diesem Zeitpunkt bereits
genau so vorlag. Prüfen kann das jeder, auch ohne mich:

```
pip install opentimestamps-client
ots verify anker/content/2026-08-10.txt.ots
```

Wurde an der Ankerdatei auch nur ein einziges Zeichen verändert, meldet die
Prüfung, dass die Datei nicht mehr zum Nachweis passt.

## Woher das kommt

Unlimitec AI hat den europäischen Verhaltenskodex zur Transparenz KI-generierter
Inhalte unterzeichnet, Abschnitt 1 für Anbieter. Wie die Kennzeichnung insgesamt
funktioniert und was Unternehmen selbst beachten müssen, habe ich auf meiner
Website beschrieben:

- <https://www.unlimitecai.com/ki-transparenz>
- <https://www.unlimitecai.com/ki-verordnung>

Dieses Verzeichnis wird automatisch befüllt. Wenn Sie Fragen dazu haben, erreichen
Sie mich über <https://www.unlimitecai.com/kontakt>.
