## Hypertext-Markup-Language (HTML)

Hypertext-Markup-Language ist keine Programmiersprache ist keine Programmiersprache, sondern eine Auszeichnungssprache, welche vorrangig für die Strukturierung von Dokumenten konzipiert wurde. Ein HTML Starttag beginnt mit eckigen Klammern wie in diesem Beispiel `<p>`. Das entsprechende Endtag wird wie ein Starttag geschrieben mit der Ausnahme, dass ein Forwardslash dem Namen voran gestellt wird `</p>`. In der Regel müssen die meisten HTML-Tags auch mit einem Endtag geschlossen werden, allerdings ist dies nicht immer nötig. 

    
    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>Document</title>
    </head>
    <body>
        <h1>Das ist ein Titel!</h1>
        Dies ist normaler Text. Der Text wird umgebrochen, wenn ich ein Breaktag setze. <br>
        Ich kann auch text <b>fett schreiben lassen</b> oder <i>kursiv</i>. Wenn wir ein Bild einfügen 
        wollen, so machen wir das in einem Imagetag mit Pfad 
        <img src="https://www.w3schools.com/images/lamp.jpg" alt="Lampe">. Wir können auch 
        eine ganz andere Seite <a href="https://www.google.de/">verlinken</a>
    </body>
    </html>
  
  Wir in diesem Beispiel sehen, haben einige Tags keine Endtags. Andere Tag funktionieren allerdings erst, wenn wir zusätzliche Angaben wie im Image-Tag machen.

| Tag       | Beschreibung                                                                                         | Endtag      |
|:---------:|------------------------------------------------------------------------------------------------------|-------------|
|`<p>`      | *Paragraph*-Tag fügt einen Paragraph ein.                                                            |optional     |
|`<h1>`     | *Header*-Tag erzeugt eine Überschrift. Mit höherer Nummer werden kleinere Überschriften erzeugt      |obligatorisch|
|`<br>`     | *Break*-Tag erzwingt eine neue Zeile.                                                                |nein         |
|`<b>`      | *Bold*-Tag schreibt den Text im Inneren fett.                                                        |obligatorisch|
|`<i>`      | *Italic*-Tag schreibt Text kursiv.                                                                   |obligatorisch|
|`<img>`    | *Image*-Tag. Damit ein Bild angezeigt wird muss eine Quelle angegeben werden.                        |nein         |
|`<a>`      | *Anchor*-Tag verlinkt mit dem *href* Attribut eine andere Seite.                                     |obligatorisch|
|`<div>`    | *Divisions*-Tag hat keine direkte Auswirkung auf Inhalt im Tag und fügt am Ende einen Line-Break ein.|obligatorisch| 
|`<span>`   |  Hat keine direkte Auswirkung auf Inhalt im Tag und fügt keinen Line-Break am Ende ein.              |obligatorisch| 
    
## Cascading Style Sheets (CSS)
Wenn wir diese Website im Browser aufrufen sehen wir, dass diese Website praktisch ungestylt ist. Um dies zu ändern benutzen wir **CSS**. CSS ist eine Sylesheet Sprache, welche HTML-Elemente ansteuert, um deren aussehen zu verändern. Es gibt drei Möglichkeiten, um CSS in einem HTML-Dokument anzusteuern. Wir können zum einen CSS direkt im HTML-Tag anwenden, im HTML-Dokument oder in einer externen CSS-Datei. Am besten können wir CSS über ein sogenanntes Box-Modell verstehen. Das heißt, dass wir jedes HTML-Element im Prinzip eine Box darstellt die wir mit CSS ansteuern und verändern können.

    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>Document</title>
    </head>
    <body>
        <h1 style="background-color: blue; color: white;">Das ist ein Titel!</h1>
        <p style="font-style:italic">Dies ist normaler Text. Der Text wird umgebrochen, wenn ich ein Breaktag setze. <br>
        Ich kann auch text <b>fett schreiben lassen</b> oder <i style="font-style : normal">kursiv</i>. Wenn wir ein Bild einfügen 
        wollen, so machen wir das in einem Imagetag mit Pfad</p> 
        <img src="https://www.w3schools.com/images/lamp.jpg" alt="Lampe">. Wir können auch 
        eine ganz andere Seite <a href="https://www.google.de/">verlinken</a>
        <div>Ein Divisions-Tag keine Auswirkung</div>
    </body>
    </html>
    
Da es sehr aufwendig sein kann alle HTML-Tag so einzeln anzusteuern können wir mit einem **Selektor** auch bestimmte HTML-Elementze ansteuern.

    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>Document</title>
      
      <style>
        h1 {
            background-color: blue;
        }
        
        p {
            font-style: italic;
        }
      </style>
    </head>
    <body>
        <h1>Das ist ein Titel!</h1>
        <p>Dies ist normaler Text. Der Text wird umgebrochen, wenn ich ein Breaktag setze. <br>
        Ich kann auch text <b>fett schreiben lassen</b> oder <i>kursiv</i>. Wenn wir ein Bild einfügen 
        wollen, so machen wir das in einem Imagetag mit Pfad</p> 
        <img src="https://www.w3schools.com/images/lamp.jpg" alt="Lampe">. Wir können auch 
        eine ganz andere Seite <a href="https://www.google.de/">verlinken</a>
    </body>
    </html>
    
Wie Javascript Dateien können wir den CSS Code auch in ein externes CSS auslagern indem wir diese Datei im `<link rel="stylesheet" href="style.css">` verlinken.

## Selektoren 
Wir haben in dem letzten Abschnitt bereits gesehen, dass wir einzelne Tags ansteuern können. Wenn wir aber einzelne Gruppen von Tags ansteuern wollen dann brauchen wir genauere Selektoren. Dafür gibt es verschiedene HTML-Attribute die wir beim erstellen des HTML-Dokuments vergeben können. 

    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>Document</title>
      
      <style>
        // Klasse wird im Tag angegeben.
        .meineKlasse {
            background-color: blue;
        }
        
        // Id wird wie eine Klasse angegeben
        #Titel2 {
            font-style: italic;
        }
        
        // Wählt alle div Tags aus die einen p Tag als Parent haben  
        p > div {
              background-color: red;
        }
      </style>
    </head>
    <body>
        <h1>Das ist ein Titel!</h1>
        <h1 id="Titel2">Zweiter Titel</h1>
        <p>Dies ist normaler Text. Der Text wird umgebrochen, wenn ich ein Breaktag setze. <br>
        Ich kann <div class="meineKlasse">auch text <b>fett schreiben lassen</b> oder <i>kursiv</i>. Wenn wir</div> ein Bild einfügen 
        wollen, so machen wir das in einem Imagetag mit Pfad</p> 
        <img src="https://www.w3schools.com/images/lamp.jpg" alt="Lampe">. Wir können auch 
        eine ganz andere Seite <a href="https://www.google.de/">verlinken</a>
    </body>
    </html>
    
Hier ist eine vollständige [Referenz](https://www.w3schools.com/css/css_selectors.asp) für alle Selektoren.

## Domain-Object-Model (DOM)
Wenn wir eine Seite mit JavaScript verlinken so haben wir Zugang zum sogenannten *Domain-Objekt-Model*. Das heißt, dass das JavaScript alle HTML-Elemente und alle CSS-Eigenschaften in ein JavaScript Objekt bündelt und im Skript zur Verfügung stellt. Wenn wir jetzt in einem Skript Anpassungen am DOM machen, so sehen wir die Veränderung auch direkt auf der Website. Da ein Skript direkt beim Laden der Seite ausgeführt wird fügen wir in das DOM EventListener ein, welche nur auf bestimmte Events reagieren. Hierzu ein Beispiel:

    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>Document</title>
      
      <style>
        .meineKlasse {
            background-color: blue;
        }
        
        #Titel2 {
            font-style: italic;
        }
      </style>
    </head>
    <body>
        <button>Drück mich!</button>
        <script>
            const BUTTON = document.querySelector("button");
            BUTTON.addEventListener("click", buttonClicked);

            function buttonClicked() {
                BUTTON.style.backgroundColor="red";
                BUTTON.innerHTML="Ja du hast mich gedrückt!";
            }
        </script>
    </body>
    </html>
    
Um mit dem DOM zu interagieren gibt es mehrere Methoden die wir hier Beipielhaft darstellen wollen

| Methode            | Beschreibung                                                                             |
|:------------------:|------------------------------------------------------------------------------------------|
|`querySelector`     | Wählt den ersten Tag oder die erste Klasse aus die gefunden wird.                        |
|`querySelectorAll`  | Wählt alle Tags oder alle Klassen aus die gefunden werden und gibt eine Liste zurück     |
|`addEventListener`  | Fügt einen Eventlistener hinzu, welcher unter einer bestimmten Bedingung ausgeführt wird.|
|`getElementById`    | Wählt den ersten Tag mit der speziellen Id aus der gefunden wird.                        |         
