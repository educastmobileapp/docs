# Userguide

In diesem Abschnitt wird Ihnen eine Schritt-für-Schritt Anleitung beschrieben, wie Sie unsere App nutzen können und welche Funktionalitäten Ihnen zur Verfügung stehen. 

Damit die Studierenden alle Funktionen der App nutzen können und sich gut zurechtfinden, gibt es mehrere möglichst intuitive Ansichten. In der folgenden Grafik sind diese Ansichten und ihre Navigationswege zu sehen.
![](/assets/images/Frontent-Entwurf_Grafik.jpg)

### Login

Bevor man auf die eigentliche App zugreifen kann, muss man sich auf der Login Seite anmelden. Der Anmeldeprozess erfolgt über die Authentifikations- und Autorisierungs-Infrastruktur des Deutschen Forschungsnetzes (DFN-AAI). Dabei wählt der:die Studierende seine Universität oder Fachhochschule aus und meldet sich dann mit den entsprechenden Zugangsdaten an.  Detailliertere Informationen und technische Hintergründe finden Sie auf der [Login Seite](login.md). Nach erfolgreichem Anmelden kommt man zur Hauptansicht der App.

**Bottom Navigation Bar**

Über die dauerhaft eingeblendete Bottom Navigation Bar können Sie zwischen drei Ansichten wählen, wie den Studierenden von anderen Apps bereits bekannt sein sollte. Dort können die Studierenden zwischen den Ansichten [Home](userguide.md#home), [Suche](userguide.md#suche) und [Einstellungen](userguide.md#einstellungen) wechseln.

### Home
Auf der Homeansicht sieht man zunächst einmal alle im derzeitigen Semester abonnierten Kurse und die zugehörigen Vorlesungsvideos. Zum Aktualisieren zieht man die Seite einmal nach unten. 

Dabei ist der Aufbau so, dass alle Kurse untereinander angeordnet sind und man dementsprechend durch vertikales Scrollen nach und nach alle seine Kurse untereinander angezeigt bekommt. Durch Anklicken des Kurstitels wechselt man zur [Kursansicht](userguide.md#kursansicht) dieses Kurses. 

Die Videos eines Kurses sind im Gegensatz dazu nebeneinander angeordnet und durch horizontales Wischen alle zu betrachten. Dabei werden einem zu jedem Video bereits der Titel, der:die Dozierende, das Erstelldatum, ein Vorschaubild und die Dauer des Videos angezeigt. Bei Anklicken dieses Videobereichs wird man auf die [Videoansicht](userguide.md#videoansicht) weitergeleitet. 


##### Kursansicht
In der Kursansicht finden Sie alle Vorlesungsvideos eines Kurses. Diese sind nun untereinander angeordnet und jeder Videoblock enthält die gleichen Informationen wie in der Homeansicht. Durch Anklicken eines Videoblocks wechseln Sie zu dessen [Videoansicht](setup.md#videoansicht). Hier besteht die Möglichkeit ein Video oder gleich alle Videos des Kurses herunterzuladen. Dadurch klickt man entweder auf das Download Symbol (Pfeil nach unten) rechts neben dem Titel eines Videos oder auf das Download-Symbol ganz oben rechts neben dem Kurstitel. 

##### Videoansicht
Die Videoansicht wird durch den auf die App zugeschnittenen [Video Player](implementation/player.md) umgesetzt und bildet das Herzstück unserer Anwendung. Hier können Sie die Vorlesungsvideos anschauen. Unter dem Video lesen Sie eine Beschreibung des Vorlesungsinhalts. Über ein Menü erhalten Sie die Auswahlmöglichkeit zwischen unterschiedlichen Wiedergabeschwindigkeiten, Auflösungen und falls vorhanden auch auf verschiedene Ansichten des Vorlesungsvideos, beispielsweise der Foliensicht und der Sicht auf den:die Dozierende:n. Außerdem sind die Standardoptionen verfügbar, wie Start/Stopp des Videos in der Mitte des Bildschirms, 15 Sekunden zurück- oder vorspringen durch Doppelklicken im linken oder rechten Bereich des Videos und der Wechsel in den Vollbildmodus durch Anklicken des bekannten Symbols unten rechts. 

### Suche 
In der Ansicht Suche haben Sie die Möglichkeit  neue Kurse zu abonnieren. Dazu geben Sie einige Buchstaben des Titels, der:des Dozent:in oder der Beschreibung ein. Nach einer Sekunde erscheinen dann die zur Anfrage passenden Kurse der Universität oder Fachhochschule des:der Student:in. Durch vertikales Scrollen nach unten können noch weitere passende Kurse nachgeladen werden. Zum Abonnieren eines Kurses drücken Sie auf das Plus-Symbol des entsprechenden Kurses.

Daraufhin öffnet sich ein Bereich, in dem Sie das Semester auswählen können, in dem der Kurs abonniert werden soll. Voreingestellt ist das aktuelle Semester. Es ist aber auch möglich das vorherige oder nächste Semester zu wählen. Außerdem erscheint in diesem Auswahlbereich auch ein Feld für einen Einschreibeschlüssel, sofern der:die Dozent:in einen hinterlegt hat. In dem Fall können sich Studierende nicht ohne korrekte Eingabe des Einschreibeschlüssels zu dem Kurs anmelden. 

Falls ein Kurs nicht durch einen Einschreibeschlüssel geschützt ist, können Sie bereits vor dem Abonnieren durch Klicken auf den Kursnamen zur Kursansicht gelangen. 

### Einstellungen
In den Einstellungen sehen Sie ganz oben mit welchen Nutzerdaten Sie angemeldet sind. Darunter haben Sie die Möglichkeit die Sprache der App zu wählen. Zur Zeit stehen Englisch und Deutsch zur Verfügung. Außerdem können Sie hier ihre Downloads verwalten. Das bedeutet, dass Sie einen Überblick über all Ihre heruntergeladenen Videos nach Kursen sortiert bekommen. Eine Löschfunktion steht für jedes Video, alle Videos eines Kurs und alle Videos insgesamt zur Verfügung. Darüber hinaus können Sie sich von unserer App auch wieder abmelden. Dadurch gelangen Sie wieder auf die Startseite, auf welcher Sie zum Login aufgefordert werden.  

### Offline-Modus
Sollten Sie keinen Internetempfang haben, stehen Ihnen dennoch umfangreiche Funktionen zur Verfügung. Im Prinip bleiben sowohl Homeansicht, wie auch Kursansicht und Videoansicht gleich mit dem Unterschied, dass nun nur heruntergeladene Videos angezeigt werden. Wie Sie Videos herunterladen können, können Sie [hier](userguide.md#kursansicht) nachlesen. 
In der Suche werden Sie darauf hingewiesen, dass Sie zur Zeit keinen Internetempfang haben, denn diese Funktion steht Ihnen nur online zur Verfügung.  