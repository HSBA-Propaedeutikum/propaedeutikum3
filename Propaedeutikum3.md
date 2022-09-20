## Hypertext-Markup-Language (HTML)

Hypertext-Markup-Language ist keine Programmiersprache ist keine Programmiersprache, sondern eine Auszeichnungssprache, welche vorrangig für die Strukturierung von Dokumenten konzipiert wurde. Ein HTML Starttag beginnt mit eckigen Klammern wie in diesem Beispiel `<p>`. Das entsprechende Endtag wird wie ein Starttag geschrieben mit der Ausnahme, dass ein Forwardslash dem Namen voran gestellt wird `</p>`. In der Regel müssen die meisten HTML-Tags auch mit einem Endtag geschlossen werden, allerdings ist dies nicht immer nötig. 

    
    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>Document</title>
    </head>
    <body>
        <h1>Hier kommt der Inhalt rein.</h1>
        Dies ist normaler Text. Der Text wird umgebrochen, wenn ich ein Breaktag setze. <br>
        Ich kann auch text <b>fett schreiben lassen</b> oder <i>kursiv</i>. Wenn wir ein Bild einfügen 
        wollen, so machen wir das in einem Imagetag mit Pfad 
        <img src="https://de.wikipedia.org/wiki/Pizza#/media/Datei:Eq_it-na_pizza-margherita_sep2005_sml.jpg" alt="Pizza"> 
    </body>
    </html>
  
  Wir in diesem Beispiel sehen, haben einige Tags keine Endtags. Andere Tag funktionieren allerdings erst, wenn wir zusätzliche Angaben wie im Image-Tag machen.

  | Tag       | Beschreibung                                                                                   | Endtag      |
  |-----------|------------------------------------------------------------------------------------------------|-------------|
  |`<p>`      | Der Paragraph-Tag fügt einen Paragraph ein.                                                    |optional     |
  |`<h1>`     | Header-Tag erzeugt eine Überschrift. Mit höherer Nummer werden kleinere Überschriften erzeugt  |obligatorisch|
  |`<br>`     | Break-Tag erzwingt eine neue Zeile.                                                            |nein         |
  |`<b>`      | Bold-Tag schreibt den Text im Inneren fett.                                                    |obligatorisch|
  |`<i>`      | Italic-Tag schreibt Text kursiv.                                                               |obligatorisch|
  |`<img>`    | Image-Tag. Damit ein Bild angezeigt wird muss eine Quelle angegeben werden.                    |nein         |
