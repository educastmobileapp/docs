# Anforderungen
In diesem Abschnitt sind die Anforderungen an die App aufgelistet.

Die Hauptaufgabe der App ist das Abspielen von Vorlesungsvideos auf dem mobilen Endgerät. Die Videos sind auf dem educast.nrw Server der jeweiligen Hochschule der Studierenden gespeichert. Von den Servern aus werden die Inhalte beim abspielen der Videos geladen.

## Der Player
Der Player ist ein Zentraler Bestandteil der App und halt viele Funktionen, neben dem abspielen und pausieren der Videos.

So kann man die Qualität und die Wiedergabegeschwindigkeit ändern. Mit einem Doppelklick auf dem Bildschirm auf der linken bzw. rechten Seite lässt sich das Video vor bzw. zurück spulen, so dass die Studierenden sich z.B. komplexe Inhalte einfach nochmal anschauen können.

Der Videofortschritt wird auch Geräteübergreifend gespeichert. Nach einer Pause können die Studierenden genau an der richtigen Position das Video weiter schauen.

Bei der Aufzeichnung von Vorlesungen gibt es oft zwei Ansichten. Eine Ansicht von den Folien und eine von der Vortragenden Person. Deshalb gibt es eine Funktion zum Wechseln der Ansicht.

## Login
Des Weiteren ist eine Anmeldefunktion benötigt. Hier melden sich die Studierenden mit ihrer Hochschulkennung und ihren Passwörtern an. Dieselben Anmeldedaten, die auch für andere Hochschule bezogene IT-Dienste benötigt sind. So ist sichergestellt das nur berechtigte Personen die App nutzen können. Außerdem können individuelle Einstellungen gespeichert werden. Zuletzt ermöglicht die Anmeldung die Identifizierung der Hochschulzugehörigkeit der Studierenden. Dies ist für die Auswahl des richtigen educast.nrw Servers nötig.

Die Studierenden bleiben 6 Monate lang angemeldet und müssen sich nicht jeden Tag neu anmelden. Außerdem können die Studierenden in den Einstellungen ihren Namen und ihre E-Mail einsehen, um so festzustellen wer gerade angemeldet ist.

## Einschreibeschlüssel
Da ein Großteil der Vorlesungen und somit auch der Vorlesungsvideos mit einem Einschreibeschlüssen gesichert sind, ist eine sichere Funktion zum Abfragen des Einschreibeschlüssells notwendig.

## Benutzeroberfläche
Außerdem wird eine intuitive UI Struktur benötigt, mit der durch die App navigieren werden kann.

## Sprachauswahl
Für die Barrierefreiheit der App ist die Option der Sprachauswahl wichtig. In den Einstellungen kann zwischen Deutsch und Englisch gewechselt werden. So wird die Nutzung der App auch internationalen Studenten ermöglicht.

## Download
Eine weitere Wichtige Funktion, ist das Downloaden der Videos und spätere abspielen ohne eine Internetverbindung. Dies ermöglicht zum Beispiel das Schauen von Vorlesungsvideos in der Deutschen Bahn unabhängig von einer stabilen Internetverbindung. Ein entscheidender Vorteil der Mobilen App, im Vergleich zum Anschauen der Videos im Browser.

Im Browser ist kein Download möglich, da nicht sichergestellt werden kann, dass die Videos nicht an unbefugte weitergegeben werden. Bei der educast App werden die Videos in einem sicheren App spezifischen Bereich gespeichert, so dass nicht außerhalb der App darauf zugegriffen werden kann.

Es ist möglich einzelne Videos zu downloaden, sowie alle Videos einer Vorlesung zusammen. In den Einstellungen kann man die Videos wieder löschen und es gibt auch die Möglichkeit alle Videos auf einmal zu löschen.

## Performance
Auch die Performance der App ist wichtig. Es wird vermieden redundante Requests an den Server zu senden, stattdessen werden Informationen die später noch gebraucht werden im App internen Cache gehalten. So werden zum Beispiel die Thumbnails der Vorlesungsvideos gecached. Dies geschieht auf Grund ihrer Größe und da sie für die Vorschau in der Home View benötigt werden. Sodass diese nicht bei jedem Neustart der App neu heruntergeladen werden müssen.

Dadurch wird Internetbandbreite eingespart und jene Elemente können schneller angezeigt werden. Außerdem werden auch viele Requests im Backend für 15 Minuten gecached. So wird die Antwort Zeit von häufigen Anfragen beschleunigt und Rechenleistung vom Server geschont, wodurch größere Nutzerzahlen weniger problematisch sind.
