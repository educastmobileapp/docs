# Entwurf

In diesen Abschnitt sind die Strukturen beschrieben, mit denen die Anforderungen umgesetzt sind. Unterteilt sind diese in Frontend und Backend.

## Frontend

Damit die Studierenden der App alle Funktionen nutzen können und sich gut zurechtfinden, gibt es mehrere möglichst intuitive Ansichten. In der folgenden Grafik sind diese Ansichten und ihre Navigationswege zu sehen.

![](assets/images/Frontent-Entwurf_Grafik.jpg)
*App Ansichten und Navigationspfade*

Bevor man auf die eigentliche App zugreifen kann, muss man sich auf der Login Seite anmelden. Diese wird automatisch geöffnet, falls man kein gültiges Token hat, welches man nach anmelden für 6 Monate bekommt. Hier werden die Studierenden durch den Anmeldeprozess geleitet. Detailliertere Informationen gibt es auf der Login (todo: Link einfügen) Seite. Nach erfolgreichen anmelden kommt man zur Hauptansicht der App. 

Bei der Botton Navigation Bar kann man zwischen 3 Ansichten wählen, wie den Studierenden von anderen Apps bereits bekannt sein sollte. Dort können die Studierenden zwischen den Ansichten Home, Suche und Einstellungen wechseln.

Home

Die Ansicht Suche ist dafür da neue Kurse zu Abonnieren, um deren Vorlesungsvideos ansehen zu können.

Einstellungen

fortsetzung folgft

ist das nicht quasi schon ein Userguide?

## Backend

Das Backend stellt die Daten für das Frontend bereit. App spezifische Daten, wie z.B. die Abonnierten Vorlesungen der Studierenden sind in der Datenbank (todo: link Datenbank) von dem Backend gespeichert. Diese werden vom Backend aufbereitet und durch HTTPS API-Endpunkte bereitgestellt.

Die Vorlesungsvideos und die Metadaten zu jenen hat jede Hochschule auf ihrer educast Instanz gespeichert. 

Grafik