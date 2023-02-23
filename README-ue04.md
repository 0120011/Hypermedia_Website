# Übung 4 – Die erste Website: Grid und Flexbox
HYP1UE_T1 Hypermedia 1 Webprogrammierung | 15./17.11.2021 | Wolfgang Hochleitner

Sie haben in der Vorlesung das CSS Grid Layout und das CSS Flexible Boxes Layout kennengelernt. Verwenden Sie beide, um Ihrer Seite mehr Struktur zu verleihen bzw. Dinge einfacher anzuordnen.

## Layout am Raster

In der letzten Übung haben Sie einen oder mehrere Container in Ihre Seite integriert, um den Inhaltsbereich in der Breite zu begrenzen. Diese Container sind ideal, um mit dem Grid Layout Modul zu experimentieren. Statten Sie alle Ihre Container mit einem Raster aus. Dieser ist – was die Spalten betrifft – sinnvollerweise in allen Abschnitten gleich, um ein konsistentes Erscheinungsbild zu gewährleisten. Sie können aber natürlich auch verschiedene Raster für unterschiedliche Bereiche anlegen, weil etwa der Start- oder Header-Bereich anders angeordnet wird, als Fließtext oder eine Bildergalerie (in der Regel ist dies aber bei einem einigermaßen feinmaschigen Raster gar nicht nötig).

### Responsive Grid

Achten Sie darauf, dass ihr Raster responsive gut funktioniert. Reduzieren Sie etwa bei kleineren Auflösungen entsprechend die Anzahl der Spalten oder verteilen Sie alternativ Elemente über mehrere Spalten. Denken Sie beim Erstellen des Grids daran, dass mobil andere Anforderungen schlagend werden können. Falls Sie etwa Bilder in drei Spalten anordnen, ist es unter Umständen sinnvoller, sechs Spalten zu definieren und ein Bild zunächst über zwei Spalten erstrecken zu lassen. Bei kleineren Auflösungen werden dann nur noch zwei Bilder nebeneinander angezeigt, indem diese sich über jeweils drei Spalten erstrecken und schließlich hat nur noch ein Bild pro Zeile Platz und nimmt alle sechs Spalten ein.

Das Tutorial [A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/) hat alle Eigenschaften des Grid Layouts übersichtlich mit Abbildungen dargestellt.

## Anordnen mit flexiblen Boxen

Das CSS Flexible Boxes Layout ist keine Konkurrenz um Grid Layout, sondern eine sinnvolle Ergänzung. Während im Grid das Layout der Seite festgelegt wird, können mit flexiblen Boxen Elemente darin einfach angeordnet werden.

Verwenden Sie die Eigenschaften des Flexible Box Layout Moduls, Elemente auf Ihrer auszurichten. Sehr gut geeignet sind Dinge, die aktuell mit Hilfe von Floats, `position`- oder `display: inline`-Anweisungen positioniert sind.

Eine Möglichkeit dafür kann eine horizontal angeordnete Navigation sein. Entfernen Sie zunächst die bestehenden Positionierungs-Anweisungen und geben Sie dann dem umgebenden Element (z.B. `<ul>`) die Eigenschaft `display: flex`. Mit `flex-direction` können Sie dann die Richtung bestimmen, in der die Elemente angeordnet sind, mit Eigenschaften wie `justify-content` können Sie die Verteilung von Leerräumen kontrollieren. Mit Hilfe der `flex`-Eigenschaft bei den `<li>`-Elementen können Sie deren grundsätzliche Breite definieren (wenn sie etwa jedes Navigationselement gleich breit gestalten wollen).

Ebenso können Sie auch ihr Formular mittels Flexible Boxes ausrichten. Beachten Sie hierbei, dass das `<fieldset>`-Element (falls in Verwendung) nicht als Flex-Container geeignet ist. Hier ist es besser, alle `<label>`- und `<input>`-Elemente mit einem eigenen Element (z.B. `<div>`) zu umgeben und dort die Eigenschaft `display: flex` zu setzen.

Auch zur vertikalen und horizontalen Zentrierung von Elementen (z.B. Titel der Seite) ist Flexbox perfekt geeignet.

Greifen Sie bei der Arbeit mit flexiblen Boxen auf das Tutorial [A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) zurück. Es enthält alle wichtigen Informationen anhand von konkreten Beispielen.

## Umsetzung und Abgabe

Der Status ihrer Webseite nach Übung 4 zählt als Abgabe. Die Seite sollte weitgehend ihrem Figma-Prototyp entsprechen (es ist aber okay, wenn nicht alles genauso umgesetzt ist).

Folgende Punkte sind für die Abgabe aber relevant und werden beurteilt:

- Vollständige und korrekte HTML-Grundstruktur mit den korrekten HTML-Elementen analog zu [Übung 2](README-ue02.md). Dies Struktur soll semantisch dem Prototyp entsprechen.
- Korrekte Formatierung der Inhalte mit CSS (Schriften, Farben, Abstände, Hintergründe etc.) analog zu [Übung 2](README-ue02.md) und [Übung 3](README-ue03.md).
- Responsive Version (mindestens ein Breakpoint), sodass eine Version für breitere und schmälere Viewports existiert ([Übung 3](README-ue03.md)).
- Korrekte Verwendung des CSS Grid Layout und des CSS Flexible Boxes Layout zur Anordnung der Inhalte entsprechend des Prototyps, analog zu [Übung 4](README-ue04.md).
- Valides HTML und CSS. Beide Validatoren dürfen keine Fehler anzeigen, auch Warnungen sollten vermieden werden.

Bewertet wird der Inhalt des GitHub-Repositories zum Zeitpunkt der Deadline von Übung 4. Arbeiten Sie bereits bei Übung 2 und 3 mit dem Repository und committen Sie regelmäßig ihre Zwischenstände. Auch wenn nach Übung 2 und 3 nichts abzugeben ist bzw. nichts kontrolliert wird, empfiehlt es sich, nicht mit allem bis kurz vor der Deadline zuzuwarten.

## Tipps und Richtlinien

- Das HTML-Markup muss nach dem aktuellen HTML-Standard validieren. Das Kriterium ist alleinig der [W3C Markup Validator](https://validator.w3.org/). Validieren Sie Ihre Seite regelmäßig und korrigieren Sie Fehler entsprechend.
- CSS muss nach dem aktuellen CSS-Standard validieren. Das Kriterium ist der [W3C CSS Validator](https://jigsaw.w3.org/css-validator/).
- Denken Sie beim Schreiben bzw. Abändern ihrer CSS-Stile etwas an die in der Vorlesung vorgestellten CSS-Methodiken – vielleicht lassen sich einige Dinge ja strukturierter damit definieren.
- Falls sie viele wiederkehrende Angaben (z.B. Farbdefinitionen) haben, werfen Sie einen Blick auf [CSS Custom Properties (Variablen)](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties).
- [MDN](https://developer.mozilla.org/en-US/) als Referenz für HTML-Tags und Attribute sowie für CSS verwenden.
- Bei Fragen oder Problemen zur Aufgabe verwenden Sie den Pull Request "Feedback" oder eröffnen Sie Issues. Alternativ können Sie Fragen auch in Microsoft Teams stellen.

