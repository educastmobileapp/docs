# Technisches Setup des Systems

## Backend
Damit die App funktioniert, muss zuerst das Backend aufgesetzt werden.

Hierfür ist ein Server mit Linux zu empfehlen, ein anderes OS würde aber durchaus auch funktionieren. 


### Installation
Nach erfolgreichem Aufsetzen des Servers und Installierens von Python (Version >= 3.7) den Source Code herunterladen mit  
`git clone https://zivgitlab.uni-muenster.de/educast-nrw/student-work/app/backend.git`

Alle vom Backend verwendeten Dependencies können anschließend mit pip installiert werden:  
`cd backend`  
`pip install -r requirements.txt`

### Config erstellen
Als nächstes muss die Config aufgesetzt werden. Der einfachste Weg dazu ist, das Programm zu starten, sodass eine leere Konfigurationsdatei erstellt wird.  
`python main.py [--config '/path/to/.login.yaml']`  
Wenn keine Config-Flag übergeben wird, wird die Konfigurationdatei '.login.yaml' im home-Directory des aktuellen Users erstellt. Durch Verwendung des Arguments kann die Datei einen anderen Pfad und Namen bekommen, wobei wichtig ist, dass der Dateityp YAML ist.

### Konfiguration
In der Konfigurationsdatei müssen die Login-Credentials für die verwendeten API-User, sowie für die MySQL-Datenbank angeben werden.  # TODO private key

##### API-User
Die API-User müssen in der Section `apiuser` konfiguriert werden. Jeder dieser User ist eine weitere Section, die benannt ist mit der dazugehörigen Domain der jeweiligen Universität. Dies ist wichtig, um die API-Requests, bei Studierenden von unterschiedlichen Universitäten, dem richtigen API-User zu schicken.  
Die Section ist ein Dictionary mit den String-Werten `url`, `username` und `password`.

Für die Uni Münster würde die Konfiguration also wie folgt aussehen.
```yaml
apiuser:
  uni-muenster.de:
    url: https://link.to.uni-muenster.educast.de/api
    username: 'username'
    password: 'password'
```
Die Section `apiuser` kann beliebig viele API-User enthalten, bzw. sollte für jede Uni, die den educast.nrw nutzt, einen enthalten.


##### Datenbank
Die Section `database` konfiguriert die Verbindung zur MySQL-Datenbank. Hier müssen die Host-Addresse, die verwendete Datenbank und der User konfiguriert werden. Der User muss Schreibzugriff in der Datenbank haben, alle genutzten Tabellen werden dann automatisch erstellt.

```yaml
database:
  database: backend
  host: localhost
  user: 'username'
  password: 'password'
```

##### Keypair

TODO: Keypair erklären

### Server starten
Nach erfolgreichem Konfigurieren kann das Backend gestartet werden. Zum Starten folgenden Befehl ausführen:  
`python main.py`  
Wenn gewünscht, kann der Pfad der Konfigurationsdatei mit dem Argument `--config '/path/to/.login.yaml'` übergeben werden.

Der Server wird standardmäßig auf Port 80 gestartet. Auch das ist anpassbar mit dem Argument `--port 8080`. Meistens werden zum binden eines Ports unter 1000 Root-Rechte benötigt.

## Frontend

Die App ist mit dem Framework [Flutter](https://flutter.dev/) in [Dart](https://dart.dev/) geschrieben. Der erste Schritt um die App zu kompilieren ist, Flutter nach der [offiziellen Anleitung](https://docs.flutter.dev/get-started/install) zu installieren.

### Kompilierung

#### Android
Um die App für Android zu kompilieren muss das Appbundle oder die APK gebaut werden. Das Appbundle enthält die APKs für unterschiedliche Laufzeiten (ARM 32-bit, ARM 64-bit, x86 64-bit) und ist deshalb vom Google Playstore bevorzugt. Zum erstellen muss im Projektordner `flutter build appbundle` ausgeführt werden. Anschließend ist es unter `/build/app/outputs/bundle/release/app.aab` zu finden.

Um die APKs zu kompilieren muss `flutter build apk --split-per-abi` ausgeführt werden. Die Flag führt dazu, dass für die unterschiedlichen Laufzeiten eigene APKs erstellt werden, anstatt eine Große, die den kompilierten Code von allen enthält. Anschließend können alle gebauten APKs unter `/build/app/outputs/bundle/release` gefunden werden.

Um die App nun direkt auf einem Gerät zu installieren, muss es über USB angeschlossen werden und USB-Debugging in den Einstellungen aktiviert sein. Anschließend reicht es `flutter install` auszuführen und der richtige Build wird installiert.


