# Übung 4 (Javascript)

Verwende das HTML-Element `<video>`, um einen Videoplayer zu entwerfen.

Nutze anschliessend Javascript, um die Bedienelemente mit Funktionalität zu versehen.

## Anweisung

Die Anleitung unter
[MDN: Video und Audio APIs](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Video_and_audio_APIs) (englisch) lässt sich gut dafür verwenden. Für die Aufgabe ist nicht nötig, Seeking oder sonstige, über einfache Play/Pause/Skip Funktionalität hinausgehende, Aspekte umzusetzen.

Wähle in Javascript das Video-Element aus:
```javascript
const videoEle = document.querySelector('video');
```

Verwende die vordefinierten Funktionen um das Video zu starten oder zu pausieren:
```javascript
videoEle.play();
videoEle.pause();
```

Das ganze soll beim Klick auf eines deiner Bedienelemente passieren:
```javascript
const playMedia = function () {
    videoEle.play();
}

const playButton = document.querySelector(".playbutton");
playButton.addEventListener("click", playMedia);
```

Gestalte den Player mit `CSS`, ansprechend und funktional. Er sollte direkt responsive gehalten sein, so dass die Größe des Anzeigefensters keine Rolle für die Benutzbarkeit spielt.

**Bonusaufgabe:**

- Gestalte Grafiken für die Bedienelemente und binde sie statt der Texte, oder ergänzend zu ihnen, ein.
- Informiere dich über die weiteren vordefinierten Funktionalitäten des `<video>`-Elements und verbessere deinen Player, zB. mit Seeking, Mute, oder weiteren Funktionen. Als Vorlage können zB. [Youtube](https://www.youtube.com/), [Vimeo](https://vimeo.com/), oder [Twitch](https://www.twitch.tv/) dienen.
- Auf die gleiche Weise lässt sich auch ein Audioplayer mit dem `<audio>`-Element umsetzen.

## Dauer und Abgabe

Die veranschlagte Bearbeitungszeit für diese Aufgabe beträgt 7 Tage, bis zur nächsten Kursstunde.  
Die Abgabe dieser Aufgabe ist nicht vorgesehen und dient lediglich deiner eigenen Übung.

## Referenzen und weiterführende Links

### MDN

- [`<video>`](https://developer.mozilla.org/de/docs/Web/HTML/Element/video)
- [`<audio>`](https://developer.mozilla.org/de/docs/Web/HTML/Element/audio)
- [Funktionen in Javascript](https://developer.mozilla.org/de/docs/Web/JavaScript/Guide/Funktionen)