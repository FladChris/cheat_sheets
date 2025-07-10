## Linux Shell Cheat Sheet

### Navigation

| Befehl             | Beschreibung                   |
| ------------------ | ------------------------------ |
| `pwd`              | Aktuelles Verzeichnis anzeigen |
| `ls`               | Dateien und Ordner auflisten   |
| `ls -l`            | Liste im Langformat            |
| `cd <verzeichnis>` | In Verzeichnis wechseln        |
| `cd ..`            | Eine Ebene nach oben wechseln  |

### Datei- und Verzeichnis-Operationen

| Befehl               | Beschreibung                                  |
| -------------------- | --------------------------------------------- |
| `touch <datei>`      | Neue Datei erstellen                          |
| `mkdir <ordner>`     | Neues Verzeichnis erstellen                   |
| `cp <quelle> <ziel>` | Datei oder Verzeichnis kopieren               |
| `mv <quelle> <ziel>` | Datei oder Verzeichnis verschieben/umbenennen |
| `rm <datei>`         | Datei löschen                                 |
| `rm -r <ordner>`     | Verzeichnis rekursiv löschen                  |
| `cat <datei>`        | Dateiinhalt anzeigen                          |
| `head -n 10 <datei>` | Erste 10 Zeilen anzeigen                      |
| `tail -n 10 <datei>` | Letzte 10 Zeilen anzeigen                     |

### Prozessverwaltung

| Befehl          | Beschreibung                            |
| --------------- | --------------------------------------- |
| `ps`            | Aktive Prozesse auflisten               |
| `ps aux`        | Detaillierte Prozessliste               |
| `top`           | Interaktive Prozessübersicht            |
| `htop`          | Erweiterte, farbliche Prozessübersicht  |
| `kill <PID>`    | Prozess beenden (mit SIGTERM)           |
| `kill -9 <PID>` | Prozess erzwingen abzubrechen (SIGKILL) |
| `pkill <name>`  | Prozesse nach Name beenden              |

### Suche & Filter

| Befehl                            | Beschreibung                    |
| --------------------------------- | ------------------------------- |
| `grep 'pattern' <datei>`          | In Datei nach Pattern suchen    |
| `grep -r 'pattern' <verzeichnis>` | Rekursiv in Verzeichnis suchen  |
| `find . -name '*.sh'`             | Dateien nach Name suchen        |
| `locate <name>`                   | Dateien anhand Datenbank finden |
| `which <befehl>`                  | Pfad eines Befehls anzeigen     |

### Berechtigungen

| Befehl                     | Beschreibung                           |
| -------------------------- | -------------------------------------- |
| `chmod 755 <datei>`        | Dateiberechtigungen ändern (rwxr-xr-x) |
| `chmod +x <script.sh>`     | Ausführbar-Flag setzen                 |
| `chown user:group <datei>` | Eigentümer und Gruppe ändern           |
| `sudo <befehl>`            | Befehl als root (Superuser) ausführen  |

### Ein- und Ausgabe

| Befehl                  | Beschreibung                               |                                               |
| ----------------------- | ------------------------------------------ | --------------------------------------------- |
| `command > output.txt`  | Standardausgabe in Datei umleiten          |                                               |
| `command >> output.txt` | An Datei anhängen                          |                                               |
| `command < input.txt`   | Standardinput aus Datei lesen              |                                               |
| \`command1              | command2\`                                 | Ausgabe von command1 an command2 weiterleiten |
| `tee output.txt`        | Ausgabe auf Konsole und in Datei schreiben |                                               |

### Archivierung & Kompression

| Befehl                              | Beschreibung                        |
| ----------------------------------- | ----------------------------------- |
| `tar -cvf archiv.tar <dateien>`     | Archiv erstellen                    |
| `tar -xvf archiv.tar`               | Archiv entpacken                    |
| `tar -czvf archiv.tar.gz <dateien>` | Gzip-komprimiertes Archiv erstellen |
| `tar -xzvf archiv.tar.gz`           | Gzip-entpacken                      |
| `zip -r archiv.zip <verzeichnis>`   | ZIP-Archiv erstellen                |
| `unzip archiv.zip`                  | ZIP-Archiv entpacken                |

### Netzwerk

| Befehl          | Beschreibung                |
| --------------- | --------------------------- |
| `ping <host>`   | Host anpingen               |
| `curl <url>`    | HTTP-Anfrage senden         |
| `wget <url>`    | Datei von URL herunterladen |
| `ssh user@host` | SSH-Verbindung herstellen   |
| `scp src dst`   | Datei per SCP kopieren      |

### Paketverwaltung (Debian/Ubuntu)

| Befehl                     | Beschreibung               |
| -------------------------- | -------------------------- |
| `sudo apt update`          | Paketlisten aktualisieren  |
| `sudo apt upgrade`         | Pakete aktualisieren       |
| `sudo apt install <paket>` | Paket installieren         |
| `sudo apt remove <paket>`  | Paket entfernen            |
| `sudo apt autoremove`      | Verwaiste Pakete entfernen |

