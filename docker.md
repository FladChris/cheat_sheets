## Docker Cheat Sheet

### Installation & Setup

| Befehl                                                        | Beschreibung                             |                                                 |
| ------------------------------------------------------------- | ---------------------------------------- | ----------------------------------------------- |
| \`curl -fsSL [https://get.docker.com](https://get.docker.com) | sh\` Docker Engine installieren (offizielles Skript) |
| `sudo apt update && sudo apt install docker.io`               | Docker über Paketmanager (Debian/Ubuntu) |                                                 |
| `sudo systemctl enable --now docker`                          | Docker-Dienst aktivieren und starten     |                                                 |
| `docker version`                                              | Installierte Docker-Version anzeigen     |                                                 |
| `docker info`                                                 | Systeminformationen und Status           |                                                 |

### Images

| Befehl                   | Beschreibung                     |
| ------------------------ | -------------------------------- |
| `docker pull <image>`    | Image aus Registry herunterladen |
| `docker images`          | Lokale Images auflisten          |
| `docker rmi <image>`     | Lokales Image löschen            |
| `docker tag <src> <tag>` | Image umbenennen/taggen          |

### Container Management

| Befehl                                  | Beschreibung                                       |
| --------------------------------------- | -------------------------------------------------- |
| `docker run -d --name <name> <image>`   | Container im Hintergrund starten                   |
| `docker run -it --rm <image> /bin/bash` | Interaktives Terminal und Container danach löschen |
| `docker ps`                             | Laufende Container auflisten                       |
| `docker ps -a`                          | Alle Container (inkl. gestoppter)                  |
| `docker stop <container>`               | Container stoppen                                  |
| `docker start <container>`              | Container starten                                  |
| `docker restart <container>`            | Container neu starten                              |
| `docker kill <container>`               | Container sofort beenden (SIGKILL)                 |
| `docker rm <container>`                 | Beendeten Container löschen                        |
| `docker logs <container>`               | Logs eines Containers anzeigen                     |
| `docker exec -it <container> <cmd>`     | Befehl in laufendem Container ausführen            |

### Netzwerke

| Befehl                               | Beschreibung                     |
| ------------------------------------ | -------------------------------- |
| `docker network ls`                  | Netzwerke auflisten              |
| `docker network create <name>`       | Neues Netzwerk erstellen         |
| `docker network connect <net> <ctr>` | Container mit Netzwerk verbinden |
| `docker network inspect <net>`       | Netzwerkdetails anzeigen         |
| `docker network rm <name>`           | Netzwerk löschen                 |

### Volumes & Bind Mounts

| Befehl                                 | Beschreibung                          |
| -------------------------------------- | ------------------------------------- |
| `docker volume ls`                     | Volumes auflisten                     |
| `docker volume create <name>`          | Neues Volume erstellen                |
| `docker volume inspect <name>`         | Volume-Details anzeigen               |
| `docker volume rm <name>`              | Volume löschen                        |
| `docker run -v <host>:<ctr> <image>`   | Host-Verzeichnis in Container mounten |
| `docker run -v <volume>:/data <image>` | Volume in Container mounten           |

### Docker Compose

| Befehl                            | Beschreibung                                     |
| --------------------------------- | ------------------------------------------------ |
| `docker-compose up -d`            | Dienste im Hintergrund starten                   |
| `docker-compose up --build`       | Build und starten                                |
| `docker-compose down`             | Dienste stoppen und Ressourcen entfernen         |
| `docker-compose ps`               | Status der Dienste anzeigen                      |
| `docker-compose logs [<service>]` | Logs aller oder eines bestimmten Dienstes zeigen |
| `docker-compose exec <svc> <cmd>` | Befehl im Dienst-Container ausführen             |

### Dockerfile-Grundlagen

| Befehl                           | Beschreibung                                        |
| -------------------------------- | --------------------------------------------------- |
| `FROM <image>`                   | Basis-Image festlegen                               |
| `RUN <cmd>`                      | Befehl beim Build ausführen                         |
| `COPY <src> <dst>`               | Dateien vom Host in das Image kopieren              |
| `ADD <src> <dst>`                | Wie COPY, mit zusätzlicher URL/Entpackungs-Funktion |
| `WORKDIR <dir>`                  | Arbeitsverzeichnis setzen                           |
| `ENV <key>=<val>`                | Umgebungsvariable definieren                        |
| `EXPOSE <port>`                  | Port im Container freigeben                         |
| `CMD [\"executable\",\"param\"]` | Standardkommando beim Containerstart                |
| `ENTRYPOINT [\"cmd\"]`           | Festes Start-Kommando festlegen                     |

### Aufräumen

| Befehl                             | Beschreibung                      |
| ---------------------------------- | --------------------------------- |
| `docker container prune`           | Alle gestoppten Container löschen |
| `docker image prune`               | Ungenutzte Images löschen         |
| `docker volume prune`              | Unbenutzte Volumes löschen        |
| `docker network prune`             | Unbenutzte Netzwerke löschen      |
| `docker system prune -a --volumes` | Alles nicht Genutzte entfernen    |
