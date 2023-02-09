# Notes

## HTML & CSS

### 1
Erklären Sie den Unterschied zwischen Struktur und Layout einer Webseite.

* Die Struktur handelt sich von der Inhalte der Webseite und wie sie strukturiert sollen.
* Beim Layout geht es um wie etwas auf der Webseite dargestellt werden.

### 2
Skizzieren Sie den DOM-Baum mit entsprechenden Knoten zu gegebenem HTML. (oder auch umgekehrt möglich)

```
<html>
    <body>
        <main>
            <article>
                <section contenteditable="true">
                    Dies ist die erste übung im WebTech
                    <br>
                    Aufgabe 2
                </section>
            </article>
        </main>
    </body>
</html>
```
```
[main]
|
[article]
|
[section]
|
|-> {contenteditable}->("true")
|
|-> (Dies ist die erste übung in WebTech)
|
|-> [br]
|
|-> (Aufgabe 2)

[] ist ein HTML-Element
{} ist eine Attribute
() ist ein Text
```

### 3
Geben Sie an um welche HTML-Elemente es sich in einem gegebenen HTML-Layout handelt.

| Selector                             | Description                                                                                              |
| ------------------------------------ | -------------------------------------------------------------------------------------------------------- |
| `#element_id {}`                     | Ein HTML Element mit `id="element_id"`                                                                   |
| `.element_class {}`                  | Ein HTML Element mit `class="element_class"`                                                             |
| `video {}`                           | Alle `<video>` Elemente auf der Webseite                                                                 |
| `* {}`                               | Alle Elemente auf der Webseite                                                                           |
| `#element_id, .element_class, h1 {}` | Die Gruppe von Elemente mit `id="element_id"`, Elemente mit `class="element_class"` und `<h1>` Elemente. |
| `[href] {}`                          | Alle Elemente mit dem Attribut `href`                                                                    |

### 4
Woraus besteht eine CSS-Regel und was bewirken diese?

* Ein CSS-Regel besteht aus zwei Teile: Selector und Declaration
* Selector ist für bestimmen, auf welche HTML-Elemente diese Regel wirken.
* Declaration ist für bestimmen, welche Layout-Eigenschaften angewandt werden.

### 5
Welche Arten gibt es CSS-Regeln einzubinden? Wann ist welche Art sinnvoll? (Vor- und Nachteile)

* Man kann CSS-Regeln in drei Wege einbinden:
* Man kann ein inline-CSS einbinden, indem die `style` Attribut angewandt wird.
* Man kann den `<style>` Element im HTML Head hinfügen.
* Man kann einen externen CSS-Sheet einbinden mit dem `<link rel="stylesheet" href="stylesheet.css">`.
  
### 6
Welche Arten von Selektoren gibt es und wann ist deren Verwendung sinnvoll?

* Siehe (HTML & CSS/ Frage 3)

### 7
Beschriften Sie eine HTML-Layout-Abbildung gemäß des gegebenen CSS und HTML.

* Siehe Übungsblatt 2/Aufgabe 1

### 8
Welche Spezifität hat eine gegebene CSS-Regel?

| Selector       | Spezifität |
| -------------- | ---------- |
| id             | 100        |
| class          | 010        |
| element        | 001        |
| style-Attribut | 1000       |

Bsp:

| CSS-Rule                                   | Spezifität |
| ------------------------------------------ | ---------- |
| `#wrapper article .header .navbar a {...}` | 122        |

### 9
Was sind wichtige HTML-Tags, um eine HTML5 Seite aufzubauen? (Beschreiben Sie in einem Satz jeweils die Funktion des Tags. Nennen Sie 5 HTML-Tags.

1. `<nav>`: Man nutzt es um Linke für die Navigation hinzulegen.
2. `<div>`: Man kann es benutzen um Containers für die Elemente darunten zu erstellen.
3. `<h1><h2>...<h6>`: Dient dazu Headings zu erstellen.
4. `<footer>`: Enthält wichtige Informationen für die Section, die diese Footer enthält, oder für die Webseite.
5. `<section>`: Für die Abschnitte, die ein Heading und weitere Inhalte enthalten.

### 10
Auf einer Webseite werden die Umlaute kryptisch dargestellt. Welche Ursachen könnten dieses Verhalten haben? Welche Optionen gibt es das Verhalten zu korrigieren?

* Nicht alle Webseiten unterstützen die Sonderzeichen wie `ä,ü,ö` et cetera. Um dieses Problem zu lösen kann man einfach die Charset der Webseite deklarieren mit `<meta charset="UTF-8">` innerhalb der `<head>` Element.

## Server

### 1
Beschreiben Sie die Funktionsweise und Eigenschaften des HyperText Transfer Protocols.

* HTTP ist ein Protokol zur Übertragung von Daten an der Anwendungsschicht.
* Es ist zustandlos und funktioniert über Requests und Responses.

### 2
Wofür sind die HTTP Header Informationen nützlich oder notwendig?

* Da HTTP zustandlos ist, man muss einige notwendige Informationen im HTTP Header behalten.
* Dies kann man benutzen z.B. um den Typ der Inhalt zu bestimmen (`Content-Type`).
* Oder kann man die Cache-Eigenschaften verwalten (`Cache-Control`).
* Oder kann man die User Agent des Geräts noch deklarieren (`User-Agent`).

### 3
