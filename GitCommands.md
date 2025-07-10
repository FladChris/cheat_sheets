# Git Cheat Sheet

## 1. Repository anlegen & klonen

| Befehl                                 | Beschreibung                                         |
|----------------------------------------|------------------------------------------------------|
| `git init`                             | Neues Git-Repository im aktuellen Verzeichnis anlegen |
| `git clone <url>`                      | Repository von Remote-Server klonen                   |
| `git clone <url> <ziel-verzeichnis>`   | Klonen und in bestimmtes Verzeichnis legen            |

## 2. Arbeitsverzeichnis & Staging

| Befehl                                 | Beschreibung                                         |
|----------------------------------------|------------------------------------------------------|
| `git status`                           | Aktuellen Status anzeigen (geänderte, neue Dateien)   |
| `git diff`                             | Unterschiede im Arbeitsverzeichnis anzeigen          |
| `git add <datei>`                      | Datei zum Staging-Bereich hinzufügen                 |
| `git add .`                            | Alle Änderungen zum Staging-Bereich hinzufügen       |
| `git reset <datei>`                    | Datei aus dem Staging-Bereich entfernen              |
| `git reset`                            | Staging-Bereich komplett zurücksetzen                |

## 3. Commits

| Befehl                                         | Beschreibung                             |
|------------------------------------------------|------------------------------------------|
| `git commit -m "<nachricht>"`                  | Änderungen committen mit kurzer Nachricht |
| `git commit -a -m "<nachricht>"`               | Automatisch alle geänderten Dateien adden und committen |
| `git commit --amend`                           | Letzten Commit korrigieren oder Nachricht ändern |

## 4. Branching & Merging

| Befehl                                     | Beschreibung                                         |
|--------------------------------------------|------------------------------------------------------|
| `git branch`                               | Lokale Branches auflisten                            |
| `git branch <name>`                        | Neuen Branch anlegen                                 |
| `git checkout <name>`                      | Zu anderem Branch wechseln                           |
| `git switch <name>`                        | (Neuere Alternative zu `checkout`)                   |
| `git checkout -b <name>`                   | Neuen Branch anlegen und direkt wechseln             |
| `git merge <branch>`                       | Anderen Branch in aktuellen Branch mergen            |
| `git rebase <branch>`                      | Aktuellen Branch auf Basis eines anderen neu anordnen |

## 5. Remote-Repositories

| Befehl                                      | Beschreibung                                      |
|---------------------------------------------|---------------------------------------------------|
| `git remote -v`                             | Remote-Quellen auflisten                          |
| `git remote add <name> <url>`               | Neuen Remote anlegen                              |
| `git fetch <remote>`                        | Neue Referenzen vom Remote herunterladen          |
| `git pull <remote> <branch>`                | `fetch` + `merge`: Änderungen vom Remote holen und mergen |
| `git push <remote> <branch>`                | Lokalen Branch zum Remote senden                  |
| `git push -u <remote> <branch>`             | Branch erstmalig pushen und Tracking setzen       |

## 6. Historie & Logs

| Befehl                                     | Beschreibung                                           |
|--------------------------------------------|--------------------------------------------------------|
| `git log`                                  | Commit-Historie anzeigen                               |
| `git log --oneline --graph --decorate`     | Kompakte, grafische Historie                           |
| `git show <commit>`                        | Details zu einem bestimmten Commit                     |
| `git blame <datei>`                        | Zeilenweises Anzeigen, wer wann was geändert hat       |

## 7. Rückgängig machen & Korrektur

| Befehl                                       | Beschreibung                                       |
|----------------------------------------------|----------------------------------------------------|
| `git checkout -- <datei>`                    | Änderungen im Arbeitsverzeichnis verwerfen         |
| `git revert <commit>`                        | Neuen Commit erstellen, der einen alten rückgängig macht |
| `git reset --soft <commit>`                  | HEAD auf Commit setzen, Änderungen bleiben gestaged |
| `git reset --mixed <commit>`                 | HEAD auf Commit setzen, Staging zurücksetzen       |
| `git reset --hard <commit>`                  | HEAD auf Commit setzen, Arbeitsverzeichnis zurücksetzen (!!! Datenverlust) |

## 8. Stashing

| Befehl                                     | Beschreibung                                               |
|--------------------------------------------|------------------------------------------------------------|
| `git stash`                                | Änderungen stashen (temporär sichern und Arbeitsverzeichnis sauber) |
| `git stash list`                           | Alle Stashes auflisten                                     |
| `git stash apply [<stash> ]`               | Stash wieder anwenden ohne zu löschen                      |
| `git stash pop`                            | Stash anwenden und aus Liste entfernen                     |
| `git stash drop <stash>`                   | Stash aus Liste löschen                                    |

## 9. Tags

| Befehl                                     | Beschreibung                                           |
|--------------------------------------------|--------------------------------------------------------|
| `git tag`                                  | Alle Tags anzeigen                                     |
| `git tag <name>`                           | Leichtgewicht-Tag erstellen                            |
| `git tag -a <name> -m "<nachricht>"`       | Annotierten Tag erstellen                              |
| `git push <remote> <tag>`                  | Tag zum Remote pushen                                  |
| `git push <remote> --tags`                 | Alle lokalen Tags zum Remote senden                    |

## 10. Konfiguration

| Befehl                                     | Beschreibung                                             |
|--------------------------------------------|----------------------------------------------------------|
| `git config --global user.name "<name>"`   | Namen für alle Repos setzen                              |
| `git config --global user.email "<email>"` | E-Mail für alle Repos setzen                             |
| `git config --list`                        | Alle Konfig-Einstellungen anzeigen                        |
| `git config <scope> core.editor "<editor>"`| Standard-Editor für Git-Kommandos festlegen (`system`, `global` oder `local`) |
