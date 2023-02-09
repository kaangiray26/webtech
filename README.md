# Fragenkatalog

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
Was ist die Aufgabe der "Request Line" eines HTTP Requests?

Die "Request Line" z.B. (`GET /api/feed HTTP/1.1`) ist notwendig dafür, die Methode für die HTTP Protocol, die Adresse der Resource und den Version von der HTTP Protokol zu bestimmen.

### 4
Erklären Sie die Eigenschaft "Idempotent" mit dem Beispiel der DELETE Methode (Austauschbar mit anderen Eigenschaften und Methoden)

* Wenn eine Methode **idempotent** ist, die Wirkung an dem Server bei einem Request ist das gleiche wie beim mehreren identische Requests an den gliechem Resource.
* Also, die DELETE Methode wird benutzt, um ein Resource an dem Server zu löschen. DELETE ist **idempotent**, weil es immer die gleiche Wirkung an dem Server erzeugt. Dabei, löscht es den Resource an jedem Request, wenn es da vorhanden ist.

### 5
Sie erhalten den Status Code nxy (Konkretisierung durch nє[1-9], x,yє[0-9]). Kreisen Sie die Fehlerursache ein (Austauschbar durch andere Status Codes).

| Code | Bedeutung                              |
| ---- | -------------------------------------- |
| 1xx  | Für Informationen über die Anforderung |
| 2xx  | Für erfolgreiche Anforderungen         |
| 3xx  | Für Umleitung der Anforderung          |
| 4xx  | Für Client-Fehlern                     |
| 5xx  | Für Server-Fehlern                     |
| 9xx  | Proprietäre                            |

### 6
Was ist der Vorteil von HTTPS bzw. TLS?

Die Übertragung zwischen den beiden Endpoints sind beim HTTPS Protokol verschlüsselt. Damit kann man sicher private Daten übertragen. Heute nutzt man TLS.

### 7
In Ihrer Applikation ist die Kommunikation zum Server über den TLS-Standard gesichert. Ist ein Hashing des Passworts seitens Clients weiterhin notwendig? Begründen Sie Ihre Antwort.

Man soll immer den Passwort als Hash zum Server senden. Wenn der Client den Passwort zum Server sendet, wird dies entweder bearbeitet oder speichert. In beiden Fällen Bearbeitung von den tatsächlichen Passwort ist ein Sicherheitsrisiko, da die Person, die den Server verwaltet alles sehen kann. Sonst, gehashte Passworte haben die gleiche Funktionalität.

### 8
Was ist Caching und wie unterscheidet es sich zu gegenüber Sessions und Cookies?

Beim Caching bewahrt man den Response von einer Anforderung für zukünftige Zugriffe auf. Dabei können z.B. Bilder, CSS-Sheets usw. aufbewahrt werden.

Im Vergleich, Sessions und Cookies sind domain-basiert. Diese verwendet man um einige Daten auf dem Browser aufzubewahren und dabei einen Context mit dem Server zu binden.

### 9
Erkläre den Unterschied zwischen einem Proxy und einem Reverse Proxy.

* Bei einem Proxy wird der Client, der die Anforderung macht, unbekannt für den Server sein.
* Bei einem Reverse Proxy aber, sind mehrere Servern unter einem domain gesammelt. Dabei wird der Server, der die Anforderung nimmt, unbekannt für den Client sein.

### 10
Erklären Sie die Funktionsweise des CGI (Common Gateway Interface).

Mit dem CGI werden HTML-Seiten dynamisch erzeugt. Bei jedem Request wird ein Interpreter im Server erzeugt und dies bearbeitet den Request mit einem externen Program, welches im Request spezifiziert wurde.

### 11
Was sind die Vorteile und Nachteile von Apache Modules gegenüber von CGI und Fast CGI? Nennen Sie jeweils x Vor- und Nachteile.

