# Übung 5

Erstelle `SVG`-Grafiken für Media Player Controls.

## Anweisung

Erstelle `SVG`-Grafiken von Hand. In der nächsten Stunde soll ein Videoplayer mit selbst erstellten Navigationselementen entstehen. Die Bedienelemente sollten Start und Pause, eventuell auch Stop enthalten, sowie Grafiken für Skip, bzw. Fast Forward. Sie sollen als `SVG`-Grafiken umgesetzt werden und am besten den bekannten Formen entsprechen:

![Video-Bedienelemente](https://user-images.githubusercontent.com/1279725/73025089-3e6df500-3e2f-11ea-8b60-761e8c4e5892.png)

Die Grafiken sollen in dieser Aufgabe auf quadratischen Grundflächen der Maße 100×100 Pixel aufgebaut werden.

```html
<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
</svg>
```

Die fertigen Dateien sollen in ein HTML-Dokument eingebunden werden, vorzugsweise in einem `<nav>` Element und einer Liste `<ul>`.

Das geht entweder über ein `<img>`-Element, oder indem man den `SVG`-Code direkt ins HTML an die entsprechende Stelle einfügt. (Beides hat Vor- und Nachteile.)

Auf diese Weise lässt sich das Dokument später leicht um das benötigte Video-Element erweitern.

Gib den `SVG`-Elementen sinnvolle Klassennamen, um sie später mit `CSS` leichter gestalten zu können. In der Regel empfiehlt sich hier, eine Klasse für die Füllfarbe des Hintergrunds, eine für die Linienfarbe und eine mit dem Fill der Linienfarbe vorzusehen.

**Bonusaufgabe:**

- Eventuell macht es je nach deinem gewählter Form Sinn, sich das [`<path>`](https://developer.mozilla.org/de/docs/Web/SVG/Tutorial/Pfade) Element mit seinen Beziertools oder das [`<use>`](https://developer.mozilla.org/en-US/docs/Web/SVG/Element/use) Element etwas genauer anzuschauen. Damit lassen sich Kurven bzw. sich wiederholende Elemente umsetzen.


## Dauer und Abgabe

Die veranschlagte Bearbeitungszeit für diese Aufgabe beträgt 7 Tage, bis zur nächsten Kursstunde.  
Die Abgabe dieser Aufgabe ist nicht vorgesehen und dient lediglich deiner eigenen Übung.

## Referenzen und weiterführende Links

### Bücher

- [Practical SVG](https://abookapart.com/products/practical-svg) (A Book Apart, englisch)

### MDN

- [SVG Tutorial](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial) (englisch)
- [Pfade](https://developer.mozilla.org/de/docs/Web/SVG/Tutorial/Pfade)
- [`<use>`](https://developer.mozilla.org/en-US/docs/Web/SVG/Element/use) (englisch)

### Path Editor

- [Cubic Bézier Curve Example](http://blogs.sitepointstatic.com/examples/tech/svg-curves/cubic-curve.html)
- [jxnblk.github.io/paths](https://jxnblk.github.io/paths/)
- [editor.method.ac](https://editor.method.ac)

### Verschiedene

- [SVG](https://de.wikipedia.org/wiki/Scalable_Vector_Graphics) (Wikipedia)
- [An in-depth SVG tutorial](https://flaviocopes.com/svg/) (englisch)
- [A Primer on Bézier Curves](https://pomax.github.io/bezierinfo/) (englisch)
- [SVG Path Visualizer](https://svg-path-visualizer.netlify.app/) (english)
- [The Bezier Game](https://bezier.method.ac)
- [An illustrated guide to the `path` syntax](https://css-tricks.com/svg-path-syntax-illustrated-guide/)
- [StackOverflow: Is the `xmlns` parameter needed?](https://stackoverflow.com/a/34249810/3625228)
- [Using Javascript with SVG](https://www.petercollingridge.co.uk/tutorials/svg/interactive/javascript/) (SVG -> Javascript interface options)
