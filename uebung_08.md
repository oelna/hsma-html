# Übung 8

Erweitere deine Slideshow um Responsive Images mit [`srcset`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/srcset) und [`<picture>`](https://developer.mozilla.org/de/docs/Web/HTML/Element/picture)


## Anweisung

Deine Slideshow aus [Übung 6](uebung_06.md) soll verbessert werden, indem die Bilder den Ausgabegeräten angepasst werden. Untersuche dafür, in welchen wirklichen Größen deine Seite die Bilder anzeigt. Du brauchst diese Information, um sie im `sizes`-Attribut anzugeben. Nur so kann der Browser aus einer Liste möglicher Bilddateien die passende auswählen.

Denke auch daran, deine JPG- oder PNG-Dateien mit [ImageOptim](https://imageoptim.com/versions) (oder ähnlichem) zu optimieren.

### Beispiel

```html
<img srcset="pasta-alla-chef-320w.jpg 320w,
             pasta-alla-chef-480w.jpg 480w,
             pasta-alla-chef-800w.jpg 800w"
     sizes="(max-width: 320px) 280px,
            (max-width: 480px) 440px,
            800px"
     src="pasta-alla-chef-800w.jpg" alt="Nudeln mit Schinken, Erbsen und Sahne" />
```

**Bonusaufgabe:**

- Verwende das `type`-Attribut, um deinen `<picture>`-Elementen Bilddateien in verschiedenen Formaten zur Verfügung zu stellen, zum Beispiel in [`.WEBP`](https://de.wikipedia.org/wiki/WebP). ([Example Repo mit Code](https://github.com/oelna/picture-element-example))

## Dauer und Abgabe

Die veranschlagte Bearbeitungszeit für diese Aufgabe beträgt 7 Tage, bis zur nächsten Kursstunde.  
Die Abgabe dieser Aufgabe ist nicht vorgesehen und dient lediglich deiner eigenen Übung.

## Referenzen und weiterführende Links

### Elemente

- [`srcset`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/srcset)
- [`<picture>`](https://developer.mozilla.org/de/docs/Web/HTML/Element/picture)

### Programme

- [ImageOptim](https://imageoptim.com/versions) (Mac)
- [FileOptimizer](https://sourceforge.net/projects/nikkhokkho/) (Win)
- [Squoosh](https://squoosh.app/) (Website)
- [avif CLI converter](https://github.com/Kagami/go-avif/releases) (Mac, Win)

### Verschiedene

- [CSS-Tricks: Responsive Images](https://css-tricks.com/responsive-images-css/) (englisch)
- [Picture perfect images](https://stackoverflow.blog/2022/03/28/picture-perfect-images-with-the-modern-element/) (englisch)
- [Serving sharp images to Retina screens](https://jakearchibald.com/2021/serving-sharp-images-to-high-density-screens/) (englisch)
- [Image Resizing with Imagemagick](https://www.smashingmagazine.com/2015/06/efficient-image-resizing-with-imagemagick/) (englisch)
- [DPI.lv](https://dpi.lv/) Auflösung von Screens berechnen (englisch)
- [Understanding DPI](https://affinityspotlight.com/article/understanding-dpi/) (englisch)
- [Next generation image codecs](https://cloudinary.com/blog/time_for_next_gen_codecs_to_dethrone_jpeg) (siehe Bild unten)

![](https://res.cloudinary.com/cloudinary-marketing/image/upload/w_700,c_fill,f_auto,q_auto,dpr_2.0/Web_Assets/blog/Battle-of-the-Codecs_fnl.png)
