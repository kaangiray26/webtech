# WebTech

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