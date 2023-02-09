# WebTech WS22

## HTML & CSS

* Erklären Sie den Unterschied zwischen Struktur und Layout einer Webseite.
    ```
    Die Struktur handelt sich von der Inhalte der Webseite und wie sie strukturiert sollen.

    Beim Layout geht es um wie etwas auf der Webseite dargestellt werden.
    ```

* Skizzieren Sie den DOM-Baum mit entsprechenden Knoten zu gegebenem HTML. (oder auch umgekehrt möglich)
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
* Geben Sie an um welche HTML-Elemente es sich in einem gegebenen HTML-Layout handelt.
    | Selector                             | Description                                                                                              |
    | ------------------------------------ | -------------------------------------------------------------------------------------------------------- |
    | `#element_id {}`                     | Ein HTML Element mit `id="element_id"`                                                                   |
    | `.element_class {}`                  | Ein HTML Element mit `class="element_class"`                                                             |
    | `video {}`                           | Alle `<video>` Elemente auf der Webseite                                                                 |
    | `* {}`                               | Alle Elemente auf der Webseite                                                                           |
    | `#element_id, .element_class, h1 {}` | Die Gruppe von Elemente mit `id="element_id"`, Elemente mit `class="element_class"` und `<h1>` Elemente. |
    | `[href] {}`                          | Alle Elemente mit dem Attribut `href`                                                                    |

* Woraus besteht eine CSS-Regel und was bewirken diese?
