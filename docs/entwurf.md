# Entwurf

In diesen Abschnitt sind die getroffenen Entwurfsentscheidungen und die Strukturen beschrieben, mit denen die Anforderungen umgesetzt sind.

## Entwurfsentscheidungen

### Frontend

Nutzung des Flutter-Frameworks! Warum? Vorteile, Nachteile, usw


### Backend
Die Aufgabe des Backends ist das Bereitstellen von Daten, die im Frontend gebraucht werden. Hierbei geht es um die Abfrage von verfügbaren Serien, Videos, Metadaten sowie das Verwalten von Abonnements.  

Um diese Aufgabe vollumfänglich zu erfüllen ist das Entwickeln einer REST-API nötig, mit der das Frontend Daten mittels HTTP-Requests anfordern kann. Für die Entwicklung unserer REST-API haben wir ein Python-Programm mit dem Webframework [Flask](https://flask.palletsprojects.com/en/2.2.x/) entwickelt.

Mit einem knappen zeitlichen Rahmen und einem kleinen Team, war bei der Auswahl, der für das Backend verwendeten Programmiersprache, vor Allem wichtig, dass wir schnell eine funktionierende Anwendung entwickeln können. Da wir zum Teil schon erfahren in der Verwendung von Python waren und die Sprache außerdem eine im Vergleich sehr leicht zu erlernende Programmiersprache ist, war sie die beste Wahl für uns.

Auch bei der Wahl des Webframeworks legten wir dieses Maß an und entschieden uns für Flask. Flask ist ein light-weight Framework, der relativ minimal ist, sodass schon mit wenig Code ein funktionierender Webserver erstellt werden kann.







## Frontend

Damit die Studierenden der App alle Funktionen nutzen können und sich gut zurechtfinden, gibt es mehrere möglichst intuitive Ansichten. In der folgenden Grafik sind diese Ansichten und ihre Navigationswege zu sehen.

![](assets/images/Frontent-Entwurf_Grafik.jpg)
*App Ansichten und Navigationspfade*

Bevor man auf die eigentliche App zugreifen kann, muss man sich auf der Login Seite anmelden. Diese wird automatisch geöffnet, falls man kein gültiges Token hat, welches man nach anmelden für 6 Monate bekommt. Hier werden die Studierenden durch den Anmeldeprozess geleitet. Detailliertere Informationen gibt es auf der Login (todo: Link einfügen) Seite. Nach erfolgreichen anmelden kommt man zur Hauptansicht der App. 

Bei der Botton Navigation Bar kann man zwischen 3 Ansichten wählen, wie den Studierenden von anderen Apps bereits bekannt sein sollte. Dort können die Studierenden zwischen den Ansichten Home, Suche und Einstellungen wechseln.

### Home
Die Ansicht Home gibt ein Überblick über die Vorlesungsvideos der abbonierten Kurse. Mithilfe des Burgermenüs, welches sich durch den Button am oberen Linken Bildschirmrand öffnen lässt, kann das Semester, welches angezeigt wird, ausgewählt werden. Die abbonierten Kurse des Semesters werden Untereinander angezeigt. Durch runterscrollen werden weitere Kurse angezeigt. Innerhalb der Kurse werden die zugehörigen Vorlesungen angezeigt. Hier kann nach rechts gescrollt werden um weitere Videos sehen zu können. Durch klicken auf den Titel einer Vorlesung gelangt man zur Kursansicht. Durch klicken auf ein Video, gelangt man hingegen direkt zur Videoansicht.

#### Kursansicht
In dieser Ansicht werden Alle Videos zu einem Kurs untereinander Angezeigt. Zu jedem Video wird ein Thumbnail und einige Metainformationen angezeigt. Durch Klicken auf ein Video, gelangt man zur Videoansicht. 

#### Videoansicht
In dieser Ansicht kann das eigentliche Video angeschaut werden. Im Hochkantformat werden unter dem Player noch einige Informationen zum Video angezeigt, im Querformat hingegen nimmt der Player den ganzen Bildschirm ein. Mit dem drei Punkte Symbol oben rechts in der Ecke lässt sich das Menü öffnen. Hier kann die Videoqualiät, die Abspielgeschwindigkeit anpassen und außerdem kann zwischen den verschiedenen Ansichten des Videos gewechselt werden (Vorlesungsfolien vs. Vortragender) falls vorhanden. Durch doppel tippen rechts, bzw. links kann 10 Sekunden vor bzw, zurück gespult werden. 

### Suche

Die Ansicht Suche ist dafür da neue Kurse zu Abonnieren, um deren Vorlesungsvideos ansehen zu können. Mithilfe der Suchleiste kann man nach Titel oder anderen Metainformationen zu den Vorlesungen Suchen. Zu den Meainformationen zählen zu Beispiel der Name des Vortragenden oder die Beschreibung der Vorlesung. Es werden maximal 10 passende Ergebnisse Angezeigt. Ist ein Kurs noch nicht abboniert, wird neben dem Titel ein Plus angeziegt. Ist der Kurs hingegen bereits abboniert, wird ein Minus angezeigt.

Durch klicken auf das Plus oder den Titel des Kurses, wird der abbonieren Dialog geöffnet. Hier wird, falls benötigt der Einschreibeschlüssel angegeben und überprüft. Außerdem wird ein Semester gewählt, zu dem der Kurs hinzugefügt werden soll. Von März bis inklusive August wird standardmäßig das aktuelle Sommersemester vorgeschlagen, Von September bis inklusive Februar hingegen das aktuelle Wintersemester. Falls das vorgeschlagene Semester nicht gewünscht ist, kann ein Semester früher oder später ausgewählt werden. Nach Bestätigen wird der Einschreibeschlüssel, falls vorhanden, überprüft. Ist jener korrekt, wird der Studierende in den Kurs eingeschrieben. Nach erfolgreichen Einschreiben oder falls der Studierende bereits Eingeschrieben ist und auf den Titel des Kurses klickt, wird er zur Kursansicht des Kurses weitergeleitet. Durch klicken des Minuses neben dem Titel eines abbonierten Kurses, wird der Kurs deabboniert und ein Hinweis hierzu wird am unteren Rand des Bildschirmes Angezeigt. 

### Einstellungen

fortsetzung folgt

ist das nicht quasi schon ein Userguide?

## Backend

Das Backend stellt die Daten für das Frontend bereit. App spezifische Daten, wie z.B. die Abonnierten Vorlesungen der Studierenden sind in der Datenbank (todo: link Datenbank) von dem Backend gespeichert. Diese werden vom Backend aufbereitet und durch HTTPS API-Endpunkte bereitgestellt.

Die Vorlesungsvideos und die Metadaten zu jenen hat jede Hochschule auf ihrer educast Instanz gespeichert. 

Grafik