# Übung 3 (Javascript)

Erzeuge eine zufällige Grafik aus Buchstaben

![Zufällige Buchstaben](https://user-images.githubusercontent.com/1279725/73022641-44ada280-3e2a-11ea-9aaf-d2bd915bb000.png)

## Anweisung

Erstelle ein `Array` mit verschiedenen Begriffen. Bei jedem Aufruf der Seite soll ein zufälliger Begriff aus dem `Array` gewählt werden. Der gewählte Begriff wird über eine Schleife in einzelne Buchstaben zerlegt. Die jeweiligen Buchstaben werden als neu erzeugte Elemente, zB. `<p>` ins [DOM](https://developer.mozilla.org/de/docs/Gecko-DOM-Referenz/Einf%C3%BChrung) eingefügt, am Besten mit zufälligen Positionen, oder in zufälliger Reihenfolge.

Du benötigst ein Containerelement für die Buchstaben, zB. `<div>`. Ausserdem [`Math.random()`](https://developer.mozilla.org/de/docs/Web/JavaScript/Reference/Global_Objects/Math/math.random), eine [`for()`](https://developer.mozilla.org/de/docs/Web/JavaScript/Reference/Statements/for)-Schleife, [`document.createElement()`](https://developer.mozilla.org/de/docs/Web/API/Document/createElement) und die Funktion [`appendChild()`](https://developer.mozilla.org/de/docs/Web/API/Node/appendChild). Über die Eigenschaften [`.innerHTML`](https://developer.mozilla.org/de/docs/Web/API/Element/innerHTML) oder [`.textContent`](https://developer.mozilla.org/de/docs/Web/API/Node/textContent) lässt sich der Wert eines DOM-Nodes setzen.

Idealerweise erzeugst du den Ablauf direkt in einer Funktion, die sich mehrfach aufrufen lässt. Dann kann man das Containerelement leeren und zur Laufzeit der Seite einen neuen Begriff generieren.

**Bonusaufgabe:**

- Füge ein Eingabefeld hinzu, in dem die seitenbesuchende Person den Begriff eingeben kann, wenn sie ihn erraten hat. Dazu benötigt man die Eigenschaft `.value` des [`<input>`](https://developer.mozilla.org/de/docs/Web/HTML/Element/input)-Felds, sowie einen "Absenden"-Button mit einem Event-Listener, der per 
  ```javascript
  let testElement = document.querySelector("#mein-element");
  testElement.addEventListener("click", function(event) {
      console.log("Klick!");
  });
   ```
  hinzugefügt werden kann
- Gestalte die Seite ansprechend mit CSS. Achte dabei auf unterschiedliche Bildschirmgrößen ([media queries]()!) und setze die Positionen der Buchstaben im Container als prozentuale Werte. Bestenfalls ist auch die Schriftgröße selbst responsive, oder zumindest angepasst auf ein paar Größen.

## Dauer und Abgabe

Die veranschlagte Bearbeitungszeit für diese Aufgabe beträgt 7 Tage, bis zur nächsten Kursstunde.  
Die Abgabe dieser Aufgabe ist nicht vorgesehen und dient lediglich deiner eigenen Übung.

## Referenzen und weiterführende Links

### MDN

- [.addEventListener()](https://developer.mozilla.org/de/docs/Web/API/EventTarget/addEventListener)
- [Media Queries](https://developer.mozilla.org/de/docs/Web/CSS/Media_Queries/Using_media_queries) (englisch)
- [Schleifen in Javascript, "Loops"](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code) (englisch)
- [Document Object Model, "DOM"](https://developer.mozilla.org/de/docs/Gecko-DOM-Referenz/Einf%C3%BChrung)

### StackOverflow

- [innerHTML, innerTextm, textContent, nodeValue](https://stackoverflow.com/questions/21311299/nodevalue-vs-innerhtml-and-textcontent-how-to-choose)
