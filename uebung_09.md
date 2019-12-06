# Übung 9

Entwickle ein Online-Adventure-Game


## Beschreibung

Entwickle ein Online-Adventure(?)-Game, auf Basis von `Javascript` und `HTML`/`CSS`. Die Komplexität ist nicht vorgeschrieben. Es kann sich um eine bildlastige Umsetzung im Stil von Myst handeln, oder um ein klassisches Textadventure, was im Prinzip Interactive Fiction ist, also eine Erzählung, bei der der Leser die Handlung beinflussen kann. Alle Freiheiten sind gegeben. 

Die Aufgabe soll im Idealfall die im Kurs vermittelten Inhalte widerspiegeln.

### Konzept

- Sitemap bzw. Flowdiagramm mit den benötigten Templates/Einzeldesigns
- Wireframes für die verschiedenen Templates
- Entwickle ein Navigationskonzept und -design für dein Spiel
- Entwicklung eines Erscheinungsbildes

### Umsetzung

- `HTML`-Grundgerüst, `<meta>`-Tags, externe `CSS` und `Javascript`-Dateien
- Arbeit vom Allgemeinen ins Detail
- Wenn möglich responsive im Bereich `~400px` bis `1400px`

Wenn du möchtest, nutze [Git](https://git-scm.com/) (siehe auch PDF der entsprechenden Stunde) und/oder [Github](https://github.com/), um dein Projekt in Einzelschritten zeitlich nachvollziehbar zu machen und dich gegen Fehler abzusichern. Ausserdem kannst Du, wenn Du von Anfang an etwas planst, deine Seite direkt bei [Github Pages](https://pages.github.com/) hosten und veröffentlichen.

### Anforderungen

- Startseite/Titelgrafik
- Gebrauchsanweisung, Manual, Bedienungsanleitung, Steuerung
- Spielfluss mit mehreren Entscheidungsmöglichkeiten
- Verschiedene Spielausgänge/Enden
- Abgabe der Seite als `URL`. Die Seite sollte für die Abgabe online gehostet werden, zB. bei [Github Pages](https://pages.github.com/) oder [Uberspace](https://uberspace.de/de/). Das erhöht die Chance, dass das Spiel so auf der nächsten [Werkschau](http://diewerkschaumannheim.de/) gezeigt werden kann, aber auch, dass man Freunde und Bekannte auf einfache Weise probespielen lassen kann, um Feedback zu erhalten.

### Optionale Ideen

- Bildlastiges Spiel, à la [Myst](https://de.wikipedia.org/wiki/Myst#Myst)
- Fantasy- oder Science-Fiction-Themen (Lovecraft?) vs. realitätsnaher Fakultäts-Tatort
- Bedienelemente als Grafiken. Falls du simple Icons für die Bedienung verwendest, sollten diese im Format `SVG` hergestellt werden, zB. in [Sketch](https://www.sketch.com/store/edu/), Illustrator oder notfalls von Hand.
- Visuelle Rückmeldung, zB. [Dialoge](https://developer.mozilla.org/de/docs/Web/HTML/Element/dialog) oder [Toasts](https://codepen.io/kipp0/pen/pPNrrj), für gängige Aktionen.
- Rollenspiel-Aspekte wie Spielereigenschaften (Glück, Stärke, Lebenskraft). Diese liessen sich gut in einem globalen `Javascript`-Objekt, oder Variablen, ablegen.

```javascript
let player = {
	'stats': { // Spielereigenschaften
		'level': 2,
		'health': 25,
		'strength': 15,
		'luck': 10
	},
	'items': { // Gegenstände
		'hasKey': true,
		'hasLamp': false,
		'hasSword': false
	}
};

if (player.items.hasLamp) {
	// Betreten eines dunklen Raums möglich?
}
```

- Ein Spiel kann interessanter, aber auch frustrierender werden, wenn man Zufallselemente einbringt, zB. eine prozentuale Chance, bei einer Entscheidung/Wahl zu versagen.

```javascript
/*
"Öffnen einer verfluchten Kiste"
Aktion erfordert das Gewinnen einer 50/50-Chance,
aber der Glückswert des Spielercharakters verbessert
die Chance.
*/
if ((Math.random()*100 + player.stats.luck) > 50) {
	// Aktion klappt
	player.items.hasKey = true;
} else {
	// Aktion scheitert, Spieler nimmt 5 Schaden
	player.stats.health -= 5;
}
```

### Tips zum Spielfluss

Man kann ein Spiel komplex aufbauen, indem man sich eine Art Engine ausdenkt, die zB. `Javascript`-Objekte nutzt, um Einzelscreens mit Eigenschaften anlegen und speichern zu können, und diese dann dynamisch generiert und anzeigt.
Man kann aber ebenso ein simpleres Format wählen, das die Einzelscreens mit Buttons für Wahlmöglichkeiten bereits in `HTML` vollständig definiert, alle über `CSS` ausblendet und dann jeweils einen davon sichtbar schaltet, je nach Wahl des Spielers.

## Dauer und Abgabe

Die veranschlagte Bearbeitungszeit für diese Aufgabe beträgt `n` Tage, bis zum Ende des Semesters.  
Die Abgabe dieser Aufgabe findet an einem zu vereinbarenden Termin statt, üblicherweise 1-3 Wochen nach Semesterende. Zu diesem Zeitpunkt sind zu übermitteln:

- `URL` des Projekts zu Präsentationszwecken
- Quelldaten des Projekts als Archiv, zB. `.zip`
- Textliche Angaben zu Quellen und durch andere Personen erhaltene Hilfen
- Textliche Angaben zu verwendeter Software, wie Libraries und Plugins

## Referenzen und weiterführende Links

- [Liste von Textadventures](https://de.wikipedia.org/wiki/Liste_von_Textadventures) (Wikipedia)
- [Die Myst-Ära](https://de.wikipedia.org/wiki/Adventure#Die_Myst-%C3%84ra) (Wikipedia)
- [One Page Dungeon](https://watabou.itch.io/one-page-dungeon)
- [ChooseYourStory.com](http://chooseyourstory.com/) (Choose-Your-Own-Adventure style storygames)
- [AI Dungeon](http://ai-adventure.appspot.com/) (AI generated text adventure)

### Code-Beispiele

- [SVG Image Maps](https://gist.github.com/oelna/1efd149dcb9ea0fa8b526a44ff108446) (klickbare Bereiche in Bildern)
- [Random Title Generator](https://gist.github.com/oelna/d85427f6704c2904f537bfec62ca79ec) (zufällig generierte Text-Titel)

### Libraries und Tutorials

- [Vue.js](https://vuejs.org/) (Framework für Webanwendungen, [Wikipedia-Link](https://de.wikipedia.org/wiki/Vue.js))
- [Dragula](https://bevacqua.github.io/dragula/) (drag and drop Library)
- [Javascript Game Loops](https://developer.mozilla.org/en-US/docs/Games/Anatomy) (MDN)
- [Responsive Image Maps](https://wiki.selfhtml.org/wiki/SVG/Tutorials/responsive_Imagemaps) (SelfHTML)
- [My JSON Server](https://my-json-server.typicode.com/) (Simple API mit JSON und Github)
