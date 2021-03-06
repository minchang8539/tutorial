# Django - Was ist das?

Django (*/ˈdʒæŋɡoʊ/*) ist ein freies, quelloffenes Web-Anwendungs-Framework, geschrieben in Python. Ein Web-(Anwendungs-)Framework ist eine Art Baukastensystem, das dir mit vielen vorgefertigten Teilen die Entwicklung von Web-Anwendungen stark erleichtert.

Wenn du eine Website entwickelst, brauchst du immer wieder sehr ähnliche Elemente: Einen Weg, Benutzer zu verwalten (Registrierung, Anmeldung, Abmeldung etc.), einen Administrationsbereich, Formulare, Upload von Dateien usw.

Glücklicherweise wurde schon vor einiger Zeit erkannt, dass Web-Entwickler immer wieder die gleichen Probleme zu lösen haben. Gemeinsam entstanden so verschiedene Frameworks (Django ist so eines), welche die Web-Entwicklung durch vorgefertigte Elemente erleichtern.

Frameworks sind dazu da, damit du das Rad nicht neu erfinden musst. Du kannst dich auf die konkret zu erfüllenden Anforderungen der Webseite kümmern. Die grundlegende Basis der Webseite stellt dir das Framework zur Verfügung.

## Warum brauchst du ein Framework?

Um besser zu verstehen, welche Vorteile dir Django bietet, werfen wir einen Blick auf Server im Allgemeinen. Als Erstes muss der Server wissen, dass er eine Webseite ausliefern soll.

Der Server hat mehrere "Ports". Ein Port ist vergleichbar mit einem Briefkasten, der auf eingehende Briefe ("Anfragen", "requests") überwacht wird. Das macht der Webserver. Der Webserver liest die eingeworfenen Briefe (requests) und beantwortet sie mit der Webseite (response). Um etwas ausliefern zu können, brauchen wir Inhalte. Und Django hilft dir dabei, diese Inhalte zu erstellen.

## Was passiert, wenn jemand eine Webseite beim Server anfordert?

Wenn die Anfrage beim Web-Server ankommt, reicht er diese an Django weiter. Und Django versucht herauszufinden, welche Seite genau angefordert wurde. Django wertet zuerst die Adresse der Webseite aus und versucht herauszufinden, was getan werden soll. Dafür ist der **urlresolver** von Django verantwortlich (Hinweis: URL - Uniform Resource Locator ist ein anderer Name für die Web-Adresse, daher der Name *urlresolver*). Sehr schlau ist er aber nicht. Er hat eine Musterliste und vergleicht diese mit der URL. Der Vergleich der Muster erfolgt von oben nach unten. Wenn ein Muster auf die URL zutrifft, wird der damit verknüpften Funktion (der sogenannten *view*) der Request/die Anfrage übergeben.

Stell dir eine Postbotin mit einem Brief vor. Sie geht die Straße entlang und prüft jede Hausnummer mit der Adresse auf dem Brief. Wenn beide passen, dann steckt sie den Brief in den Briefkasten. So funktioniert der urlresolver!

In der *view* Funktion passieren all die interessanten Dinge: wir können in eine Datenbank gucken und dort nach Informationen suchen. Vielleicht wollte die Benutzerin irgendetwas in den Daten ändern? So, als ob der Brief sagen würde: "Bitte ändere meine Stellenbeschreibung!" Die Funktion *view* kann nun prüfen, ob du dazu berechtigt bist, im positiven Fall die Änderungen durchführen und im Anschluss eine Bestätigungs-Nachricht zurücksenden. Die *view* generiert dann eine Antwort und Django kann diese an den Webbrowser der Benutzerin senden.

Die Beschreibung oben ist ein wenig vereinfacht, aber du musst noch nicht all die technischen Details wissen. Eine generelle Vorstellung zu haben, reicht erstmal.

Anstatt zu sehr ins Detail zu gehen, fangen wir lieber an, mit Django etwas zu erschaffen, und du wirst dabei alles Wichtige lernen!