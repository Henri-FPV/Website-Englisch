# Ein Tag in Sydney

Einseitige Website zum Tagesplan mit acht Stationen (11:00–21:30 Uhr): Woolloomooloo, Museum of
Contemporary Art, Eispause am Hafen, Opera House, Royal Botanic Garden, Sydney Harbour National Park,
Abendessen, Vivid Sydney.

Die Seite besteht aus einer einzigen Datei. Kein Build, kein Framework, keine Installation.

## Bei GitHub Pages veröffentlichen

1. Auf github.com ein neues Repository anlegen, zum Beispiel `sydney`, und **Public** auswählen.
2. Auf **Add file → Upload files** klicken und `index.html` (und optional den Ordner `images/`) hochladen.
3. Unten auf **Commit changes** klicken.
4. Im Repository auf **Settings → Pages** gehen.
5. Bei *Source* **Deploy from a branch** wählen, als Branch `main` und als Ordner `/ (root)`, dann **Save**.
6. Nach ein bis zwei Minuten ist die Seite erreichbar unter:
   `https://DEIN-BENUTZERNAME.github.io/sydney/`

Änderungen an `index.html` werden nach jedem Commit automatisch neu veröffentlicht. Wenn die Seite alt
aussieht: einmal mit Strg + F5 neu laden.

Alternativ per Kommandozeile:

```bash
git init
git add .
git commit -m "Sydney-Tagesplan"
git branch -M main
git remote add origin https://github.com/DEIN-BENUTZERNAME/sydney.git
git push -u origin main
```

Pages danach trotzdem einmal unter Settings → Pages aktivieren.

## Eigene Fotos einsetzen

Die Seite bringt für jede Station eine eigene Illustration mit, damit sie ohne zusätzliche Dateien
funktioniert. Sobald ein Foto mit passendem Namen im Ordner `images/` liegt, wird es automatisch
darübergelegt:

| Station | Dateiname |
| --- | --- |
| Woolloomooloo | `images/woolloomooloo.jpg` |
| Museum of Contemporary Art | `images/mca.jpg` |
| Eispause am Hafen | `images/harbour.jpg` |
| Sydney Opera House | `images/opera-house.jpg` |
| Royal Botanic Garden | `images/botanic-garden.jpg` |
| Sydney Harbour National Park | `images/national-park.jpg` |
| Abendessen | `images/dinner.jpg` |

Querformat funktioniert am besten (16:9), etwa 1600 Pixel breit reicht völlig.

Fotos bitte nur aus Quellen nehmen, die das erlauben – eigene Bilder, Wikimedia Commons, Unsplash oder
Pexels. Bei Wikimedia steht die geforderte Namensnennung auf der Bildseite; sie kann unten im Footer
von `index.html` ergänzt werden.

## Was in der Datei wo steht

- Die Stationen sind die `<article class="stop">`-Blöcke. Texte, Zeiten und Infos stehen direkt darin.
- Die Uhrzeit oben in der Leiste kommt aus `data-time` am jeweiligen Stopp.
- Die Farben liegen ganz oben im `<style>` unter `:root`.
- Die Himmelsfarben, die beim Scrollen von Vormittag auf Nacht wechseln, stehen unten im Skript in der
  Liste `skies`.
