# Übung 6

Erzeuge eine Slideshow in HTML, CSS und Javascript


## Anweisung

Eine Slideshow soll eine Reihe von Abbildungen auf kleinem Raum betrachtbar machen. Dabei wird stets nur ein Bild angezeigt. Die anderen werden entweder automatisch durchlaufen, von Hand weiter und zurück navigiert, oder per Pagination direkt aktiviert.

Grundsätzlich funktionieren Slideshows (oder Carousels) meist so, dass die Bilder in HTML und CSS eingebunden und gestaltet werden und anschliessend alle bis auf das erste verborgen werden, zB. mit `display: none`, `opacity: 0` oder ähnlichen Eigenschaften.

Die Bedienung erfolgt meist über Javascript. Die derzeit aktive Abbildung wird entweder über einen Timer [`setInterval()`](https://developer.mozilla.org/de/docs/Web/API/WindowTimers/setInterval) oder Mausklicks/Taps [`addEventListener()`](https://developer.mozilla.org/de/docs/Web/API/EventTarget/addEventListener) festgelegt. Das heisst, man benötigt oft Navigationselemente wie Buttons für „Weiter“ oder „Zurück“ oder eine Möglichkeit, Bilder direkt anzusteuern mit Links für „1“, „2“, „3“, etc.

Bei Klick oder Timeout werden dann zunächst alle (oder nur die derzeit sichtbare?) Folie/Bild ausgeblendet, und das nächste (oder gewünschte) eingeblendet. Wenn man sauber arbeiten möchte, sollte man das umsetzen, indem die jeweiligen Elemente CSS-Klassen hinzugefügt oder entfernt bekommen, siehe [`classList.add()`](https://developer.mozilla.org/de/docs/Web/API/Element/classList) und [`classList.remove()`](https://developer.mozilla.org/de/docs/Web/API/Element/classList)

```javascript
let slideIndex = 1;
let targetElement = document.querySelector('#slide-' + slideIndex);

targetElement.classList.add('sichtbar');
```

**Bonusaufgabe:**

- Die Übergänge zwischen den einzelnen Folien lassen sich auch animieren. Dafür kann man entweder Javascript verwenden, oder etwas moderner Arbeiten und CSS Transitions einsetzen. Damit lassen sich Übergänge von zB. `opacity: 0.0` zu `opacity: 1.0` sanft animieren.

## Dauer und Abgabe

Die veranschlagte Bearbeitungszeit für diese Aufgabe beträgt 7 Tage, bis zur nächsten Kursstunde.  
Die Abgabe dieser Aufgabe ist nicht vorgesehen und dient lediglich deiner eigenen Übung.

## Referenzen und weiterführende Links

### Elemente

- [Simple Slideshow with Flexbox](http://mediatemple.net/blog/tips/carousels-dont-have-to-be-complicated/) (englisch)

#### MDN

- [addEventListener()](https://developer.mozilla.org/de/docs/Web/API/EventTarget/addEventListener)
- [classList](https://developer.mozilla.org/de/docs/Web/API/Element/classList)
- [setInterval()](https://developer.mozilla.org/de/docs/Web/API/WindowTimers/setInterval)
- [setTimeout()](https://developer.mozilla.org/de/docs/Web/API/WindowTimers/setTimeout)
- [Array.forEach()](https://developer.mozilla.org/en-US/docs/Web/API/NodeList/forEach)
- [CSS Transitions](https://developer.mozilla.org/de/docs/Web/CSS/transition)
