# Übung 1 (Javascript)

Berechne die verbleibenden Tage bis Weihnachten

## Anweisung

Erstelle eine `HTML`-Seite, auf der die verbleibenden Tage bis Weihnachten berechnet werden. Du benötigst ein Element, in dem das Resultat ausgegeben wird, zB. ein `<p>` mit einer `id`. Dein Javascript soll ausgeführt werden, nachdem der Browser die `HTML`-Inhalte bereits gerendert hat. Daher steht das `<script>`-Element zu aller letzt im `<body>`.

Die Berechnung ist nicht kompliziert. Man braucht das Datum heute und das Datum von Weihnachten. Die Daten zieht man voneinander ab und zeigt die Differenz in Tagen an.

Um die Berechnung von Monaten und Tagen zu vereinfachen, benutzt man häufig den [UNIX-Timestamp](https://de.wikipedia.org/wiki/Unixzeit), eine Zeitrepräsentation in Sekunden seit 1. Januar 1970. Mit diesen ganzzahligen Werten lässt sich die Differenz leicht kalkulieren.

Das Datum von heute als UNIX-Timestamp:
```javascript
let heute = new Date().getTime();
```

Das Datum von Weihnachten:
```javascript
let heute = new Date(2019, 11, 24).getTime();
```

Weil es sich um Millisekundenwerte handelt, muss man zunächst durch `1000` teilen (ergibt Sekunden), danach durch `60` (ergibt Minuten), nochmal durch `60` (ergibt Stunden), zuletzt durch `24` (ergibt Tage).

Hat man den Wert berechnet, muss man ihn noch sichtbar auf der Seite platzieren, als Inhalt des dafür vorgesehenen `<p>`-Elements, das wir zu Beginn platziert haben.
```javascript
document.querySelector('p#deine-id').innerHTML = ergebnisWert;
```

**Bonusaufgabe:**

- Man kann evtl. eine Bedingung vorsehen, dass auch Tage nach Weihnachten ein korrektes Ergebnis ausgeben. (siehe Javascript [`if`](https://developer.mozilla.org/de/docs/Web/JavaScript/Reference/Statements/if...else))
- Man kann die generierten Datumsangaben so umformulieren, dass sie für jedes Jahr funktionieren, nicht nur 2019. Mit [`Date().getFullYear()`](https://developer.mozilla.org/de/docs/Web/JavaScript/Reference/Global_Objects/Date/getFullYear) lässt sich das aktuelle Jahr herausfinden.
- Im Idealfall passt Du die Gestaltung der Seite noch etwas mit `CSS` an, dass ersichtlich ist, was das Ergebnis ist und wofür die Seite überhaupt da ist.

## Dauer und Abgabe

Die veranschlagte Bearbeitungszeit für diese Aufgabe beträgt 7 Tage, bis zur nächsten Kursstunde.  
Die Abgabe dieser Aufgabe ist nicht vorgesehen und dient lediglich deiner eigenen Übung.

## Referenzen und weiterführende Links

### MDN

- [Date()](https://developer.mozilla.org/de/docs/Web/JavaScript/Reference/Global_Objects/Date)
- [Date.getTime()](https://developer.mozilla.org/de/docs/Web/JavaScript/Reference/Global_Objects/Date/getTime)
- [document.querySelector()](https://developer.mozilla.org/de/docs/Web/API/Document/querySelector)
- [Element.innerHTML](https://developer.mozilla.org/de/docs/Web/API/Element/innerHTML)