# Übung 2 (Javascript)

Programmiere einen einfachen Spielautomaten

## Anweisung

Erstelle eine `HTML`-Seite, auf der der Besucher mit einem Klick einen Spiel- automaten starten kann. Der Automat soll, angelehnt an einen Einarmigen Banditen, aus drei Zahlenreihen je einen Wert zufällig auswählen. Stimmen die drei Werte überein, gewinnt der Spieler.

Du benötigst drei Elemente, in denen das Resultat ausgegeben wird, zB. ein `<ul>`, das drei `<li>` mit einzigartigen `id`-Attributen beinhaltet.

Die drei Wertepools der Maschine simulieren wir mit drei Arrays, die zB. so aussehen können:
```javascript
const slot1 = [1,2,3,4,5,6,7,8,9];
```

Mit einer Funktion lässt sich der Aufruf eines zufälligen Wertes aus einem der Arrays automatisieren:
```javascript
let getSlot = function (slotNumber) {
    const currentSlot = window["slot" + slotNumber];
    const output = currentSlot[Math.floor(Math.random() * currentSlot.length)];
    return output;
};
```

Der Aufruf, zB. für Slot 2, sieht dann so aus:
```javascript
let slot2Value = getSlot(2);
```

Der Vergleich der drei Zufallswerte ist dann einfach:
```javascript
if (slot1Value == slot2Value && slot2Value == slot3Value) {
    console.log("Gewonnen!");
} else {
    console.log("Leider nicht gewonnen.");
}
```

Idealerweise hat man den kompletten Spielverlauf in einer einzigen Funktion, zB. `runMachine()`, dann ist es einfach, diese auf Knopfdruck auszuführen:
```javascript
document.querySelector('a#button-id').addEventListener("click", function (event) {
    event.preventDefault();
    runMachine();
});
```

Um dem Spieler Feedback zu geben, sollte man die drei Zufallswerte auf der Seite ausgeben, am besten in der vorbereiteten Liste. Das geht genau wie in [Übung 1](../../uebung_01b.md):
```javascript
document.querySelector('li#deine-id').innerHTML = slot1Value;
```

**Bonusaufgabe:**

- Finde einen Weg, Bilder statt Zahlen für die Werte anzuzeigen
- Modifiziere den Automaten so, dass je ein Klick nötig ist, um die nächste Zufallszahl auszulosen. Das vermittelt dem Spieler den Eindruck, er könnte das Geschehen beeinflussen und macht das Spiel interaktiver.

## Dauer und Abgabe

Die veranschlagte Bearbeitungszeit für diese Aufgabe beträgt 7 Tage, bis zur nächsten Kursstunde.  
Die Abgabe dieser Aufgabe ist nicht vorgesehen und dient lediglich deiner eigenen Übung.

## Referenzen und weiterführende Links

### Bücher

- [Javascript for Web Designers](https://abookapart.com/products/javascript-for-web-designers) (A Book Apart, englisch)

### MDN

- [Array](https://developer.mozilla.org/de/docs/Web/JavaScript/Reference/Global_Objects/Array)
- [function()](https://developer.mozilla.org/de/docs/Glossary/Function) (englisch)
- [if/else](https://developer.mozilla.org/de/docs/Web/JavaScript/Reference/Statements/if...else)
- [addEventListener()](https://developer.mozilla.org/de/docs/Web/API/EventTarget/addEventListener)