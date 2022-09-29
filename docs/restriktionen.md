# Restriktionen 

Wie jede andere Software auch, unterliegt auch die mobile educast.nrw App gewissen Restriktionen, beziehungsweise konnten ein paar wenige Funktionalitäten leider (noch) nicht so umgesetzt werden, wie erwünscht. 


* Grundsätzlich ist die **Aktualisierbarkeit des Flick Videoplayers** eingeschränkt, da dessen Paket lokal integriert und leicht verändert werden musste, um es auf unsere Anforderungen anzupassen. Dies bedeutet, dass Updates des Flick Videplayers nicht automatisiert in unsere App übernommen werden können, sondern manuell in den Code eingefügt werden müssen. Weitere Informationen zum Player finden Sie [hier](implementation/player.md).

* Darüber hinaus ist das **Auswählen des Player Menüs bisher nur im Hochformat** möglich. Dies ist eine Funktion, welche nicht von dem Flick Videoplayer bereitgestellt wird. Auch nach ausführlichem Suchen und Austesten diverser Workarounds ist es uns leider nicht gelungen dieses Problem zu lösen. Ein möglicher weiterer Ansatz wäre der Austausch der Dropdown Buttons durch Custom Dropdownbuttons des Pakets [*cool_dropdown*](https://pub.dev/packages/cool_dropdown). Weitere Informationen zum Player finden Sie [hier](implementation/player.md). 

* Außerdem sind **Untertitel nur einzeilig** möglich. Mehrzeilige Untertitel werden demnach in einer Zeile dargestellt. Der Fehler liegt in der Klasse [*WebVttCaptionFile*](https://pub.dev/documentation/video_player_extra/latest/video_player/WebVTTCaptionFile-class.html) vom Flutter Player. Weitere Informationen zum Player finden Sie [hier](implementation/player.md).

* Daneben sind **Downloads nur auf Android abspielbar**. Hierbei liegt der Fehler scheinbar im Flutter Player beim Abspielen lokaler Dateien, da die Datei [*VideoPlayerController.file*](https://pub.dev/documentation/video_player/latest/video_player/VideoPlayerController-class.html) fehlerhaft ist. Weitere Infomationen zu dem [Download von Videos](implementation/download.md) und dem [Video Player](implementation/player.md) finden Sie unter den entsprechenden Links.

* Des Weiteren wird beim Download von Videos nicht gespeichert, in welchem Semester der zugehörige Kurs abonniert wurde. Dies führt dazu dass **im offline-Modus alle Kurse und zugehörigen Videos im aktuellen Semester angezeigt** werden. Weitere Informationen zum Download von Videos finden Sie [hier](implementation/download.md).

* Ein Formfehler tritt im [Loginprozess](login.md) auf iOS auf. Dort wird bei der Eingabe der Nutzerkennung der **Anfangsbuchstabe immer groß** geschrieben. Da dies allerdings die Anmeldeseite des DFN-AAI betrifft, konnten wir diesen Fehler leider nicht beheben. 

