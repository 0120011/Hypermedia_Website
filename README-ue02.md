# Übung 2 – Die erste Website: HTML-Grundgerüst und erste Styles
HYP1UE_T1 Hypermedia 1 Webprogrammierung | 19.10.2021 | Wolfgang Hochleitner

Es ist nun an der Zeit, den Design-Prototypen, den Sie in Übung 1 in [Figma](https://www.figma.com/) erstellt haben, in eine Webseite mit HTML und CSS zu übertragen. In dieser Übung geht es zunächst darum, eine logische Struktur mit den entsprechenden Gliederungselementen zu erstellen und bereits einige erste CSS-Formatierungen darauf anzuwenden. Beachten Sie, dass es zu Beginn nicht möglich sein wird, den Prototypen genau nachzubauen. Vielmehr handelt es sich über einen stufenweisen Prozess, an dessen Ende eine möglichst getreue Implementierung des Design-Prototypen steht (aber nicht stehen muss, es kann durchaus sein, dass manche Dinge so nicht möglich sind, das ist okay).

## HTML-Struktur

Beginnen Sie zuerst, eine Struktur (das HTML-Grundgerüst) für Ihre Webseite zu definieren.

Legen Sie dazu zunächst eine neue HTML-Datei an und nennen Sie diese `index.html`. Ihr Editor/ihre IDE (z.B. PhpStorm) sollte Ihnen bereits die entsprechende Grundstruktur anlegen. Falls nicht erledigen Sie dies und achten Sie darauf, dass die folgenden Dinge enthalten sind:

- Vollständige und korrekte DOCTYPE-Angabe,
- `<html>`-Element mit `lang`-Attribut, dessen Wert auf Wdie Sprache der Website gesetzt ist,
- `<head>`-Element mit `<title>`-Element und Zeichenkodierungsangebe (UTF-8),
- `<body>`-Element.

Beginnen Sie nun, anhand ihres Figma-Prototyps eine grobe Gliederung mit den passenden HTML-Elementen vorzunehmen. Die folgenden Dinge sollten enthalten sein:

- Ein **Kopfbereich** (`<header>`), z.B. die gesamte Hero-Section Ihrer Seite oder auch nur ein Teil davon (wie z.B. Überschrift und Logo).
- Der **Hauptbereich** (`<main>`), welcher die Hauptinhalte der Seite umfasst.
- Eine Unterteilung des Hauptbereichs in einzelne **Abschnitte** (z.B. About me, Portfolio, Kontakt) mit Hilfe von `<section>`.
- Die **Navigation** (`<nav>`), welche auf die einzelnen Abschnitte innerhalb der Seite verweist. Die Navigation kann innerhalb des Kopfbereichs sein, aber auch außerhalb, d.h. ein Geschwisterelement von `<header>` und `<main>`. Realisieren Sie die eigentliche Navigation darin mit einer **Liste** (`<ul>`/`<ol>`).
- Ein **Fußbereich** (`<footer>`) für abschließende Informationen wie z.B. Copyright, Kontaktdaten (mit `<address>`), social Links, oder ähnlichem.

## HTML-Inhalte

Fahren Sie nun fort mit dem Einbinden weiterer Inhalte, analog zu Ihrem Prototyp. Da wir im Rahmen dieser Lehrveranstaltung noch nicht alle notwendigen CSS-Kenntnisse für die genaue Positionierung von Elementen besitzen, ist es hier vor allem wichtig, diese Elemente im korrekten Bereich einzufügen. Die genaue Anordnung erfolgt in den folgenden beiden Übungen.

- **Textgliederung**: Erstellen Sie für die einzelnen Bereiche die entsprechenden Überschriften (`<h1>` bis `<h6>`, wie benötigt).
- **Fließtext**: Setzen Sie den Fließtext zu den jeweiligen Abschnitten mit Hilfen von Absätzen (`<p>`).
- **Formatierungen auf Textebene**: Wenden Sie wo nötig/gewünscht Formatierungen auf der Textebene (im Fließtext) mit Elementen wie `<em>`, `<strong>` etc. an.
- **Bilder**: Fügen Sie alle Bilder (Logo, Portfolio-Arbeiten, Icons etc.) mit Hilfe von `<img>` Elementen ein. Verwenden Sie wie benötigt Pixelgrafiken (PNG, JPG, GIF, WEBP) oder auch Vektorgrafiken (SVG). Dies betrifft *nicht* Hintergrundbilder. Diese werden über CSS eingebunden (siehe Abschnitt [CSS-Styling](#css-styling)).
- **Links**: Verlinken Sie Inhalte, wie benötigt mit Hilfe des `<a>`-Elements. Dies betrifft vor allem die Navigation mit internen Links aber auch allfällige Verlinkungen zu externen Seiten.
- **Formular**: Erstellen Sie das Kontaktformular mit dem `<form>`-Element und den entsprechenden Eingabefeldern (`<input>`, `<textarea>` etc.) und Buttons (`<button>`). Setzen Sie die für den jeweiligen Inhalt korrekten Typen von Eingabefeldern und verwenden Sie unbedingt Beschriftungen (`<label>`). Sie können auch bei Bedarf mit `<fieldset>` gruppieren.
- **Gruppieren**: Wenn es Sinn macht oder auch für das [Styling](#css-styling) nötig ist, können Sie mehrere Elemente jederzeit auch mit generischen `<div>`-Elementen gruppieren.

## CSS-Styling

Formatieren Sie nun diese Elemente mit Hilfe von Cascading Style Sheets. Im Fokus dieser Übung liegen Farben, Schriftarten und Textanordnung. Positionierungen (im Sinne von Layouts) folgen in den kommenden beiden Übungen.

### Stylesheets organisieren

Um die Styles, die ihre Webseite formatieren, besser verwalten zu können, soll es ein Master-Style-File geben, welches wiederum eine Reihe einzelner Style-Dateien mittels `@import` einbindet.

Legen Sie also zunächst eine Hauptdatei für ihre Styles in einem eigenen Unterordner `css` an (übliche Namen sind etwa `main.css`, `styles.css`, `default.css` etc.). Dann überlegen Sie sich, wie Sie das Styling Ihrer Seite logisch gut gliedern können. So könnte es etwa ein Stylesheet für Schriftformatierung (z.B. `type.css`), ein Stylesheet, das Bilder formatiert (z.B. `images.css`) oder in weiterer Folge (ab der nächsten Übung) auch ein Stylesheet für das Layout (z.B. `layout.css`) geben. Alternativ können Sie auch die Stylesheets nach Art der Selektoren gruppieren, z.B. `elements.css` (für Typ-/Elementselektoren), `classes.css` (für Klassenselektoren) usw.

In diese einzelnen Dateien schreiben Sie im Anschluss die jeweiligen Regeln, die Ihre Seite formatieren. Die einzelnen Teil-Stylesheets binden Sie mittels `@import`-Anweisungen in Ihrer Hauptdatei ein, diese wird dann im HTML-Dokument im `<link>`-Element geladen. Wenn sie später neue Teil-Stylesheets hinzufügen (oder entfernen) wollen, so müssen Sie am HTML-Dokument nichts mehr ändern. Die Änderung geschieht allein in der zentralen CSS-Datei.

### Styles anwenden

Formatieren Sie nun die Inhalte ihres HTML-Grundgerüsts so, dass Sie bereits möglichst gut dem Design-Prototyp entsprechen. Die Formatierungen werden dabei unterschiedlich angewandt:

#### Für das gesamte Dokument

Für das `<body>`-Element werden Formatierungen gesetzt, die zunächst für die ganze Seite gelten sollen und ggf. für einzelne Elemente wieder überschrieben werden.

- **Schriftart**: Wählen Sie eine Standardschriftart für die gesamte Seite. Diese Schrift wird den Fließtext darstellen, für die Überschriften soll in weiterer Folge eine separate Schrift gewählt werden. Um nicht auf die im System installierten Schriften begrenzt zu sein, binden Sie eine Web-Schriftart über [Google Fonts](https://fonts.google.com/) ein. Arbeiten Sie sich dazu selbst in die Funktionsweise dieser Plattform ein und beachten Sie, dass Sie dazu online sein müssen, damit die Web Font auch angezeigt werden kann, da ein Stylesheet eingebunden wird, das bei Google gehostet wird. Binden Sie die CSS-Datei mit den Schriftinformationen mittels `@import`-Deklaration ein (z.B. in die CSS-Datei zur Schriftformatierung oder auch in die Hauptdatei). Verwenden Sie dann die Schriftart ganz normal in der entsprechenden CSS-Regel, setzen Sie jedoch auch mindestens eine Ersatzschriftart aus den klassischen, im System installierten und eine der in der Vorlesung gezeigten Fallback-Schriften, die immer verfügbar sind.
- **Schriftgröße und -farbe**: Wählen Sie die Standard-Schriftgröße und auch -farben analog zu ihrem Design-Prototypen. Dies betrifft vor allem den Fließtext in Absätzen, beeinflusst aber natürlich auch Überschriften, da diese mit relativen `em`-Abgaben auf diesen Formatierungen aufbauen. Die Standardgröße sind `16px`, sie wird bereits vom `<html>`-Element vererbt. Wenn sie später mit relativen `rem` Einheiten arbeiten wollen, können sie auch diesen Wert anpassen, wenn es nötig ist.
- **Hintergrund**: Setzen Sie eine Hintergrundfarbe für Ihre Seite fest. Spezifizieren Sie diese durch eine Farbangabe ihrer Wahl oder spezifizieren Sie ein Hintergrundbild. Anmerkung: diese Farbe wird momentan, sobald die einzelnen Abschnitte eingefärbt werden, überdeckt. Mit Hilfe von Positionierung und Breitenangaben in der kommenden Übung bekommt der Hintergrund wieder mehr Bedeutung.

#### Für einzelne Elemente

Definieren Sie nun Formatierungen für einzelne Elemente, die die zuvor definierten Grundformate überschreiben. Sie können dies mit jeder Art von Selektor erreichen (Element-/Typselektoren, Klassenselektoren, ID-Selektoren, Attributselektoren, diverse Kombinatoren etc.).

- **Überschriften**: Passen Sie Größe, Farbe, Schriftart etc. ihrer Überschriften an, sodass Sie dem Design-Prototypen entsprechen. Denken Sie daran, dass primär die logische Struktur wichtig ist, am Erscheinungsbild können Sie mit CSS so ziemlich alles verändern.
- **Abschnitte**: Heben Sie die einzelnen Abschnitte Ihrer Single-Page Webseite visuell hervor. Arbeiten Sie dazu mit wechselnden Hintergründen. Wählen Sie Bilder oder auch nur Farben. Sie können die Formatierungen über die IDs bei den `<section>`-Elementen oder auch mit Hilfe von Pseudoklassen (um schnell etwa jede zweite Sektion anders zu formatieren) vornehmen.
- **Navigation**: Bereiten Sie ihre Navigation bereits auf ihr endgültiges Erscheinungsbild vor. Dies betrifft heute das Aussehen der Liste. Passen Sie dazu den Style-Typ an. Entfernen Sie z.B. die Bullet-Points oder Aufzählungen, wenn diese bei Ihnen im endgültigen Erscheinungsbild nicht nötig sind. Die Anordnung der Navigation kann mit der folgenden Übung dann vorgenommen werden.
- **Links**: Erstellen Sie Verhalten für Ihre Hyperlinks mit Hilfe der vier Pseudoklassen `:link`, `:visited`, `:hover` und `:active`. Recherchieren Sie dazu, welchen Status eine jede der vier Pseudoklassen genau abdeckt und setzen Sie Formatierungen für alle vier davon. Hinweis: Damit auch alle funktionieren, müssen sie in der richten Reihenfolge im Stylesheet angegeben werden. Diese ist wie zuvor angegeben, als Eselsbrücke kann man sich "**L**o**V**e, **HA**te" merken.
- **CSS-Übergänge und Transformationen**: Bei interaktiven Elementen wie Links kann es gewünscht sein, diese Übergänge flüssiger bzw. in Kombination mit Transformationen (Größenänderungen etc.) zu kombinieren. Falls Sie dies einbauen möchten, werfen Sie einen Blick darauf, wie [Übergänge (Transitions)](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions) und [Transformationen](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transforms/Using_CSS_transforms) funktionieren.

## Tipps und Richtlinien

- Das HTML-Markup muss nach dem aktuellen HTML-Standard validieren. Das Kriterium ist alleinig der [W3C Markup Validator](https://validator.w3.org/). Validieren Sie Ihre Seite regelmäßig und korrigieren Sie Fehler entsprechend.
- CSS muss nach dem aktuellen CSS-Standard validieren. Das Kriterium ist der [W3C CSS Validator](https://jigsaw.w3.org/css-validator/).
- [MDN](https://developer.mozilla.org/en-US/) als Referenz für HTML-Tags und Attribute sowie für CSS verwenden.
- Bei Fragen oder Problemen zur Aufgabe verwenden Sie den Pull Request "Feedback" oder eröffnen Sie Issues. Alternativ können Sie Fragen auch in Microsoft Teams stellen.

